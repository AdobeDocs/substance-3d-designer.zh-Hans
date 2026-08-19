---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: 利用纤维玻璃Edge Wear节点，根据网格曲率生成玻璃纤维边缘的磨损蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 玻璃纤维Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# 玻璃纤维Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## 玻璃纤维Edge Wear

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

表示专门用于玻璃纤维类型的衣服的蒙版，可能用于布料。 由于纤维非常平铺、重复的特性，可以任选地启用三平面混合。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于边缘突出显示的已烘焙贴图。 必填！
* **环境遮蔽**： *灰度输入*\
  用于遮盖被遮盖区域的已烘焙贴图。 不需要，但绝对推荐。
* **污渍输入**： *灰度输入*\
  可选的自定义插槽以覆盖光纤模式。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。
* **正常世界空间**： *颜色输入*\
  仅用于三平面。
* **位置**： *颜色输入*\
  仅用于三平面。

### 参数

* **磨损级别**：*0.0 - 1.0*&#x200B;像[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)一样，逐渐显示磨损。
* **磨损对比度**： *0.0 - 1.0*&#x200B;设置总体效果对比度。
* **边缘Smoothness**： *0.0 - 16.0*&#x200B;设置高亮边缘的出血/模糊。
* **污渍量**： *0.0 - 1.0*&#x200B;设置要在边缘之间混合多少纤维效果。 结合磨损程度对此进行调整，以获得最大程度的控制。
* **环境遮蔽蒙版**： *0.0 - 1.0*&#x200B;设置AO对隐藏效果的影响量。
* **曲率粗细**： *0.0 - 1.0*&#x200B;设置曲率对凸边的影响量。
* **使用自定义污渍**： *False/True*&#x200B;用自定义映射覆盖内置光纤。
* **使用三平面**： *False/True*&#x200B;使[三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)能够隐藏接缝。
* **三平面混合对比度**： *0.0 - 1.0*&#x200B;控制三平面效果的对比度。

## 示例图像

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
