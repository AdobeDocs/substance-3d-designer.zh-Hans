---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ''
description: 使用Perlin噪声节点生成平滑、自然的噪声图案，用于创建有机纹理和变体。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Perlin噪声
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5a6c28b9acabf15714a1fd8bb4e7593192555fa2
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Perlin噪声

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Perlin噪声 — 图标](perlin-noise.resources/perlin_noise.png "Perlin噪声 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成Perlin噪声，一种广泛使用的灰度值平滑分布。

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
| <b>缩放</b> <i>整数</i> | 用于生成噪声拼贴的网格细分。    值越高，绘制的拼贴越多，噪声越密。 |
| <b>无序</b> <i>Float</i> | 置换噪声的组成部分。    这可用于为噪声制作动画。 |
| <b>无序速度</b> <i>Float</i> | 调整<b>无序</b>参数应用的位移的距离。    在为噪声制作动画时，这可用于控制位移的速度。 |
| <b>拼贴偏移</b> <i>Float2</i> | 控制用于渲染噪声的无限平面部分的位置。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴为方形，并将噪声生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Perlin噪声 — 示例1](perlin-noise.resources/perlin_noise_1.png "Perlin噪声 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Perlin噪声 — 示例2](perlin-noise.resources/noise_perlin_noise_v2_speed0.6_aniso0.gif "Perlin噪声 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>
