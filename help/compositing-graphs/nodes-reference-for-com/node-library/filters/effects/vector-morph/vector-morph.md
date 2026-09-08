---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: 使用Vector Morph节点使用矢量场在两个输入之间变形纹理，以实现平滑过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 矢量图Morph
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# 矢量图Morph

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## 矢量图Morph（灰度）

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

通过矢量图扭曲输入图像。 该效果类似于使用Normalmap的扭曲，或在视频游戏着色器中使用“流图”。 输入像素由在矢量图的红色和绿色值中定义的矢量移动。

此节点本身并不是最难使用的，但创建正确的矢量图非常小心。 我们建议您使用最高位深度以确保变形时的精度。

Vector Morph与[矢量变形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)非常相似：主要区别在于此Morph节点在被推到画布边界外部时不会“循环”或“平铺”结果。 相反，它会夹紧并重复边缘。

## 参数

### 输入

* **输入**： *彩色/灰度输入*&#x200B;应作为变形目标的源输入。
* **矢量字段**： *颜色输入*&#x200B;用于驱动变形的矢量映射。

### 参数

* **数量**： *0.0 - 1.0*&#x200B;设置变形效果的强度，用作矢量图的乘数。

## 示例图像

</td>
</tr>
</table>
