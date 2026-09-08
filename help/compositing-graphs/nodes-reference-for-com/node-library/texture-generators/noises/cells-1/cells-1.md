---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-1.html"
breadcrumb-title: ''
description: 使用细胞1节点产生基本细胞图案，用于产生有机和生物纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 细胞1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 细胞1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![细胞1 — 图标](../../../../../../assets/cells_1.png "细胞1 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>细胞</b>壁噪声的变体。

用户选择的图案使用“最大”混合模式进行散布和叠加。

另请参阅：[细胞2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、[细胞3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)、[细胞4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>模式</b>整数 | 在生成的图像中散布的基本形状。 |
| <b>图案大小</b>浮点2 | 其单元格中散布图案大小的乘数，其中1.0是单元格的整个跨度。 |
| <b>图案缩放</b>浮动 | <b>图案大小</b>的乘数，其中1.0为全尺寸。 |
| <b>明亮度随机</b>浮点 | 从单元格中随机减去的明亮度范围，其中1是完整范围。 |
| <b>角度</b>浮动 | 用来设置单元格方向的角度，以匝数为单位，从右边水平开始。 |
| <b>角度随机</b>浮点 | 应用于<b>角度</b>值的随机变化的最大值（轮次数）。 |
| <b>拼贴偏移</b>浮动2 | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![细胞1 — 示例1](../../../../../../assets/cells_1_1.png "细胞1 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![细胞1 — 示例2](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.3.gif "细胞1 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![细胞1 — 示例3](../../../../../../assets/noise_cells_1_v2_speed0.5_aniso0.6.gif "细胞1 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![细胞1 — 示例4](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.6.gif "细胞1 — 示例4"){zoomable="yes"}

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
