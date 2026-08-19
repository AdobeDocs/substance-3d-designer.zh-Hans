---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: 使用“Height到正常世界单位”节点，可以使用世界单位缩放将Height地图转换为正常地图，以便获取准确的细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常世界单位的Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---


# 正常世界单位的Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-hq.png){width="128px"}

## 正常世界单位的Height

**范围：** *筛选器/法线图*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

一种高级的“Height到正常”转换节点，在转换过程中使用真实世界的单位。

当您知道源高度图的尺寸并希望执行最精确的转换时（例如，在处理扫描的材质时），此功能非常有用。

## 参数

* **表面大小(cm)**： *0.0 - 1000.0*&#x200B;输入Heightmap的Dimension。
* **深度(cm)**： *0.0 - 100.0* Heightmap详细信息的最大深度。
* **普通格式**： *OpenGL，DirectX*\
  在不同正常映射格式之间切换（反转绿色通道）。
* **采样**： *标准，Sobel*&#x200B;在两个采样模式之间切换以确定精度。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
