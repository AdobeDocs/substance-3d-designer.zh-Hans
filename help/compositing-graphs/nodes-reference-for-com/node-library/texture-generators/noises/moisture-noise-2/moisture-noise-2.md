---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise-2.html"
breadcrumb-title: ''
description: 使用水分噪声2节点生成有机水分图案，用于逼真的表面纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水分噪声2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---


# 水分噪声2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![湿度噪声2 — 图标](../../../../../../assets/moisture_noise_2.png "湿度噪声2 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

丰富和海绵的<b>水分</b>噪声的变化。

硬度和大小不一的磁盘，从基础灰色开始，分散在下面的颜色中，增加或减去下面的颜色。

另请参阅： [水分噪声1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

</td>
</tr>
</table>

## 输出

|  |  |
| --- | --- |
| <b>输出</b> *灰度* | 生成的灰度位图噪声。 |

## 参数

|  |  |
| --- | --- |
| <b>缩放</b>整数 | 用于生成噪声拼贴的网格细分。    值越高，绘制的拼贴越多，噪声越密。 |
| <b>无序</b>Float | 置换噪声的组成部分。    这可用于为噪声制作动画。 |
| <b>无序速度</b>Float | 调整<b>无序</b>参数应用的位移的距离。    在为噪声制作动画时，这可用于控制位移的速度。 |
| <b>无序各向异性</b>Float | 控制<b>无序</b>参数应用的位移的方向跨度，值越高，方向越窄，定义越明确。    方向由<b>无序anisotropy angle</b>参数控制。 |
| <b>无序anisotropy angle</b>Float | 当<b>无序位移</b>参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>图案大小</b>Float2 | 散布图案大小的乘数。其中1.0是其原始散布大小。 |
| <b>图案角度</b>Float | 用于设置散布图案方向的角度，以匝数为单位，从水平右边开始。 |
| <b>图案角度随机</b>Float | 应用于<b>图案角度</b>值的随机变化的最大值（轮次数）。 |
| <b>全局不透明度</b>Float | 噪声所有成分的不透明度，其中0.0表示基色纯灰色，1.0表示成分所应用的完全加法或减法结果。 |
| <b>拼贴偏移</b>Float2 | 控制用于渲染噪声的无限平面部分的位置。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴为方形，并将噪声生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![湿度噪声2 — 示例1](../../../../../../assets/moisture_noise_2_1.png "湿度噪声2 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![湿度噪声2 — 示例2](../../../../../../assets/noise_moisture_noise_2_speed0.6_aniso0.gif "湿度噪声2 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![湿度噪声2 — 示例3](../../../../../../assets/noise_moisture_noise_2_speed0.6_aniso1.gif "湿度噪声2 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![湿度噪声2 — 示例4](../../../../../../assets/noise_moisture_noise_2_speed0.3_aniso0.6.gif "湿度噪声2 — 示例4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
