---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: 使用细胞4节点产生高级细胞图案，用于产生有机和生物纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 细胞4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---


# 细胞4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![细胞4 — 图标](../../../../../../assets/cells_4.png "细胞4 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>细胞</b>壁噪声的变体。

每个单元格被分配一种平坦颜色，该颜色可以是随机的，也可以是从输入图像中取样的。

另请参阅：[细胞1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、[细胞2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、[细胞3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 输入

</td>
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

## 输入

|  |  |
| --- | --- |
| <b>输入</b> *灰度* |  |

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
| <b>颜色源</b>整数 | 应用于单元格的单色源：<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>随机：</i></b>使用由节点的随机种子控制的随机颜色</li> <li data-preserve-html="true"><b><i>伪随机：</i></b>使用由单独的用户集值植入的随机颜色</li> <li data-preserve-html="true"><b><i>图像输入：</i></b>使用在输入图像中的单元格位置取样的颜色</li> </ul> |
| <b>伪随机种子</b>整数&#x200B;*在“颜色源”设置为“伪随机源”时可用* | 允许独立于节点种子更改颜色的种子。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![细胞4 — 示例1](../../../../../../assets/cells_4_1.png "细胞4 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![细胞4 — 示例2](../../../../../../assets/noise_cells_4_v2_speed0.3_aniso0.6.gif "细胞4 — 示例2"){zoomable="yes"}

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
