---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: 使用泄漏节点根据网格几何形状生成泄漏图案，以创建水渍和流体效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 泄露
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# 泄露

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## 泄露

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此节点表示从尖锐边缘泄露出的Dirt和尘埃条纹。 当条纹与烘焙位置一起生成时，它们总是向下运行。

确保尝试更改变化蒙版：因为它驱动条纹的放置，这可能会产生比使用其他蒙版生成器更大的影响。

## 参数

### 输入

* **位置**： *灰度输入*\
  烘焙位置图，用于条纹方向。 必填！
* **曲率**： *灰度输入*\
  用于条纹放置的已烘焙贴图。 必填！
* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。 建议使用，但您可以使用纯白色。
* **正常世界空间**： *颜色输入*\
  烘焙世界空间常态图，用于条纹方向。 必填！
* **变体蒙版**： *灰度输入*\
  可选的变化蒙版，可通过将覆盖设置为True来启用。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  结果的总级别。 逐渐显示效果，同时影响长度。 应该设置得相当高，才能长滴水滴。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **变化**： *0.0 - 1.0*&#x200B;设置用于遮盖条痕的大规模变化量。 将此值设置为0可产生完全一致的条纹，因此应避免这样做。
* **长度**： *0.0 - 8.0*&#x200B;条纹滴的长度。 在较小的范围内将此值设置得太高将导致出现明显的步进。 同时尝试使用色阶。
* **遮蔽**： *X、Y、Z、None*&#x200B;设置AO应影响的方向。
* **覆盖变体蒙版**： *False/True*&#x200B;允许使用自定义输入插槽覆盖变体蒙版。 使用稀疏或较稠的蒙版可能非常有趣，是控制滴落的良好方法。

## 示例图像

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
