---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: 使用“Shape Glow”（形状发光）节点为形状和纹理添加发光效果，创造明亮的大气视觉效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状发光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# 形状发光

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## 形状发光（灰度）

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在输入蒙版（适用于灰度版本）或具有Alpha通道的形状（适用于颜色版本）周围创建柔和发光。 与[发光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md)相比，它的工作方式更类似其他2D图像编辑软件，因为它具有更多控件，是一种更完整的效果。

## 参数

* **模式**： *柔和、精确*&#x200B;在两个精确模式之间切换。
* **宽度**： *-1.0 - 1.0*&#x200B;控制发光到达的距离。
* **外扩**： *0.0 - 1.0*&#x200B;模糊效果的切断/阈值化，使发光在形状附近显示为纯色。
* **不透明度**： *0.0 - 1.0*\
  混合发光效果的不透明度。
* **（阴影）颜色**： *（颜色值）*要应用于发光的色调。
* **蒙版颜色**： *（颜色值） *（仅限灰度版本）**纯色用于透明度映射输出。
* **输入是预乘**： *False/True *（仅限颜色版本）**是否应该假定输入是预乘。
* **预乘输出**： *False/True*&#x200B;是否应该预乘输出。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
