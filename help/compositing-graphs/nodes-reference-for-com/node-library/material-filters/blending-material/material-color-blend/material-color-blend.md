---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: 使用“材料颜色混合”节点可以混合材料之间的颜色通道，以创建复合材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料颜色混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# 材料颜色混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## 材料颜色混合

**范围：** *材质过滤器/混合*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点允许通过在顶部混合纯色来调整多通道完全材料。 这是[材料调整混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)的主要区别，它只允许对通道进行[色阶](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)类型的调整，而此节点使用纯色的[混合](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)类型的调整。

此节点在要将平面Base color提示引入Diffuse或颜色时最有用，或要通过使用设置的纯色值“平整”其它通道时最有用。

## 参数

### 输入

* **颜色ID**： *颜色输入*\
  用于遮盖节点效果的遮罩槽。
* **灰度蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **频道**
  * 例如，在使用Specular/光泽度映射而非金属/粗糙度时，可打开和关闭此组中的材料通道。
* **Diffuse**
  * **颜色**： *（颜色值）*要在Diffuse通道顶部混合的颜色值。
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度。
  * **混合模式**：*正常、相加、去除、正片叠底、相加/次方、最大值、最小值、切换*&#x200B;混合模式以在操作中使用。
* **Base color**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **正常**
  * **源**： *Height，蒙版*
  * **混合模式**： *合并，混合*
  * **Height强度**： *0.0 - 1.0*
  * **Height不透明度**： *0.0 - 1.0*
  * **格式**： *DirectX，OpenGL*
* **Specular**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **Emissive**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **光泽度**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **粗糙度**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **金属**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **Specular level**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **Ambient occlusion**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **Height**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **不透明度**
  * 使用此通道上与Diffuse组中相同的选项混合纯色。
* **色彩 ID 蒙版**： *False/True*&#x200B;使用色彩 ID 蒙版而非灰度蒙版。 请记住，这只适用于一种颜色！\
  启用以下所有选项。
* **颜色**： *（颜色值）*要选取哪种颜色并将其转换为白色。
* **模糊度**： *0.01 - 1.0*&#x200B;您选取的颜色混合到其邻近区域的程度。
* **填充**： *0.0 - 1.0*&#x200B;所选颜色的过渡对比度。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
