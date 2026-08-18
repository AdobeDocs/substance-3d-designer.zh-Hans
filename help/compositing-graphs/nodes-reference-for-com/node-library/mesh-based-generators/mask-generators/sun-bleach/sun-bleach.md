---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: 使用“Sun Bleach”（太阳漂白）节点可根据太阳曝光生成蒙版，打造逼真的太阳漂白和渐隐效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 太阳漂白
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 太阳漂白

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## 太阳漂白

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版类似于[光线](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md)，但也支持AO，从而可生成一个表示效果上的光漂白和淡化的蒙版。

## 输入

* **正常世界空间**： *颜色输入*
* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

## 参数

* **级别**： *0.0 - 1.0*\
  设置漂白的总量，将效果进一步下移。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **遮蔽**： *0.0 - 1.0*&#x200B;设置AO对最终结果的影响。

## 示例图像

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
