---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise-2.html"
breadcrumb-title: ''
description: 使用“水分杂色2”节点生成有机水分图案，以获得逼真的表面纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水汽杂色2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---


# 水汽杂色2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![水汽噪声2 — 图标](../../../../../../assets/moisture_noise_2.png "水汽噪声2 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

丰富和海绵的<b>水气</b>噪声的变化。

硬度和大小不等的圆盘，从基灰色开始，分散在下面的颜色中，并与之相加或相减。

另请参阅： [水汽杂色1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 生成的杂色作为灰度位图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>缩放</b> <i>整数</i> | 使用网格细分生成噪声拼贴。    值越高，所绘制的拼贴就越多，噪音也越浓。 |
| <b>无序</b> <i>浮动</i> | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b> <i>浮动</i> | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |
| <b>无序各向异性</b> <i>浮动</i> | 控制<b>无序</b>参数应用的位移的方向跨度，值越高，方向越窄，定义越明确。    方向由<b>无序各向异性角</b>参数控制。 |
| <b>无序anisotropy angle</b> <i>浮动</i> | 当<b>无序位移</b>参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>图案大小</b> <i>浮点2</i> | 散布图案大小的乘数。其中1.0是其原始散布大小。 |
| <b>图案角度</b> <i>浮动</i> | 用于设置散布图案方向的角度，以匝数为单位，从水平右边开始。 |
| <b>图案角度随机</b> <i>浮动</i> | 应用于<b>图案角度</b>值的随机变化的最大值（轮次数）。 |
| <b>全局不透明度</b> <i>浮动</i> | 噪声的所有成分的不透明度，其中0.0表示基本平坦灰色，1.0表示成分应用的完全加法或减法结果。 |
| <b>拼贴偏移</b> <i>浮点2</i> | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![水汽噪声2 — 示例1](../../../../../../assets/moisture_noise_2_1.png "水汽噪声2 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![水汽噪声2 — 示例2](../../../../../../assets/noise_moisture_noise_2_speed0.6_aniso0.gif "水汽噪声2 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![水分噪声2 — 示例3](../../../../../../assets/noise_moisture_noise_2_speed0.6_aniso1.gif "水分噪声2 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![水汽噪声2 — 示例4](../../../../../../assets/noise_moisture_noise_2_speed0.3_aniso0.6.gif "水汽噪声2 — 示例4"){zoomable="yes"}

</td>
</tr>
</table>
