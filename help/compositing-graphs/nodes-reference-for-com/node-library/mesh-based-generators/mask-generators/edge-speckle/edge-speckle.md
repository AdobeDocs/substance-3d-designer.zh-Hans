---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: 使用“边缘斑点”节点在网格边缘生成斑点磨损图案，以创建逼真的边缘损坏效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘斑点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# 边缘斑点

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## 边缘斑点

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版通过添加一点斑点来表示边缘，以便将其分解。 另请参阅[边缘Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于“边缘”突出显示的已烘焙贴图。 必填！
* **变体蒙版**： *灰度输入*\
  用于遮盖节点效果的可选蒙版插槽。 启用“覆盖变化蒙版”。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置边缘突出显示的总量。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **边缘选区**： *0.0 - 1.0*&#x200B;设置凸边缘的影响。
* **变化**： *0.0 - 1.0*&#x200B;设置变化蒙版打破效果的程度。
* **覆盖变体蒙版**： *False/True*&#x200B;用自定义输入插槽覆盖内置蒙版。

## 示例图像

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
