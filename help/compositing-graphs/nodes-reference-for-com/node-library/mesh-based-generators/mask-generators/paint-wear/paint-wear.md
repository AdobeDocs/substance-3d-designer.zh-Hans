---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: 使用油漆磨损节点可根据网格几何生成油漆磨损蒙版，以创建逼真的油漆碎裂效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 油漆磨损
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# 油漆磨损

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## 油漆磨损

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示油漆在边缘处脱落和磨损。

## 参数

### 输入

* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **变体蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置油漆磨损的总量，逐渐显现。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **遮蔽**： *0.0 - 1.0*&#x200B;设置烘焙的AO在防止较暗区域磨损方面的作用量。
* **半径**： *0.0 - 2.0*&#x200B;设置碎石效果从凸形边缘扩散的距离。
* **变化**： *0.0 - 1.0*&#x200B;设置变化量(污渍)以混合到效果中。
* **覆盖变体蒙版**： *False/True*&#x200B;启用自定义变体(污渍)映射输入槽。

## 示例图像

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
