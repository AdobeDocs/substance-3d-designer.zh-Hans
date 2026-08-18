---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: 使用“皮革风化”节点，根据网格曲率为皮革材料添加磨损图案和老化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 皮革风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# 皮革风化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## 皮革风化

**在：** *基于网格的生成器**/Weathering*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

这是一种同时适用于多个通道的完全素材效果。 它增加了皮革的随机磨损效果，同时控制了年龄和污浊度。 它类似于[织物风化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)，但专门针对皮革进行调整。\
除非插入适当的烘焙AO和世界空间正常映射，否则此效果不会非常好，因为它需要它们来充分计算和生成所有内容。

在使用完整素材时，请确保完全了解[链接创建模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)。

## 参数

### 输入

* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **普通Wold空间**： *颜色输入*
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
  * **Dust**： *0.0 - 1.0*&#x200B;根据世界空间正常映射中正对着的区域混合形成较暗的Dust效果。
  * **污迹**： *0.0 - 1.0*&#x200B;在全球Dirt/涂抹效果中混合，主要基于AO中遮蔽（深色）的区域。
  * **边缘磨损**： *0.0 - 1.0*&#x200B;根据“材质正常”为边缘添加锐化/强化效果。
  * **已使用**： *0.0 - 1.0*&#x200B;融入全球破旧的皮革外观。
  * **年龄**：*0.0 - 1.0*&#x200B;根据AO混合旧皮革外观。 职位安排受年龄限制的影响很大。
  * **年龄阈值**： *0.0 - 1.0*&#x200B;设置年龄效果的外观阈值。
  * **裂缝比例**： *1.0 - 16.0*&#x200B;设置旧皮革和旧皮革效果的深度。
  * **裂缝变形强度**： *0.0 - 1.0*&#x200B;设置旧皮革和旧皮革效果的强度。
  * **锐边Scratches比例**： *1.0 - 32.0*
  * **锐边Scratches变形强度**： *0.0 - 1.0*
  * **旧皮革去饱和度**：*0.0 - 1.0*&#x200B;设置旧皮革外观的饱和度和“旧皮革”效果。
  * **旧皮革亮度**：*0.0 - 1.0*&#x200B;设置旧皮革外观和“旧”效果的亮度。
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
