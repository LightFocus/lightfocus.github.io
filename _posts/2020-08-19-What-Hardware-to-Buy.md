---
layout: post
title:  "自己装机硬件怎么选？"
author: lightfocus
categories: [ Hardware ]
tags: [ Gear ]
image: "https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/cover/hardware.jpg"
---
装一台电脑可能对于很多人来说不是一件容易事，但其实它真的很简单。

本文先从最基本的硬件选购开始，介绍各个硬件、教你如何判断一个硬件的性能，以及选购的时候需要注意的事项。
<h1>一、CPU</h1>
CPU作为电脑的大脑，肯定是要好好选。能选择的有两家：Intel、AMD，俗称红蓝厂。

<del>自古红蓝出CP</del>

Intel和AMD可以说是老冤家了，从上个世纪就开始CPU市场的竞争，什么第一个64位处理器啊，第一个突破1GHz主频的CPU啊。在很长一段时间里，Intel都是吊打AMD的，只有便宜的电脑才会装AMD的CPU。而今天的故事还要从2014年说起。

2014年10月27日，Intel发布了Broadwell处理器，用上了14nm的制程。在处理器制程上的更新，Intel一直都是采用Tick-Tock策略，即一代提升制程，下一代优化，再下一代再提升制程，以此类推。例如：Penryn(45nm)-&gt;Nehalem(45nm)-&gt;Westmere(32nm)-&gt;Sandy Bridge(32nm)。从22nm的Haswell开始，Intel变成了Tick-Tock-Refresh的策略，也就是说一个制程用三年。但是让人没想到的是，2014年发布的14nm处理器，竟然让Intel用了Broadwell、Skylake、Kaby Lake、Kaby Lake R、Coffee Lake、Amber Lake、Comet Lake整整六代（我没有数错）处理器上。Intel自此也被人称为“牙膏厂”，因为新制程一直挤不出来。

AMD这边则是通过2017年发布的基于Zen架构的Ryzen开始翻身，从以前的性价比首选，到高端电脑也可以选。尤其是2019年发布的3代Ryzen，基于Zen2机构，赶在Intel之前实现了7nm制程。

因此，在Intel挤出桌面10nm牙膏之前，装机我<strong>个人推荐</strong>AMD的处理器。不过Intel的处理器在游戏方面可能更胜一筹，但是两者差距只有在100+fps时才体现的出来（即需要顶级显卡）。装黑苹果建议选择Intel。

选购CPU主要关注以下几个参数：

核心数：顾名思义，核心的数量，越多越快

线程数：一般等于核心数，具有超线程功能的CPU则等于核心数的两倍。

基准频率：一般运行的频率，越高速度越快

Boost频率：可以波动频率的最高值（非手动超频情况下）

TDP：热设计功耗，和散热及电源的选择密切相关

下面列出Zen2架构的CPU（不包含HEDT平台）
<div class="table-container">
<table class="table">
<thead class="table-header">
<tr>
<th class="header-item">型号</th>
<th class="header-item">售价MSRP($)</th>
<th class="header-item">核心数/线程数</th>
<th class="header-item">基准频率(GHz)</th>
<th class="header-item">Boost频率(GHz)</th>
<th class="header-item">TDP(W)</th>
</tr>
</thead>
<tbody>
<tr class="tabel-row">
<td class="table-data" colspan="6">入门级</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3100</td>
<td class="table-data">99</td>
<td class="table-data">4/8</td>
<td class="table-data">3.6</td>
<td class="table-data">3.9</td>
<td class="table-data">65</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3300X</td>
<td class="table-data">120</td>
<td class="table-data">4/8</td>
<td class="table-data">3.8</td>
<td class="table-data">4.3</td>
<td class="table-data">65</td>
</tr>
<tr class="tabel-row">
<td class="table-data" colspan="6">主流级</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3500X</td>
<td class="table-data">￥1099</td>
<td class="table-data">6/6</td>
<td class="table-data">3.6</td>
<td class="table-data">4.1</td>
<td class="table-data">65</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3600</td>
<td class="table-data">199</td>
<td class="table-data">6/12</td>
<td class="table-data">3.6</td>
<td class="table-data">4.2</td>
<td class="table-data">65</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3600X</td>
<td class="table-data">249</td>
<td class="table-data">6/12</td>
<td class="table-data">3.8</td>
<td class="table-data">4.4</td>
<td class="table-data">95</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3600XT</td>
<td class="table-data">249</td>
<td class="table-data">6/12</td>
<td class="table-data">3.8</td>
<td class="table-data">4.5</td>
<td class="table-data">95</td>
</tr>
<tr class="tabel-row">
<td class="table-data" colspan="6">性能级</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3700X</td>
<td class="table-data">329</td>
<td class="table-data">8/16</td>
<td class="table-data">3.6</td>
<td class="table-data">4.4</td>
<td class="table-data">65</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3800X</td>
<td class="table-data">399</td>
<td class="table-data">8/16</td>
<td class="table-data">3.9</td>
<td class="table-data">4.5</td>
<td class="table-data">105</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3800XT</td>
<td class="table-data">399</td>
<td class="table-data">8/16</td>
<td class="table-data">3.9</td>
<td class="table-data">4.7</td>
<td class="table-data">105</td>
</tr>
<tr class="tabel-row">
<td class="table-data" colspan="6">发烧级</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3900X</td>
<td class="table-data">499</td>
<td class="table-data">12/24</td>
<td class="table-data">3.8</td>
<td class="table-data">4.6</td>
<td class="table-data">105</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3900XT</td>
<td class="table-data">499</td>
<td class="table-data">12/24</td>
<td class="table-data">3.8</td>
<td class="table-data">4.7</td>
<td class="table-data">105</td>
</tr>
<tr class="tabel-row">
<td class="table-data">3950X</td>
<td class="table-data">749</td>
<td class="table-data">16/32</td>
<td class="table-data">3.5</td>
<td class="table-data">4.7</td>
<td class="table-data">105</td>
</tr>
</tbody>
</table>
</div>
建议预算4000以内装机的用户选择3300X，6000左右的选择3600，10000左右选择3700X。
<h1>二、主板</h1>
选好CPU的同时也就确定了主板可选的范围。

以3代Ryzen为例，其接口为AM4，通过查询我们可以得知支持该接口的芯片组有：
<div class="table-container">
<table class="table">
<thead class="table-header">
<tr>
<th class="header-item">型号</th>
<th class="header-item">PCI Express (PCIe)</th>
<th class="header-item">市场定位</th>
<th class="header-item" colspan="4">CPU 支持</th>
</tr>
</thead>
<tbody>
<tr class="table-row">
<td class="table-data"></td>
<td class="table-data">芯片组PCIe 通道数</td>
<td class="table-data"></td>
<td class="table-data">Zen</td>
<td class="table-data">Zen+</td>
<td class="table-data">Zen 2</td>
<td class="table-data">Zen 3</td>
</tr>
<tr class="table-row">
<td class="table-data">X570</td>
<td class="table-data">PCIe 4.0 ×16</td>
<td class="table-data" rowspan="3">性能级</td>
<td class="table-data">否</td>
<td class="table-data" rowspan="3">是</td>
<td class="table-data" rowspan="2">是</td>
<td class="table-data">是</td>
</tr>
<tr class="table-row">
<td class="table-data">X470</td>
<td class="table-data" rowspan="2">PCIe 2.0 ×8</td>
<td class="table-data" rowspan="2">是</td>
<td class="table-data" rowspan="2">否</td>
</tr>
<tr class="table-row">
<td class="table-data">X370</td>
<td class="table-data">需要BIOS 升级</td>
</tr>
<tr>
<td class="table-data">B550</td>
<td class="table-data">PCIe 3.0 ×6</td>
<td class="table-data" rowspan="3">主流级</td>
<td class="table-data">否</td>
<td class="table-data">否</td>
<td class="table-data" rowspan="2">是</td>
<td class="table-data">是</td>
</tr>
<tr class="table-row">
<td class="table-data">B450</td>
<td class="table-data" rowspan="2">PCIe 2.0 ×6</td>
<td class="table-data" rowspan="3">是</td>
<td class="table-data" rowspan="3">是</td>
<td class="table-data" rowspan="3">否</td>
</tr>
<tr class="table-row">
<td class="table-data">B350</td>
<td class="table-data" rowspan="2">需要BIOS 升级</td>
</tr>
<tr class="table-row">
<td class="table-data">A320</td>
<td class="table-data">PCIe 2.0 ×4</td>
<td class="table-data">入门级</td>
</tr>
</tbody>
</table>
</div>
不同芯片组的功能、可扩展性、对未来CPU的支持都不一样。对于可能要升级Zen3的用户值得考虑X570和B550，否则一般用户X470和B450也足够了，因为AM4接口只用到Zen3为止。后面更新的CPU又是新的接口要买新的主板。

除了芯片组以外，主板还有一个很关键的参数就是板型。板型决定了主板的大小以及接口数量。

常见的主板板型有：ATX（305mm\*244mm）、microATX（244mm\*244mm）、Mini-ITX（170mm\*170mm）。

想要装一台体积小巧的电脑最佳选择肯定是Mini-ITX的主板，不过Mini-ITX主板一般价格稍贵而且通常只有个一个PCIe接口，所以Crossfire或者SLI就肯定不行了。

一般来说建议CPU和主板一起买，价格会比较优惠，而且对于部分老主板可以让卖家帮你刷好新的BIOS以保证CPU能正常工作。
<h1>三、显卡</h1>
独立显卡并不是人人都需要。对于不需要太强劲显卡性能同时想省钱的用户可以考虑Intel带集成显卡的CPU或者AMD的APU系列，即把显卡集成在CPU里面。

目前3代Ryzen能买到的APU好像只有Ryzen 5 3400G。购买APU需要注意两个问题：1、APU的性能与内存息息相关，买APU的用户一定不能在内存上省钱 2、APU对黑苹果的支持有问题。

那么剩下的用户自然就是需要高性能独立显卡的了。类似的，独立显卡市场也是两大阵营，AMD和NVIDIA，俗称红绿厂，也是老冤家，这里就不展开叙述了。

AMD的显卡没有像它的CPU那么猛，吊打竞争对手。在高端显卡这块，还是NVIDIA一家独大。

AMD这边你能买到最好的显卡就是RX 5700 XT，略逊于NVIDIA的RTX 2070 Super。但是NVIDIA往上还有2080、2080super、2080ti呢。（这里不讨论Titan以及Vega II Duo）

新显卡的独家功能上，NVIDIA更吸引人。光线追踪、DLSS以及CUDA，AMD这边只有RIS比较有看头。注意：GTX 16xx显卡不支持光线追踪及DLSS。

关于上面功能的介绍请移步<a href="https://lightfocus/github.io/blog/intro-ray-tracing">这里</a>。

下面给出热门在售显卡的参考性能，可以根据实时价格对比购买。

GTX 1650 参考性能：

PUBG(1080p Ultra): 60 fps

Gears 5(1080p High): 60 fps

Assassin's Creed Odyssey(1080p Very High): 47 fps

Metro Exodus(1080p High): 46 fps

Red Dead Redemption 2(1080p Medium-High): 37 fps

Battlefield 5(1080p Ultra): 54 fps

Control(1080p High): 32 fps
<div class="table-container">
<table class="table">
<thead class="table-header">
<tr>
<th class="header-item">型号</th>
<th class="header-item">相对性能（1080p）</th>
</tr>
</thead>
<tbody>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">GTX 1650</span></td>
<td class="table-data"><span style="color:#00ff00;">100%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#ff0000;">RX 570</span></td>
<td class="table-data"><span style="color:#ff0000;">114%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#ff0000;">RX 5500</span></td>
<td class="table-data"><span style="color:#ff0000;">129%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#ff0000;">RX 580</span></td>
<td class="table-data"><span style="color:#ff0000;">131%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#ff0000;">RX 5500 XT</span></td>
<td class="table-data"><span style="color:#ff0000;">132%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">GTX 1650 Super</span></td>
<td class="table-data"><span style="color:#00ff00;">135%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">GTX 1660</span></td>
<td class="table-data"><span style="color:#00ff00;">150%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">GTX 1660 Super</span></td>
<td class="table-data"><span style="color:#00ff00;">168%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">GTX 1660 Ti</span></td>
<td class="table-data"><span style="color:#00ff00;">172%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2060</span></td>
<td class="table-data"><span style="color:#00ff00;">202%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#ff0000;">RX 5700</span></td>
<td class="table-data"><span style="color:#ff0000;">210%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2060 Super</span></td>
<td class="table-data"><span style="color:#00ff00;">227%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2070</span></td>
<td class="table-data"><span style="color:#00ff00;">235%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#ff0000;">RX 5700 XT</span></td>
<td class="table-data"><span style="color:#ff0000;">241%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2070 Super</span></td>
<td class="table-data"><span style="color:#00ff00;">260%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2080</span></td>
<td class="table-data"><span style="color:#00ff00;">277%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2080 Super</span></td>
<td class="table-data"><span style="color:#00ff00;">294%</span></td>
</tr>
<tr class="table-row">
<td class="table-data"><span style="color:#00ff00;">RTX 2080 Ti</span></td>
<td class="table-data"><span style="color:#00ff00;">324%</span></td>
</tr>
</tbody>
</table>
</div>
在你选好了显卡以后，你会发现同一个型号，不同厂家的价格差距很大。同一型号内便宜的称为乞丐版，贵的称为顶级非公版。乞丐版会在供电、RGB以及散热上缩水，同时显卡的频率不如顶级非公版的高。在预算不足又想要高性能的前提下可以买丐版。例如2070 super丐版3300，顶级非公4000出头，但是2080super的丐版只要4300。这种情况下选择2080super丐版能获得更好的性能。
<h1>四、内存</h1>
不考虑上古DDR3的话，买内存就三个重要指标：容量、频率、时序。

容量建议起步16G，上限看你插槽数量和钱包了。

频率对高帧率游戏以及APU影响明显，建议3200MHz往上。

对于Zen2架构的用户特别注意，3733MHz是内存延迟的Sweet Spot：

<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/hardware/ryzen3memory.jpg" alt="Ryzen3Memory" width="100%">

时序介绍起来比较复杂，对新手来说，记得第一位数字越小越好。因此3600MHz C16的内存比3600MHz C18的内存好。

<del>RGB内存条性能翻倍</del>
<h1>五、硬盘</h1>
大体上分为三类：机械硬盘，SATA固态硬盘，NVMe固态硬盘
<h2>机械硬盘：使用SATA接口，内部是磁盘的传统硬盘，速度约100mb/s。</h2>
优点：容量大，数据可以恢复

缺点：需要额外供电、体积大且重、抗震性差
<h2>SATA固态硬盘：使用SATA接口，内部是闪存的固态硬盘，速度约500mb/s。</h2>
优点：不需要占用主板的m.2接口

缺点：需要额外供电、价格稍高
<h2>NVMe固态硬盘：使用m.2接口，内部是闪存的固态硬盘，速度约1gb/s-3gb/s。</h2>
优点：速度很快

缺点：温度高、主板m.2口有限、价格较高
<h1>六、电源</h1>
如果是ITX小机箱，那大概率只能买ITX电源，贵且选择少，推荐海盗船SF系列。另外小机箱可能不好走线，还需要买电源定制线。

功率看你的硬件，例如CPU TDP 100W，显卡 TDP 200W 那最好买550W以上的电源。预算够的话功率尽可能买大一点，这个功率不是指电脑耗电功率，而是电源最大能输出的功率，大一点风险低而且后面升级硬件方便。当然太便宜又号称高功率的电源你自己看着办吧。

电源转化效率有80PLUS的等级，即什么铜牌、银牌、金牌电源。看预算，没必要强上。
<h1>七、机箱</h1>
可以没有，散热性最好；或者奢侈一点，拿个鞋盒（逃）。

看着你喜欢的买就行，注意支持的板型。一些ITX小机箱会对CPU散热器限高、显卡限长、限高。
<h1>八、散热器</h1>
买盒装CPU一般会送一个风扇，不建议使用，温度压不住。有条件上水冷，没条件也买一个好一点的风冷。

注意机箱限高。

猫扇是信仰，贵但是不一定好。
