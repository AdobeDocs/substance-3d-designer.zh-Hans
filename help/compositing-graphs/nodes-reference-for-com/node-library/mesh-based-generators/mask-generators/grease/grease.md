---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: 使用“油脂”节点，根据网格几何形状和接触区域生成油脂积累蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 油脂
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# 油脂

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## 油脂

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版专门用于人物面部和其他特定区域。 在低Thickness区域生成皮肤油脂类型的蒙版。

## 参数

### 输入

* **Thickness**： *灰度输入*\
  整个效果所基于的烘焙Thickness图。 必填！
* **杂色**：*灰度输入*\
  可选的噪声映射以覆盖油脂污渍。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置要显示的效果总量。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **Thickness阈值**： *0.0 - 1.0*&#x200B;设置应显示效果的最小Thickness。 与“水平”同等重要；调整此参数以适合您的Thickness图。
* **覆盖杂色**： *False/True*&#x200B;设置为使用自定义输入插槽覆盖内部油脂污渍图。

## 示例图像

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
