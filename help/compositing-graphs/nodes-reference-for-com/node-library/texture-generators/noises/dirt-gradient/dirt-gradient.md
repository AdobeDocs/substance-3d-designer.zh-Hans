---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/dirt-gradient.html"
breadcrumb-title: ''
description: 使用“Dirt渐变”节点生成基于渐变的Dirt模式，以创建方向风化和累积效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Dirt gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt渐变
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1241ebb4d1e67c9ed9d86285a6397ddc335e0f37
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# Dirt渐变

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Dirt渐变 — 图标](dirt-gradient.resources/dirt_gradient.png "Dirt渐变 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

具有定向衰减渐变的粒状<b>Dirt</b>噪声的变体。

另请参阅：[Dirt1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-1/dirt-1.md)、[Dirt2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-2/dirt-2.md)、[Dirt3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-3/dirt-3.md)、[Dirt4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-4/dirt-4.md)、[Dirt5](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-5/dirt-5.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 生成的灰度位图噪声。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>无序</b> <i>Float</i> | 置换噪声的组成部分。    这可用于为噪声制作动画。 |
| <b>无序速度</b> <i>Float</i> | 调整<b>无序</b>参数应用的位移的距离。    在为噪声制作动画时，这可用于控制位移的速度。 |
| <b>无序各向异性</b> <i>Float</i> | 控制<b>无序</b>参数应用的位移的方向跨度，值越高，方向越窄，定义越明确。    方向由<b>无序anisotropy angle</b>参数控制。 |
| <b>无序anisotropy angle</b> <i>Float</i> | 当<b>无序位移</b>参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴为方形，并将噪声生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt渐变 — 示例1](dirt-gradient.resources/dirt_gradient_1.png "Dirt渐变 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt渐变 — 示例2](dirt-gradient.resources/noise_dirt_gradient_v2_speed0.6_aniso0.gif "Dirt渐变 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt渐变 — 示例3](dirt-gradient.resources/noise_dirt_gradient_v2_speed0.6_aniso1.gif "Dirt渐变 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt渐变 — 示例4](dirt-gradient.resources/noise_dirt_gradient_v2_speed0.3_aniso0.6.gif "Dirt渐变 — 示例4"){zoomable="yes"}

</td>
</tr>
</table>
