---
layout: post
title:  "简单介绍显卡新技术 RTRT, DLSS and RIS"
author: lightfocus
categories: [ Graphics ]
tags: [ Technology ]
image: "https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/cover/ray-tracing.jpg"
---
现在的新显卡除了绝对游戏性能以外，独家功能也是一大卖点。NVIDIA的20系显卡带来了RT和DLSS，而AMD的Navi显卡带来了RIS。对于消费者来说可能对这些功能不太熟悉，因此本文简单介绍这些功能背后的原理。

<h1>光线追踪：追的是什么光线</h1>
自然界中，光源发出光线以后会沿直线传播，直到有阻止它前进的物体。当然，传播的过程中会遇到三种情况：折射、反射、吸收。当光源发出的一部分光线通过一系列折射反射以后进入我们的眼睛，就形成了我们看见的场景。

为了模拟更真实的光照效果，我们不难想到，让计算机模拟现实的情况，计算从光源发出的每一条光线以及它在传播过程中的各种反射折射。这对于一帧静态的图片问题不大，因为我们可以有很长的时间渲染。但是对于游戏这种实时的、并且需要每秒钟渲染几十张画面的应用来说，上述方法太复杂，因此我们必须将其简化。

上述方法最大的问题在于，从光源出发的光线，最终会有很大一部分被物体吸收而没有传到“眼睛”——也就是摄像机里面。这里的摄像机就是指观察场景的窗口，通常就是我们看到的画面。那我们可以换一个思路，如果只计算那些最后进入到摄像机的光线，那就相对于计算的每一条光线都是对我们最后渲染有意义的光线，效率达到最高。

但是那些光线是最终进入到摄像机的呢？我们只能通过逆向推导的方式得知。也就是反过来从摄像机出发，发出一条想象中的光线，通过一系列反射折射直到出现下列情况之一，则停止追踪：该光线不与任意平面相交、该光线与光源相交且光源不是反射面、达到允许的最大追踪深度。上述算法即为光线追踪的基本算法。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/ray-tracing/ray_trace_diagram.jpg" style="margin: 0 auto; width: 80%;">
</div>

计算过程中，我们需要知道每一次折射、反射的系数，并通过下面几个公式推导出当前像素点的颜色值。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/ray-tracing/ray_tracing_illustration_first_bounce.png" style="margin: 0 auto; width: 80%;">
</div>

上图②式中，ka表示环境光反射系数，Ia表示环境光强度，Ii表示点光源，Kd表示漫反射系数，L为点光源单位方向向量，N为观察方向单位法向量，Ks表示一个固定的镜面反射系数，V为观察方向单位法向量，R为镜面反射方向向量，n为镜面反射参数。

在不考虑递归的情况下，上式可以写为：

<h2>I = Idiff + Ispec = Ka*Ia + Kd*Ii*(N*L) + Ks*Ii*(N*H)^n</h2>

该公式即表示光照表明上某点处的漫反射与镜面反射。
<h1>不只算法，还有硬件革新</h1>
上述算法很早以前就提出，但是一直没有运用到游戏里面。那为什么这次NVIDIA的20系显卡可以做到光线追踪呢？

我们不妨先看看新显卡的架构：

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/ray-tracing/6071743d-b2ac-46aa-865e-02273980932b.png" style="margin: 0 auto; width: 80%;">
</div>

可以看到，Turing架构配备了RT Cores。根据NVIDIA的说法，新显卡和上一代比起来在光线追踪上快了8倍。那么问题来了，RT Cores是怎么做到硬件加速的呢？

RT Cores其实是对BVH（Bounding volume hierarchy）做了加速。BVH把集合对象包裹在树的叶子节点中，越接近根节点则包含的对象越多。下图就是一个BVH的例子。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/ray-tracing/1000px-example_of_bounding_volume_hierarchy.jpg" style="margin: 0 auto; width: 80%;">
</div>

那这和光线追踪有什么关系呢？

光线追踪过程中，95%的时间都用于计算光线与表明求交。如果一个场景有多个对象，则可能出现计算光线与不可见对象的求交。因此我们可以将相邻对象用一个包围体包起来（即BVH），如果光线与该包围体没有交点，则不需要计算包围体里面的任何对象，大大减少计算时间。

别忘了上面架构图里面还有Tensor Cores，这就涉及到下一个技术，DLSS了。
<h1>DLSS，脑补出来的画面</h1>
DLSS全称Deep Learning Super Sampling，从名字就可以看出，这是一项利用深度学习实现的技术。一句话概括就是低分辨率生成高分辨率，提升帧数。DLSS有两代，原理上不太相同。
<h2>DLSS 1.0</h2>
需要针对每一个游戏训练神经网络，因此这个时候只支持战地5和地铁：离去。

简单来说就是游戏厂商提供至少64张8K原始图像去训练一个模型。在游戏过程中利用1080p或者2K的图像先生成8K的图像，再缩到4K显示，以实现2倍DLSS的效果。

第一代DLSS的问题主要有以下几个：每个游戏都需要训练、只能运行在4K分辨率，清晰度不算太高。
<h2>DLSS 2.0</h2>
2019年8月，DLSS2.0首先被用在Control这个游戏上，但是这一次没有使用AI技术。

2020年4月，NVIDIA发布了445.75驱动，提供了DLSS2.0。这个DLSS2.0同样使用了AI技术，但是不再需要对每一个游戏进行训练。

NVIDIA使用低分辨率图像和对应的高分辨率图像训练神经网络，并将神经网络存储在驱动里面。

游戏进行时，游戏引擎将低分辨率图像给DLSS，并由DLSS生成高分辨率图像。除此之外，游戏引擎还提供了运动矢量，以便DLSS预测下一帧图像应该是什么样子。

DLSS2.0增加了普适性，而且效果也比第一代DLSS好。
<h1>RIS：另一种方法？</h1>
AMD在推出Navi显卡的同时介绍了一项新技术：RIS（Radeon Image Sharpening），也就是图像锐化。它会针对游戏中每一帧画面做对比度分析，对于对比度高的边缘部分进行锐化，让低分辨率的图像看上去更锐。

除此之外，RIS也能很好改善后期抗锯齿带来的模糊感。以FXAA为例，它会首先通过寻找深度差异较大的物体以确定边缘，然后将边缘模糊。这种技术虽然性能好，但是因为不是通过超采样得到的平滑边缘，所以整个画面会模糊。而RIS技术就可以解决这种后期抗锯齿所带来的问题。

较DLSS更优的是，此技术不需要做任何额外适配，只需要开启RIS和GPU缩放即可。