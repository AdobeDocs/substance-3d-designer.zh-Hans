---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: 使用“颜色加深”混合节点通过增加对比度来调暗纹理，以创建阴影和加深效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 颜色加深
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# 颜色加深

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## 颜色加深

**范围：** *滤镜/混合*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

在前景和背景之间执行颜色加深混合。 数学公式为1 - （1 — 背景）/前景。

## 参数

### 输入

* **前景**： *颜色输入*
* **背景**： *颜色输入*
* **蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **不透明度**： *0.0 - 1.0*\
  在前景和背景之间混合不透明度。
* **Alpha 值混合处理**： *False/True*\
  切换前景颜色和背景Alpha 通道的混合。 如果设置为False，则忽略前景的Alpha 通道。

## 示例图像

</td>
</tr>
</table>
