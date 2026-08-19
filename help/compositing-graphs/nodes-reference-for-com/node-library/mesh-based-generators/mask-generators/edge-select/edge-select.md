---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: 使用“边选择”节点生成用于选择网格边的蒙版，以创建基于边的风化和磨损效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘选择
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 边缘选择

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## 边缘选择

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版是基于曲率选择任何类型的边缘的最佳方法。 凸的、凹的、任何层级或对比度都可以隔离，这提供了绝佳的快捷方式，以避免通过[层节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)手动执行此操作。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于加亮边的已烘焙贴图。 必填！
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  为“凸的”和“凹的”设置边加亮的总量。
* **对比度**： *0.0 - 1.0*\
  调整“凸的”和“凹的”高光对比度。
* **凸的**
  * **凸形边缘宽度**： *0.0 - 1.0*&#x200B;设置凸形边缘突出显示的宽度。 请记住，略微增加“柔和度”会导致边缘变细。
  * **凸柔和度**： *0.0 - 1.0*&#x200B;为凸形边缘设置过渡的柔和度。
  * **凸出强度**： *0.0 - 1.0*&#x200B;设置凸出边缘的边缘高亮最大强度。 设置为0将不突出显示。
* **凹形**
  * **凹边宽度**： *0.0 - 1.0*&#x200B;为凹边设置突出显示宽度。 请记住，略微增加“柔和度”会导致边缘变细。
  * **凹形柔和度**： *0.0 - 1.0*&#x200B;为凹形边缘设置过渡的柔和度。
  * **凹面强度**： *0.0 - 1.0*&#x200B;为凹边设置边缘突出显示的最大强度。 设置为0将不突出显示。

## 示例图像

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
