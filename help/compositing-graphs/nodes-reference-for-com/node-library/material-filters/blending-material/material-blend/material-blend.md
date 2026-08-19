---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: 使用素材混合节点，通过蒙版将整个素材混合在一起，以创建复合材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# 材质混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## 材质混合

**范围：** *素材滤镜/混合*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

材质混合是多通道、全材质等同于[原子混合节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)。 它基于灰度蒙版或可选地基于色彩 ID 蒙版中的一种颜色，在两个完整素材（所有可能的通道）之间混合。

如果要混合两种材质并具有灰度图但没有全色ID烘焙，此节点非常有用。 如果您确实有一个Color ID烘焙并且想要混合两种以上的素材，我们建议您使用[多素材混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)。

## 参数

### 输入

* **颜色ID**： *颜色输入*\
  可选的烘焙颜色ID映射。
* **灰度蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **频道**
  * 当使用“Specular/光泽度”映射而不是“金属/粗糙度”时，可打开和关闭此组中的素材通道。
* **扩散**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **基色**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **正常**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
* **Specular**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **具发射性**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **光泽度**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **粗糙度**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **金属质感**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **Specular level**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **环境遮蔽**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **Height**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **不透明度**
  * **不透明度**： *0.0 - 1.0*\
    在前景和背景之间混合不透明度
  * **混合模式**：*正常、相加、相减、相乘、相加/减色、最大值、最小值、开关*
* **色彩 ID 蒙版**： *False/True*&#x200B;使用色彩 ID 蒙版而非灰度蒙版。 请记住，这只适用于一种颜色！
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
