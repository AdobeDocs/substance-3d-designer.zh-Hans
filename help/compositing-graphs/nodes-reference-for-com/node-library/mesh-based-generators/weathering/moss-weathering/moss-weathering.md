---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: 使用苔藓风化节点可根据网格曲率和位置将苔藓生长图案添加到素材。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 苔藓风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---


# 苔藓风化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/moss-weathering.png){width="128px"}

## 苔藓风化

**在：** *基于网格的生成器**/Weathering*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

这是一种同时适用于多个通道的完全素材效果。 它通过单个传播控件生成过度生长的苔藓效果。

此效果最适合用于生成的世界空间位置图和其他高度图。 虽然这不是一个确切的要求，但它使效果更加可靠。

在使用完整素材时，请确保正确理解[链接创建模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)。

## 参数

### 输入

* **位置**： *颜色输入*\
  烘焙的世界空间位置。
* **Height** ：*灰度输入*\
  其他Heightmap输入。
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
  * **苔藓传播**： *0.0 - 1.0*&#x200B;设置苔藓的传播。 从轻微的覆盖到厚重的、粗的深色苔藓，是逐步增长的。
* **混合**
  * **扩散强度**： *0.0 - 1.0*\
    扩散的混合强度。
  * **基色强度**： *0.0 - 1.0*\
    混合基色的强度。
  * **正常强度**： *0.0 - 1.0*\
    混合“正常”的强度。
  * **Specular强度**： *0.0 - 1.0*\
    混合Specular的强度。
  * **光泽强度**： *0.0 - 1.0*\
    混合光泽度的强度。
  * **粗糙度强度**： *0.0 - 1.0*\
    混合粗糙度的强度。
  * **环境遮蔽强度**： *0.0 - 1.0*\
    混合环境遮蔽的强度。
  * **Height强度**： *0.0 - 1.0*\
    混合Height的强度。

## 示例图像

![](../../../../../../assets/moss-ex.gif)

</td>
</tr>
</table>
