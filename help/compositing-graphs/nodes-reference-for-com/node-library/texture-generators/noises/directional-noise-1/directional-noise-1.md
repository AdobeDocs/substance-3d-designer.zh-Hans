---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-1.html"
breadcrumb-title: ''
description: 使用“定向噪声1”节点生成定向噪声图案，用于创建各向异性纹理变化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 定向噪声1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 1%

---


# 定向噪声1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![定向噪声1 — 图标](../../../../../../assets/directional_noise_1.png "定向噪声1 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>定向噪声</b>噪声的变化。

另请参阅：[定向噪声2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md)，[定向噪声3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md)，[定向噪声4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>无序各向异性角度</b>浮动 | 当“无序位移”参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>角度</b>浮动 | 用来设置杂色方向的角度，以匝数为单位，并且从水平右边开始。 |
| <b>角度随机</b>浮点 | 应用于<b>角度</b>值的随机变化的最大值（轮次数）。 |
| <b>拼贴偏移</b>浮动2 | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![定向噪声1 — 示例1](../../../../../../assets/directional_noise_1_1.png "定向噪声1 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![定向噪声1 — 示例2](../../../../../../assets/noise_directional_noise_1_v2_speed0.6_aniso0.gif "定向噪声1 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![定向噪声1 — 示例3](../../../../../../assets/noise_directional_noise_1_v2_speed0.6_aniso1.gif "定向噪声1 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![定向噪声1 — 示例4](../../../../../../assets/noise_directional_noise_1_v2_speed0.3_aniso0.6.gif "定向噪声1 — 示例4"){zoomable="yes"}

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
