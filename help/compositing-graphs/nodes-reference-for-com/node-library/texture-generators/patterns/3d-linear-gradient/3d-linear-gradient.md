---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: 使用3D Linear gradient节点可根据空间效果的3D世界位置创建线性渐变。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D Linear gradient

**英寸：** *纹理生成器**/Patterns*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据输入位置映射创建体积渐变。 在3D空间的2点之间有效地生成从黑到白的过渡。 仅打算与GPU引擎结合使用。

另请参阅[3D体积蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)，了解类似效果。

## 参数

* **点位置模式**：*UV位置、世界空间位置*&#x200B;如果您想手动输入精确位置，请选择渐变点在UV空间中（在2D 视图中设置时效果最佳）还是在3D坐标中有效。
* **点1**：\
  渐变的起始点。 可以是基于“位置”模式的2D或3D坐标。
* **点2**：\
  渐变的终点。 可以是基于“位置”模式的2D或3D坐标。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。

## 示例图像

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
