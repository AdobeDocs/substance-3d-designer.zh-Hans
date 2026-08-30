---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: 使用“法向变换”节点可以将变换应用于法线图，同时正确保留矢量方向。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法线变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# 法线变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

与原子变换2D节点类似，这允许转换正常映射而不破坏正切空间，而是动态地重新计算，从而产生始终正确的正常映射。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>矩阵2x2</b> <i>（转换矩阵）：</i> | 旋转或缩放输入。 |
| <b>偏移</b> <i>-0.5 - 0.5</i> | 移动或转换结果。 当存在变换控件时，可以通过直接与画布交互来修改结果。 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同的法线贴图格式之间切换（反转绿色通道） |
