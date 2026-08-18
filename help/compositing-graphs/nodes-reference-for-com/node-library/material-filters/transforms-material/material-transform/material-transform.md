---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: 使用“素材变换”节点可将变换应用于素材输出，包括旋转、缩放和偏移。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# 材质变换

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## 材质变换

**英寸：** *素材滤镜/变换*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

素材变换只是[原子变换2D节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的“多通道”素材版本。 它与“变换2D”具有相同的界面，可同时变换输入素材的所有通道。

只要确保正确设置声道即可！ 默认情况下，同时启用“金属/粗糙度”和“Specular/光泽度”，这可能会导致混淆。

## 参数

* **转换**： *（转换矩阵）*\
  旋转和缩放结果。 移动/平移通过“偏移”参数完成
* **偏移**： *-0.5 - 0.5*\
  移动或转换结果。 当存在变换控件时，可以直接与画布交互来修改结果。
* **正常格式**\
  在DirectX和OpenGL格式之间进行选择（翻转绿色）。
* **频道**\
  在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
