---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: 使用“多方向变形”节点可在多个方向应用变形效果，以创建复杂的扭曲图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多方向变形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# 多方向变形

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-directional-warp-color.png)![](../../../../../../assets/multi-directional-warp-grayscalepng.png)

## 多定向翘曲（灰度）

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

多方向变形可在置换的纹理保持原位时，沿相反方向多次应用[方向变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)。 它与标准方向变形的不同之处在于，它可以在多个方向推送，而原子版本只允许一个方向。 通过这种方式，它解决了经典问题：方向变形似乎总是在单个方向将您的图像推走太多，而不是沿多个方向或轴而不是单个方向工作。

它主要与[Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md)不同，因为它稍微受限一些：变形的方向仅通过参数控制，不能通过输入映射设置。 优点是使用起来稍微容易一些，并且根据您的用例可以更精确。

## 参数

### 输入

* **输入**： *灰度/彩色输入*\
  将应用变形的基础图。 可以是彩色或灰度。
* **强度输入**：*灰度输入*\
  驱动变形效果强度的强制蒙版图必须是灰度。

### 参数

* **强度**： *0.0 - 20.0*\
  设置变形效果的强度，将像素向外推移的距离。
* **变形角度**： *0.0 - 1.0*\
  设置应用变形效果的角度或方向。
* **模式**： *平均值、最大值、最小值、链形*\
  设置连续刀路的混合模式。 仅当方向数为2或4时才有效！
* **方向**： *1、2、4*&#x200B;设置变形工作的多少轴。 1表示沿角度的方向移动，与该方向相反，2表示角度的轴加上垂直轴，4表示之前的轴，加上45度增量。

## 示例图像

</td>
</tr>
</table>
