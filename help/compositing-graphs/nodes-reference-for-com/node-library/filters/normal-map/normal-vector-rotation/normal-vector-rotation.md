---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: 使用“法线矢量旋转”节点旋转法线图矢量，以调整表面光照和细节方向。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法线矢量旋转
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# 法线矢量旋转

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## 法线矢量旋转

**范围：** *筛选器/法线图*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

旋转正切空间中输入Normalmap的所有向量的普通效用节点。 并不会实际变换像素，而会修改它们所表示的值。 它可以利用可选映射向灰度小平面添加随机旋转。

## 输入

* **正常**： *颜色输入*\
  要执行旋转的基本映射。 必需。
* **旋转贴图（可选）**： *灰度输入*\
  调整旋转强度的灰度映射。

## 参数

* **旋转角度**： *0.0 - 1.0*\
  设置旋转正常映射的角度
* **普通格式**： *DirectX，OpenGL*\
  在不同的法线贴图格式之间切换（反转绿色通道）

## 示例

</td>
</tr>
</table>
