---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: 使用细胞2节点产生用于产生有机和生物纹理效果的中间细胞图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 细胞2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# 细胞2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![细胞2 — 图标](../../../../../../assets/cells_2.png "细胞2 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>细胞</b>壁噪声的变体。

具有可调壁Thickness的单元的二进制掩模。

另请参阅：[细胞1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、[细胞3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)、[细胞4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>边缘宽度</b>Float | 按Thickness比例调整单元格之间的壁网格。 （即不依赖于分辨率） |
| <b>反转</b>布尔值 | 切换输出图像中的黑色和白色。 |
| <b>无序</b>Float | 置换噪声的组成部分。    这可用于为噪声制作动画。 |
| <b>无序速度</b>Float | 调整<b>无序</b>参数应用的位移的距离。    在为噪声制作动画时，这可用于控制位移的速度。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴为方形，并将噪声生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![细胞2 — 示例1](../../../../../../assets/cells_2_1.png "细胞2 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![细胞2 — 示例2](../../../../../../assets/noise_cells_2_v2_speed0.3_aniso0.6.gif "细胞2 — 示例2"){zoomable="yes"}

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
