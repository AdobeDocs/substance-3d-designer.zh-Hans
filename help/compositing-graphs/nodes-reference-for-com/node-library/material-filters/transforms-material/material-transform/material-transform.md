---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: 使用变换节点可将变换应用于材料输出，包括旋转、缩放和偏移。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
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

**在：** *材质过滤器/变换*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

变换只是[原子变换 2D节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的“多通道”材料版本。 它会同时变换输入材料的所有声道，并具有与“变换2D”相同的界面。

只要确保正确设置声道即可！ 默认情况下，同时启用金属/粗糙度和Specular/光泽度，这可能会导致混淆。

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
