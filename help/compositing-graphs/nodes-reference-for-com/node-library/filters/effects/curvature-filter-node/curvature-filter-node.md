---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: 使用“曲率”过滤器节点，从Height图生成曲率图以检测凸曲面和凹曲面。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率（筛选器节点）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# 曲率（筛选器节点）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## 曲率

**范围：** *滤镜/效果*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

对输入[正常映射](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)执行简单、苛刻的单程曲率转换。 生成的贴图具有凸形区域的白色色调和凹形区域的黑色色调。 曲率始终会产生像素细线和尖锐过渡。

此节点对于某些边缘的快速突出显示或变暗非常有用。 与[曲率光滑](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)（可生成更高质量的结果）和[曲率光滑](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)（具有更多选项）相比，它的作用有限。

## 参数

* **强度**： *0.0 - 10.0*&#x200B;效果的强度。 增加结果的对比度。
* **普通格式**： *DirectX，OpenGL*\
  在不同正常映射格式之间切换（反转绿色通道）。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
