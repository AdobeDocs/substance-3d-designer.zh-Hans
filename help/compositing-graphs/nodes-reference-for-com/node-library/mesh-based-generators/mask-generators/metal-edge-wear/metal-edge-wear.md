---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: 使用“金属Edge Wear”节点，根据网格曲率和位置在金属边上生成磨损蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金属Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 金属Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## 金属Edge Wear

**英寸：** *基于网格的生成器**/蒙版生成器*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示金属对象上的边缘磨损，凸起的凸起边缘上出现划痕和碎片，可能会被烘焙的AO暗区遮盖。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **污渍输入**： *灰度输入*
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。
* **正常世界空间**： *颜色输入*
* **位置**： *颜色输入*

### 参数

* **磨损级别**： *0.0 - 1.0*&#x200B;设置磨损总量，逐渐显示。
* **磨损对比度**： *0.0 - 1.0*&#x200B;设置最终结果的对比度。
* **边缘Smoothness**： *0.0 - 16.0*&#x200B;设置从曲率边缘衰减的Smoothness。
* **污渍量**： *0.0 - 1.0*&#x200B;设置要在边缘之间混合的污渍量。
* **污渍比例**： *1 - 16*&#x200B;设置污渍的比例。
* **环境遮蔽蒙版**： *0.0 - 1.0*&#x200B;设置AO对最终效果（暗区被遮盖）的影响量。
* **曲率粗细**： *0.0 - 1.0*&#x200B;设置曲率凸缘对最终效果的作用量。
* **使用自定义污渍**： *False/True*&#x200B;启用自定义污渍映射输入槽。
* **使用三平面**： *False/True*&#x200B;启用[三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)投影以隐藏接缝。
* **三平面混合对比度**： *0.0 - 1.0*&#x200B;设置三平面投影的混合对比度。

## 示例图像

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
