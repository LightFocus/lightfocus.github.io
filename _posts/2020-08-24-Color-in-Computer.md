---
layout: post
title:  "计算机色彩相关知识简介"
author: lightfocus
categories: [ Graphics ]
tags: [ Technology ]
image: "https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/cover/Hsl-Hsv_models.png"
rating: 5
---
<h2>色彩表示方法</h2>
人对于色彩的描述是很不准确的。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/Red.png" style="margin: 0 auto; width: 50%;">
</div>

以上面这个图片为例，人们都会将它们描述为红色，但是在计算机的表示里面，它们是完全不同的四个颜色。

计算机里面有很多种表示色彩的方法，一般人最耳熟能详的就是RGB色彩模型。RGB是一种加色模型，即红蓝绿三种原色光相加来获得其他颜色的光。选择红蓝绿三种颜色是因为这三种颜色能分别对人的三种锥形细胞产生刺激，虽然这些细胞并不是对这三种颜色的光最敏感。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/RGB_color_solid_cube.png" style="margin: 0 auto; width: 50%;">
</div>
RGB模型可以写成很多形式。以白色为例，可以写成(1.0,1.0,1.0)、(255,255,255)、(100%,100%,100%)等。但是我们很快就可以看出，RGB模型和显示设备的色彩空间有很大的关系，不同的设备显示的RGB(255,255,255)是不同的。

RGB色彩模型理论上可以显示256\*256\*256种颜色，即16777216种颜色，也就是我们常说的1600万色。但是在网页显示中，为了防止这1600多万种色彩产生混淆，我们引入了网页安全颜色。

RGB色彩模型虽然很常用，但是它也有一定的缺点，最明显的一点就是人不能直观的理解。例如黄色的RGB值就不能第一时间想到，除非你对三色光相加很熟悉。因此，我们引入了人看上去更为直观的HSL/HSV色彩模型。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/Hsl-Hsv_models.png" style="margin: 0 auto; width: 50%;">
</div>

虽然乍一看HSV/HSL有些复杂，但是它更直观。其中H（Hue）代表色相，是一个圆形，通过角度来表示颜色；S（Saturation）代表饱和度，圆柱体中间饱和度最低，边缘饱和度最高；V（Value）/L（Lightness）代表亮度，圆柱体越往上越亮。在这种色彩表示模型下，一切就变得很直观。例如（60°,1.0,1.0）就可以理解为最亮最饱和的黄色。HSL/HSV模型被更多的用于设计方面，例如摄影的调色就可以采用这种模型，因为调整起来更好理解。

一般来说HSV/HSL色彩模型只是用于表示，而计算机最后显示的都是采用RGB色彩模型。因此不可避免的就是HSV/HSL与RGB之间的转换。每一种转换都有对应的数学公式，这里不展开讨论。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/CMYK.png" style="margin: 0 auto; width: 50%;">
</div>

除此之外，还有一种色彩模型也很常用，那就是CMYK模型。这种模型主要用于印刷行业，因为打印机一般只有黑色（K:Black）和三色墨盒（C:Cyan, M:Magenta, Y:Yellow）。类似的，按不同比例混合这些颜色也能得到不同的颜色。

在介绍完了常见的色彩模型后，我们需要提一下色彩空间。很多人对“色域”（Gamut）这个词比较熟悉，色彩空间其实就是由色域和色彩模型共同定义的。很多人会把色域和色彩空间混为一谈，因为他们默认色彩模型是RGB模型。常见的色彩空间有sRGB、P3、Adobe RGB等。

一种最常见的对比色彩空间的方法就是将色彩空间在 CIE1931 xy色彩图上表现出来。CIE1931色彩空间是最早采用数学定义的色彩空间，是一个三维空间。但是为了方便表示，人们习惯将其投影到平面上，采用xy的形式表示，形状类似于一个舌头。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/CIE1931xy.png" style="margin: 0 auto; width: 50%;">
</div>

上图的E点表示均等能量点，又称为白点。当我们需要表示一种色彩空间的时候，将其边界在CIE1931中绘制出来就可以了。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/Colorspace.png" style="margin: 0 auto; width: 50%;">
</div>

最后要提一点的就是色度抽样，其主要用于对图片或者视频进行压缩。其原理是利用人眼对于色彩的敏感度远低于对亮度的敏感度，因此可以压缩图片中的色彩信息而保留亮度信息，以达到基本不损失视觉效果的前提下压缩体积。

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/Colorcomp.jpg" style="margin: 0 auto; width: 80%;">
</div>

以上图为例，上面一排图片看上去的视觉效果差不多，而下面一排可以明显看出色彩信息的分辨率不一样。

计算机色度抽样通常使用一个三分比值表示：J:a:b，其中J表示区域的长为J个像素，高为2个像素，J一般为4；a表示在J个像素的第一行的色度抽样数，b表示在J个像素的第二行的额外色度抽样数。有些时候会有第四个数Alpha，表示水平因素，没有时可忽略，存在时和J相同。

下面列出几种比较常见的色度抽样：

<div style="text-align: center; width: 100%;">
<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/computer-color/Chroma_subsampling.png" style="margin: 0 auto; width: 80%;">
</div>

绝大部分经过压缩的图片和视频都会采用色度抽样的方法，因此我们看到的颜色不一定是原始数据所反映的颜色。

以上就是本文要介绍的计算机色彩的基本知识。