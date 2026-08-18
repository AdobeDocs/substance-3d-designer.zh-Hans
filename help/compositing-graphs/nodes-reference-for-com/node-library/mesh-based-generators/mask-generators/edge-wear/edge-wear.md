---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: 使用Edge Wear节点在网格边缘生成磨损蒙版，以创建逼真的边缘损坏和风化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此节点表示对象边缘上的磨损。 它有几个参数，但并不是最容易使用的：我们建议您边玩边感受一些东西。 此节点功能非常强大，但无法执行自定义覆盖蒙版。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置效果的总分布。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **阈值**： *0.0 - 1.0*&#x200B;与级别类似，设置效果的总分布。
* **边缘宽度**： *0.0 - 1.0*&#x200B;设置高光效果的饱满度。 减少以使它们更稀疏。
* **无序**： *0.0 - 1.0*\
  设置要混合以分解Smoothness的杂色量。

## 示例图像

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
