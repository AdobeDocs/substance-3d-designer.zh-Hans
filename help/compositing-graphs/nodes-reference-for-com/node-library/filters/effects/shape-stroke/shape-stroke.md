---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: 使用“形状描边”节点为形状添加描边轮廓，以创建边框和边缘效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状描边
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# 形状描边

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-stroke.png){width="128px"}

![](../../../../../../assets/shape-stroke-grayscale.png){width="128px"}

## 形状描边（灰度）

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在黑白蒙版（适用于灰度版本）或具有Alpha通道的形状（适用于颜色版本）周围添加描边或轮廓，就像您从其他2D图像编辑应用程序中所熟悉的那样。 可以看作[边缘检测](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)的更完整版本。

适用于各种图像编辑效果。

## 参数

* **宽度**： *-1.0 - 1.0*&#x200B;描边效果的宽度。
* **不透明度**： *0.0 - 1.0*\
  效果的全球不透明度。
* **（轮廓）颜色**： *（颜色值）*用于轮廓效果的颜色。
* **蒙版颜色**： *（颜色值） *（仅限灰度版本）**纯色用于透明度映射输出。
* **输入是预乘**： *False/True *（仅限颜色版本）**是否应该假定输入是预乘。
* **预乘输出**： *False/True*&#x200B;是否应该预乘输出。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapestroke-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
