---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: 使用3D“Worley Noise”（3D粗杂色）节点根据3D位置生成“Worley noise”（粗杂色），创建体积纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Worley Noise
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 3D Worley Noise

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## 3D Worley Noise

**在：** *纹理生成器**/杂波*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

它是库中最通用和高级的噪声之一，基于输入位置映射在3D空间中生成Worley噪声。 提供了许多选项，使它具有比标准[细胞](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)或[距离](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)噪声更加强大的功能。

## 参数

* **缩放**： *1 - 64*\
  设置效果的全局比例。
* **大小**： *0.0 - 1.0*&#x200B;分别对X、Y和Z轴执行非均匀缩放。
* **模式**：*欧几里德，曼哈顿，Chebyshev，Minkowski\
  更改距离度量。 允许使用一些非常不同的噪声类型。*
* **闵可夫斯基数值**： *0.0 - 20.0*&#x200B;仅使用Minkowski距离度量。 在不同类型的度量之间进行混合。
* **样式**：*F1、F2、F2-F1、边框、随机颜色*&#x200B;设置度量组合数学运算。 支持更多组合。
* **边框宽度**： *0.0 - 1.0*&#x200B;当边框组合数学处于活动状态时，控制边框宽度。
* **圆形**： *0.0 - 1.0*&#x200B;仅适用于F1、F2和F2-F1模式。 设置级别中间位置。
* **反转**： *False/True*\
  反转结果。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
