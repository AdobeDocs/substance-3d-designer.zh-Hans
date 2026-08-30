---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: 使用“Height到正常世界单位”节点，可使用世界单位缩放将高度图转换为法线图，以便获得准确的细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常世界单位的Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# 正常世界单位的Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/normal-hq.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种高级的“Height到正常”转换节点，在转换过程中使用真实世界的单位。

当您知道源高度图的尺寸并希望执行最精确的转换时（例如，在处理扫描的材料时），此功能非常有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>表面大小（厘米）</b> <i>0.0 - 1000.0</i> | 输入高度映射的Dimension。 |
| <b>深度（厘米）</b> <i>0.0 - 100.0</i> | Heightmap详细信息的最大深度。 |
| <b>正常格式</b> <i>OpenGL，DirectX</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>取样</b> <i>标准， Sobel</i> | 在两个采样模式之间切换以确定精度。 |
