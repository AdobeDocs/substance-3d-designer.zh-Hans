---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 使用Sobel运算符通过曲率Sobel节点检测曲率边缘，以创建基于边缘的蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弯曲Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 弯曲Sobel

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## 弯曲Sobel

**范围：** *滤镜/效果*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

对输入[正常映射](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)执行简单、苛刻的单程曲率转换。 生成的贴图具有凸形区域的白色色调和凹形区域的黑色色调。 曲率将始终产生较粗的线条和尖锐的过渡。

此节点对于快速突出显示或调暗某些边缘非常有用。 它与[曲率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)略有不同，因为它可产生更好的质量结果，但仍然清晰且生硬。

## 参数

* **强度**： *0.0 - 1.0*&#x200B;效果的强度，用于调整对比度。
* **正常类型**： *DirectX，OpenGL*

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
