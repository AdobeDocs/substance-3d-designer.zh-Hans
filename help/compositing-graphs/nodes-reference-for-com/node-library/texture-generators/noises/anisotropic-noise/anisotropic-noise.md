---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: 使用“Anoistic Noise”（各向异性噪声）节点生成定向噪声图案，用于创建各向异性纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 各向异性噪声
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# 各向异性噪声

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向异性噪声 — 图标](../../../../../../assets/anisotropic_noise_v2.png "各向异性噪声 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一个水平或垂直栈叠的任意颜色的条纹，这些条纹会相互淡化。

条带数量可调整，其转变的Smoothness也可调整。

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
| <b>X数量</b> <i>整数</i> | X轴上的条带数量。 |
| <b>Y数量</b> <i>整数</i> | Y轴上的条带数量。 |
| <b>Y数量（按分辨率）</b> <i>布尔值</i> | 如果为True，则Y轴上的条带数量将等于该轴上的图像大小。 |
| <b>旋转</b> <i>布尔值</i> | 将噪声旋转90度。 |
| <b>Smoothness</b> <i>浮动</i> | 条带之间的衰落量，其中0不衰落，而1在其整个长度上衰落。 |
| <b>Smoothness插值</b> <i>浮动</i> | 两种插值方法的加权均适用于渐隐条带，其中0是线性的，1是高斯的。 |
| <b>无序</b> <i>浮动</i> | 替换噪点的成分。   这可用于为噪声设置动画。 |
| <b>无序速度</b> <i>浮动</i> | 调整<b>无序</b>参数应用的位移的距离。   这可用于在制作噪声动画时控制位移的速度。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![各向异性噪声 — 示例1](../../../../../../assets/anisotropic_noise_v2_1.png "各向异性噪声 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![各向异性噪声 — 示例2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "各向异性噪声 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>
