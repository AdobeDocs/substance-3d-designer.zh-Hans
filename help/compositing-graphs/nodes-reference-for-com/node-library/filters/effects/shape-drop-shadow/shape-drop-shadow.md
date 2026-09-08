---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: 使用“形状投影”节点向形状添加投影效果，以便在纹理中创建深度和维度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# 形状投影

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## 形状投影（灰度）

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在输入黑白图像（适用于灰度版本）或具有透明度的图像（适用于白色蒙版版本）上，执行来自其他2D图像处理软件的众所周知的“投影”效果。

它不同于[阴影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md)效果，因为它返回应用了完全透明度的图像，从而使效果更完整，类似于您在其他软件中期望的效果。

## 参数

* **角度**： *0.0 - 1.0*&#x200B;光线的入射角度（虚光）。
* **距离**： *-0.5 - 0.5*&#x200B;阴影下拉到/远离形状的距离。
* **大小**： *0.0 - 1.0*&#x200B;控制阴影的模糊/模糊。
* **扩展**： *0.0 - 1.0*&#x200B;模糊效果的切断/阈值使阴影进一步扩展。
* **不透明度**： *0.0 - 1.0*\
  混合阴影效果的不透明度。
* **（阴影）颜色**： *（颜色值）*要应用于阴影的色调。
* **蒙版颜色**： *（颜色值） *（仅限灰度版本）**纯色用于透明度映射输出。
* **输入是预乘**： *False/True *（仅限颜色版本）**是否应该假定输入是预乘。
* **预乘输出**： *False/True*&#x200B;是否应该预乘输出。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
