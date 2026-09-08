---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: 使用“白噪声”节点生成白噪声图案，用于创建纹理变化和随机效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 白杂色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# 白杂色

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![白噪声 — 图标](../../../../../../assets/white_noise_v2.png "白噪声 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用针对不同直方图形状的三种方法之一生成白噪声：均匀、高斯和三角形。

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
| <b>噪声分布</b>整数 | 将食材分布到目标直方图形状的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>一致：</i>平面直方图。</li> <li data-preserve-html="true"><i>高斯：</i>表示正态分布的直方图，类似于钟形曲线。</li> <li data-preserve-html="true"><i>三角形：</i>三角形直方图。</li> </ul> |
| <b>无序</b>浮动 | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b>浮动 | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![白噪声 — 示例1](../../../../../../assets/white_noise_v2_1.png "白噪声 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![白噪声 — 示例2](../../../../../../assets/white_noise_v2_speed0.6_aniso0.gif "白噪声 — 示例2"){zoomable="yes"}

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
