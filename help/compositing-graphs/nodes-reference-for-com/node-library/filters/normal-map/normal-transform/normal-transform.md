---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: 使用“法向变换”节点可以将变换应用于法线图，同时正确保留矢量方向。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# 正常变换

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## 正常变换

**范围：** *筛选器/法线图*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

与原子变换2D节点类似，这允许转换正常映射而不破坏正切空间，而是动态地重新计算，从而产生始终正确的正常映射。

## 参数

* **矩阵2x2**： *（转换矩阵）：*\
  旋转或缩放输入。
* **偏移**： *-0.5 - 0.5*\
  移动或平移结果。 当存在变换控件时，可以通过直接与画布交互来修改结果。
* **普通格式**： *DirectX，OpenGL*\
  在不同的法线贴图格式之间切换（反转绿色通道）

</td>
</tr>
</table>
