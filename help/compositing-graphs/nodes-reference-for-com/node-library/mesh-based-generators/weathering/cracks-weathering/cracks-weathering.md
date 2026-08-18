---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: 使用裂缝风化节点，基于网格曲率和应力点向材料添加裂纹图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 裂缝风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# 裂缝风化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## 裂缝风化

**在：** *基于网格的生成器**/Weathering*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

这是一种同时适用于多个通道的完全素材效果。 它添加了一个随机裂纹图案，并控制扩展和深度。

在使用完整素材时，请确保正确理解[链接创建模式](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于内部效果和蒙版的烘焙或生成的映射。
* **Height** ：*灰度输入*\
  用于内部效果和蒙版的烘焙或生成的映射。
* **蒙版** ：*灰度输入*\
  用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。

### 参数

* **频道**
  * 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **高级**
  * **普通格式**： *DirectX，OpenGL*\
    在不同正常映射格式之间切换（反转绿色通道）。
  * **蒙版**： *False/True*\
    启用或禁用蒙版图。
* **效果**
  * **裂缝传播**： *0.0 - 1.0*&#x200B;裂缝应传播的距离。 这是此效果的主要控件。
  * **深度**： *0.0 - 1.0*&#x200B;裂纹效果的深度。 这主要影响Height，对视觉Thickness影响较小。
* **混合**
  * 控制效果与每个生成的通道的混合强度。

## 示例图像

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
