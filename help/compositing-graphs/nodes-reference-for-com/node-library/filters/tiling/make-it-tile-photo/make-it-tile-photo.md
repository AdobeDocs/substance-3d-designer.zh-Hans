---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: 使用“制作拼贴照片”节点将照片转换为无缝拼贴纹理，以创建素材。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 为其拼贴照片
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# 为其拼贴照片

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## 将其拼贴照片（灰度）

**范围：** *筛选器/拼贴*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点为由于非连续边缘而不可能平铺的任何图像提供了边缘修复功能。 除了输入图像的边缘之外，它不会影响任何其他内容。 如果要以不同的方式调整缩放或平铺，请查看[使其平铺修补](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md)。

## 参数

* **蒙版变形H**： *-100.0 - 100.0*&#x200B;在水平轴上引入变形，以避免未定义的过渡。
* **蒙版变形V**： *-100.0 - 100.0*&#x200B;在垂直轴上引入变形，以避免未定义的过渡。
* **蒙版大小H**： *0.0 - 1.0*&#x200B;设置过渡边缘达到的水平距离。
* **蒙版大小V**： *0.0 - 1.0*&#x200B;设置过渡边缘垂直达到的距离。
* **蒙版精度H**： *0.0 - 1.0*&#x200B;设置过渡的水平平滑程度。
* **蒙版精度V**： *0.0 - 1.0*&#x200B;设置过渡的垂直平滑程度。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
