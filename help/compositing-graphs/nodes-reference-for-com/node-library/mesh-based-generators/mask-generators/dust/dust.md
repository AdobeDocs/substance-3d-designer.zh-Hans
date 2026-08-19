---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: 使用Dust根据网格几何形状生成Dust累积蒙版，用于创建逼真的Dust和颗粒效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示在遮蔽的降低区域中以及仅在面部朝上的区域中积累的Dust。 需要正确的烘焙原子氧和世界空间法线才能工作。

## 参数

### 输入

* **环境遮蔽**： *灰度输入*\
  用于Dust放置的已烘焙贴图。 必填！
* **正常世界空间**： *颜色输入*\
  用于Dust放置的已烘焙贴图。 必填！
* **杂色**：*灰度输入*\
  自定义Dust映射（可选），仅在“覆盖杂色”设置为True时出现。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置Dust的总量。
* **对比度**： *0.0 - 1.0*\
  调整Dust的对比度。
* **遮蔽量**： *0.0 - 1.0*&#x200B;设置AO的影响；被遮挡区域将出现更多Dust。
* **杂色不透明度**： *0.0 - 1.0*&#x200B;设置灰尘区域中可见的杂色量。
* **覆盖杂色**： *False/True*&#x200B;设置为使用自定义Dust映射输入。

## 示例图像

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
