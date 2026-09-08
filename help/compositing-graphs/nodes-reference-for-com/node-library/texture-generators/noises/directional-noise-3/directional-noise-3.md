---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-3.html"
breadcrumb-title: ''
description: 使用定向噪声3节点生成包含三个八度音阶的定向噪声模式，以创建方向纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 定向噪声3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# 定向噪声3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![定向噪声3 — 图标](../../../../../../assets/directional_noise_3.png "定向噪声3 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>定向噪声</b>噪声的变体。

另请参阅：[定向噪声1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md)，[定向噪声2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md)，[定向噪声4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>无序anisotropy angle</b>Float | 当“无序位移”参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>角度</b>Float | 用来设置噪声方向的角度，以匝数为单位，从右上方开始。 |
| <b>角度随机</b>Float | 应用于<b>角度</b>值的随机变化的最大值（轮次数）。 |
| <b>拼贴偏移</b>Float2 | 控制用于渲染噪声的无限平面部分的位置。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴为方形，并将噪声生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![定向噪声3 — 示例1](../../../../../../assets/directional_noise_3_1.png "定向噪声3 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![定向噪声3 — 示例2](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso0.gif "定向噪声3 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![定向噪声3 — 示例3](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso1.gif "定向噪声3 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![定向噪声3 — 示例4](../../../../../../assets/noise_directional_noise_3_v2_speed0.3_aniso0.6.gif "定向噪声3 — 示例4"){zoomable="yes"}

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
