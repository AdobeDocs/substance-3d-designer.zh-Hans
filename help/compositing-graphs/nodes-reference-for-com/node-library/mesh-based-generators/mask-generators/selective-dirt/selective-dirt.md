---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: 利用“选择性Dirt”节点，根据网格几何形状生成选择性Dirt累积蒙版，用于逼真的风化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 可选Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# 可选Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## 可选Dirt

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)蒙版表示凸形边缘上的简单Dirt效果。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **变体蒙版**： *灰度输入*\
  可选的变体映射，可通过参数启用。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置效果的总级别，逐渐显示出来。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **变化**： *0.0 - 1.0*&#x200B;设置要混合到效果中的变化/污渍量。
* **覆盖变体蒙版**： *False/True*&#x200B;允许使用自定义输入插槽覆盖变体。

## 示例图像

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
