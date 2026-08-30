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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# 材质变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>进入：</b>材质过滤器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

素材变换只是[原子变换2D节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的“多通道”素材版本。 它与“变换2D”具有相同的界面，可同时变换输入素材的所有通道。

只要确保正确设置声道即可！ 默认情况下，同时启用“金属/粗糙度”和“Specular/光泽度”，这可能会导致混淆。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>转换</b> <i>（转换矩阵）</i> | 旋转和缩放结果。 移动/平移通过“偏移”参数完成 |
| <b>偏移</b> <i>-0.5 - 0.5</i> | 移动或转换结果。 当存在变换控件时，可以直接与画布交互来修改结果。 |
| <b>正常格式</b> | 在DirectX和OpenGL格式之间进行选择（翻转绿色）。 |
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 |
