---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: 使用“边切口”节点在网格边上生成切口图案，以创建逼真的边损伤和缩进效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边凹槽
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# 边凹槽

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-notch.png){width="128px"}

## 边凹槽

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示用于凸起的边缘的简单蒙版，被高频噪点分解。 有关更多选项，请参阅[边缘Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)或[边缘损坏](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md)。

## 输入

* **曲率**： *灰度输入*\
  用于加亮边的已烘焙贴图。 必填！
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

## 参数

* **级别**： *0.0 - 1.0*\
  设置“边凹槽”效果的级别。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。

## 示例图像

![](../../../../../../assets/edge-notch-ex.gif)

</td>
</tr>
</table>
