---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise.html"
breadcrumb-title: ''
description: 使用“水分噪声”节点生成水分和凝结图案，以创建湿表面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水汽杂色1
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# 水汽杂色1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![水汽噪声1 — 图标](../../../../../../assets/moisture_noise_1.png "水汽噪声1 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

丰富和海绵的<b>水气</b>噪声的变化。

硬度和大小不等的圆盘，从基灰色开始，分散在下面的颜色中，并与之相加或相减。

另请参阅： [水汽杂色2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise-2/moisture-noise-2.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 输出

</td>
<td style="border: 0;" valign="top">

### 参数

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 输出

|  |  |
| --- | --- |
| <b>输出</b> *灰度* | 生成的杂色作为灰度位图。 |

## 参数

|  |  |
| --- | --- |
| <b>缩放</b>整数 | 使用网格细分生成噪声拼贴。    值越高，所绘制的拼贴就越多，噪音也越浓。 |
| <b>无序</b>浮动 | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b>浮动 | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |
| <b>无序各向异性</b>浮动 | 控制<b>无序</b>参数应用的位移的方向跨度，值越高，方向越窄，定义越明确。    方向由<b>无序各向异性角</b>参数控制。 |
| <b>无序各向异性角度</b>浮动 | 当<b>无序位移</b>参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>图案大小</b>浮点2 | 散布图案大小的乘数。其中1.0是其原始散布大小。 |
| <b>图案角度</b>浮动 | 用于设置散布图案方向的角度，以匝数为单位，从水平右边开始。 |
| <b>图案角度随机</b>浮动 | 应用于<b>图案角度</b>值的随机变化的最大值（轮次数）。 |
| <b>全局不透明度</b>浮点 | 噪声的所有成分的不透明度，其中0.0表示基本平坦灰色，1.0表示成分应用的完全加法或减法结果。 |
| <b>拼贴偏移</b>浮动2 | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![水汽噪声1 — 示例1](../../../../../../assets/moisture_noise_1_1.png "水汽噪声1 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![水汽噪声1 — 示例2](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso0.gif "水汽噪声1 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![水汽噪声1 — 示例3](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso1.gif "水汽噪声1 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![水汽噪声1 — 示例4](../../../../../../assets/noise_moisture_noise_1_v2_speed0.3_aniso0.6.gif "水汽噪声1 — 示例4"){zoomable="yes"}

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
