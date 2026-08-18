---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: 使用“边损坏”节点在网格边上生成损坏蒙版，以创建逼真的边磨损和破损效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘损坏
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# 边缘损坏

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-damages.png){width="128px"}

## 边缘损坏

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示基于曲率和烘烤的AO对凸起的凸边缘造成的损坏。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于效果放置的已烘焙贴图。 必填！
* **环境遮蔽**： *灰度输入*\
  用于效果放置的已烘焙贴图。 必填！
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  要应用的边缘损坏量。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **损坏强度**： *0.0 - 1.0*&#x200B;在破碎、一致的外观与混乱、划痕、严重损坏的外观之间切换。

## 示例图像

![](../../../../../../assets/edge-damages-ex.gif)

</td>
</tr>
</table>
