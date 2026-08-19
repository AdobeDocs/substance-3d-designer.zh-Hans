---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: 使用“边缘Dirt”节点在网格边缘上生成Dirt累积蒙版，以创建逼真的边缘风化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# 边缘Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## 边缘Dirt

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示仅基于曲率图在边缘周围累积的Dirt效果。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于效果放置的已烘焙贴图。 必填！
* **变体蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽，仅在启用override参数时使用。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置Dirt量。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **变化**： *0.0 - 1.0*&#x200B;混合了应该发生多大程度的大规模蒙版/分解。
* **覆盖变体蒙版**： *False/True*

## 示例图像

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
