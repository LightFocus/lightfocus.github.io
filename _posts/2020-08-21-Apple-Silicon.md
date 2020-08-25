---
layout: post
author: Light Focus
title: 10周年回顾，Apple Silicon发展史
date: 2020-08-21T13:48:20.613Z
thumbnail: /assets/img/posts/A4-chip.jpg
category: Apple
summary: Past, Present and Future.
keywords: Apple, SoC
permalink: /blog/apple-silicon
---
<h1>Before A series chip, there were...</h1>
初代iPhone发布于2007年，那个时候用的芯片还不是苹果自己研发的。直到2010年自研的A4芯片，一共有4款芯片被用于不同的产品中。
<h2>APL0098</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/APL0098.jpg" style="margin: 0 auto; width: 50%;">
</div>

虽然基于90nm制程、单核412MHz的频率在现在看来各种落后，但是iPhone的一切始于此。这款芯片被用于初代iPhone和iPhone 3G，以及初代iPod Touch。值得一提的是，这是本文唯一一款16位的芯片。
<h2>APL0278</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/APL0278.jpg" style="margin: 0 auto; width: 50%;">
</div>

iPhone 3G发布后几个月问世，用于2代iPod Touch。本质上是0098的制程升级版，来到了65nm工艺，使得芯片面积小了一半，散热的改进使得频率可以更高。最重要的是升级到了32位内存寻址。
<h2>APL0298</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/APL0298.jpg" style="margin: 0 auto; width: 50%;">
</div>

和初代芯片相比，升级了65nm制程，频率提升了50%之多，应证了iPhone 3GS中的S代表Speed。
<h2>APL2298</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/APL2298.jpg" style="margin: 0 auto; width: 50%;">
</div>

最后一款非苹果自研芯片，45nm制程，更高的频率给3代iPod Touch带来了强劲的性能表现。
<h1>This changes everything. Again.</h1>
2010年，iPhone 4问世。正如它的广告语一样，iPhone 4再一次刷新了人们对智能手机的认识。但是很多人不知道的是，它的芯片已经改由苹果自己设计。同时也没人能料到这种花钱自己研发芯片的吃力不讨好的事情，能对后面的苹果产生什么影响。
<h2>A4</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A4.jpg" style="margin: 0 auto; width: 50%;">
</div>

乍一看这款芯片平平无奇，一样的45nm制程，稍高的频率，最大的升级就是换了双通道内存。但是不要忘记了，iPhone 4是苹果的第一款使用Retina Display的产品，相比之前4倍的像素数对于芯片性能是极大的挑战。苹果第一次交出的答卷显然很让人满意。
<h2>A5 & A5X</h2>
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A5.png" width="100%">

A5把注意力放到了一个点上：性能。两倍多的核心面积带来了苹果第一颗双核芯片。与此同时GPU升级到了PowerVR SGX543MP2使得A5的图形性能是A4的7倍之多，这个数字是前所未有的。如果你还记得iPhone 4S的发布会的话，介绍完A5之后就是Epic Games带来的无尽之剑2(Infinity Blade II)的实机演示。有许多桌面级的游戏特效，如粒子效果，动态光照等第一次被带到了移动设备上。这让人对苹果芯片的未来充满了期待。A5还第一次集成了图像信号处理单元（ISP），给iPhone 4S的相机成像带来了提升。

但是A5的故事到这里还没完。

在iPhone上的Retina Display大受欢迎后，苹果也想升级iPad的屏幕。但是同样想要实现Retina Display，iPad的像素是iPhone的5倍之多，现有的芯片带不动。

考虑到iPad有更大的散热空间和电池，苹果决定升级现有A5芯片上的GPU。A5X就这样问世了，它的图形性能比起A5还要翻倍。自此以后，X结尾的芯片成了iPad的专属“堆料”芯片。
<h2>A6 & A6X</h2>
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A6.png" width="100%">

这代是例行升级，除了制程升级到32nm之外没有太大的亮点。值得一提的是因为A5芯片用的时间跨度很大，所以后面出的A5芯片也从45nm升级到了32nm。
<h1>World's first and only smartphone</h1>
PC行业花了数年甚至十多年才完成32位到64位的转换过渡，苹果只花了一代处理器。
<h2>A7</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A7.jpg" style="margin: 0 auto; width: 50%;">
</div>

iPhone 5S作为第一款搭载64位处理器的手机，其意义非凡。这不仅代表了苹果在芯片设计方面走在前沿，同时也表明了苹果决心把自研芯片做成专业级的芯片。

除此之外，A7也首次配备了协处理器M7，可以不唤醒A7的情况下记录传感器数据，从而实现监控步数等有用健康信息却又不影响续航。因为iPhone 5S首次配备了Touch ID，所以A7还内置了专门保护指纹数据的一块“飞地”（Secure Enclave）。

可能是苹果对A7的性能太满意，以至于后续没有发布A7X。而是将A7的频率略微提高就用到了iPad Air上。
<h2>A8 & A8X</h2>
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A8.png" width="100%">

例行升级。可能是考虑到iPhone 6大屏对电池续航影响较大，A8把重点放在了节能上，功耗仅为A7的50%。
<h2>A9 & A9X</h2>
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A9.png" width="100%">

最后一代双核芯片，可以看出单核心性能已经被压榨的差不多了，之后只能通过堆核心来提升性能了。

另外A9有三星的14nm版本和台积电的16nm版本，在iPhone中混用。2015年10月时有报道称三星的版本电池续航会更短。
<h2>A10 Fusion & A10X Fusion</h2>
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A10.png" width="100%">

为了更加省电，苹果首次使用了大小核心的架构。2+2的核心配置使A10能在执行轻量化任务的情况下延长续航，不过大小核不能同时使用。
<h1>Take it to the next level.</h1>
2017年，为了纪念iPhone发布10周年，iPhone X问世。其中最引人瞩目的便是Face ID功能，为了实现支付级别的面部识别，苹果再一次大刀阔斧的改进自研芯片。
<h2>A11 Bionic</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A11.jpg" style="margin: 0 auto; width: 50%;">
</div>

苹果在之前的芯片中只自己设计CPU部分，GPU用的还是PowerVR的方案。从A11开始，GPU部分也由苹果设计。与此同时，因为用户外貌变化可能影响Face ID的识别准确率，苹果特意在A11芯片中加入了一个神经网络引擎，可以以硬件的方式加速运算。而新的控制器使得A11可以同时调用大小核，进一步提升性能。
<h2>A12 Bionic & A12X Bionic</h2>
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A12.png" width="100%">

在尝到神经网络引擎带来的甜头后，A12大幅升级了该引擎，使其每秒可以进行5万亿次运算。除此之外，A12也是手机上的首款7nm芯片。
<h2>A13 Bionic</h2>

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/Apple-A13.jpg" style="margin: 0 auto; width: 50%;">
</div>

来到今天，iPhone的性能一直是领先高通阵营半年到一年，甚至一度有领先桌面平台的趋势，作为苹果自己研发的芯片确属不易。而当苹果有能力把越来越多的功能集成到芯片中时，一个10年前的幻想慢慢变成现实。
<h1>Those long divided shall be united.</h1>
事情往往会往意想不到的方向发展，即使是10年前的苹果，也没有想到自研芯片能给他们带来什么。
<h2>A12Z Bionic</h2>
2010年6月24日，iPhone 4开售，标志着苹果自研芯片登上舞台。10年后，2020年6月22日，在WWDC2020上苹果正式宣布未来的Mac也会使用Apple Silicon。作为演示提供给开发者用的测试机里面装载的就是只比A12X多一个GPU核心的A12Z。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/apple-chip/ADTK.png" style="margin: 0 auto; width: 50%;">
</div>

从WWDC上的演示效果来看，A12Z运行专业软件完全没有问题。视频剪辑、3D渲染、游戏等，A12Z都有很好的表现。而苹果宣布年底推出的搭载自家芯片的Mac应该使用的是A14X，肯定会比A12Z更好。这就更加让人期待未来的Mac的性能表现了。

但是从目前来看，换成自研芯片的Mac还是有利有弊的。

从好的地方来说，自家所有产品都使用自研芯片，统一度提高。可以摆脱Intel的芯片意味着成本的降低以及芯片更新可以与产品更新同步。与此同时，Mac可以直接运行iOS和iPadOS上的软件，增加了不少应用。与此同时，芯片的集成度进一步提高，过去的T系列芯片（主要用于加密）现在完全可以内置于A系列芯片中。

当然我们也不能忽略坏的方面。不能通过Bootcamp运行Windows首当其冲，这可能会成为阻挡消费者购买Mac的一大因素。另外就是现有的应用需要经过一段很长时间才能完全转换成ARM版的。一旦苹果放弃对X86的支持可能会出现部分应用不能运行了。

回过来看这10年苹果自研芯片的历程，中间出现过很多让人眼前一亮的产品。因为篇幅问题没有提及苹果的其他系列芯片。苹果最早可能只是想尝试用在手机上的自研芯片，但是随着其性能越来越强大，苹果的野心也越来越大，最终完全掌控了自家产品的芯片。
