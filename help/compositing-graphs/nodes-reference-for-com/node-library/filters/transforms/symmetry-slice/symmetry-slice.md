---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 使用“对称切片”节点沿对称轴切片纹理，以创建镜像图案和效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 对称切片
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# 对称切片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## 对称切片

**英寸：** *筛选器/变换*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

复杂的对称/镜像操作节点。 允许使用完全控制进行各种几何操作，但需要一些试验。

与[镜像](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md)和[对称](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)相比，此节点具有更多选项。

## 参数

* **对称模式**： *0 - 6*&#x200B;选择对称几何/镜像线。 选项包括“水平”、“垂直”、“左对角”、“左对角”、“垂直反相”、“边角”和“对角角”。
* **传输模式**： *0 - 6\
  混合模式。 选项为：*
* **混合**： *0.0 - 1.0*&#x200B;将原始图像混合回结果。
* **翻转**： *False/True*&#x200B;翻转原点，表示操作的原点端颠倒。 例如，“从左到右”对称就变为从右到左。
* **翻转2**： *False/True*&#x200B;仅在“对称模式”为5或6时使用。 反向角原点。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
