---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: 使用“波形1”节点生成波形图案，用于创建有机纹理和过程变化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 波形1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# 波形1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![波形1 — 图标](../../../../../../assets/waveform_01_v2.png "波形1 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种水平排列用户选择的图案，栈叠成类似于波形的形状。

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
| <b>示例</b>整数 | 沿X轴放置以绘制波形的图案数量，值越低，外观越分步。 |
| <b>函数</b>整数 | 用于绘制波形的功能。   此选项可控制每个样本处图案的垂直大小：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>值杂色：</i>值的随机分布</li> <li data-preserve-html="true"><i>余弦：</i>值遵循余弦函数的过程</li> <li data-preserve-html="true"><i>自定义函数：</i>使用用户编写的函数来驱动值</li> </ul> |
| <b>自定义函数</b>浮点&#x200B;*当“Function”设置为“Custom function”时可用* | 计算每个样本处图案的垂直大小。   可用变量：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> （<i>浮动</i>）图案在X轴上的位置。 这可用于选择图案。</li> </ul> |
| <b>粗糙度</b>浮点 | 在清晰平滑的波形与更粗糙且分布更均匀的波形之间插补。    这可以看作是干净信号与白噪声。 |
| <b>缩放</b>整数 | 图像中可见波形的水平范围。 |
| <b>振幅最小值</b>  浮点 | 波形的最小值（或Thickness）。 |
| <b>振幅最大值</b>  浮点 | 波形的最大值（或Thickness）。 |
| <b>噪声</b>Float | 将噪声应用于随机从其垂直范围中减去的波形。 |
| <b>位置</b>整数 | 波形在图像中的位置：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>居中：</i>原点位于图像的垂直中心</li> <li data-preserve-html="true"><i>底部：</i>原点为图像的底部</li> </ul> |
| <b>图案</b>整数 | 放置在波形的每个采样处的图案。 |
| <b>图案变体</b>Float | 适用于某些图案的额外调整。 |
| <b>无序</b>Float | 置换波形的值。    这可用于为其制作动画。 |
| <b>无序速度</b>Float | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作波形动画时控制位移速度。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![波形1 — 示例1](../../../../../../assets/waveform_01_v2_speed0.1_aniso0.gif "波形1 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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
