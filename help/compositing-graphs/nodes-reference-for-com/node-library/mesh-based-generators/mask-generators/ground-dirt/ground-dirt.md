---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: 根据网格相对于地面的位置和方向，利用地面Dirt节点生成Dirt累积蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 地面Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# 地面Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## 地面Dirt

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示从地面向上累积的Dirt，与[从下到上](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md)或[Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md)相反。 它没有自定义映射覆盖。

## 输入

* **位置**： *灰度输入*\
  用于基础效果的烘焙位置映射。 必填！
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

## 参数

* **级别**： *0.0 - 1.0*\
  设置Dirt的总外观级别。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **Height**： *0.0 - 1.0*&#x200B;设置Dirt应显示的Height（按比例）。

## 示例图像

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
