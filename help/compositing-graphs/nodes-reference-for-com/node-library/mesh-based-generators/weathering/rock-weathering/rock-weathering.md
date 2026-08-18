---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: 使用岩石风化节点，根据网格几何形状在岩石表面生成风化图案，以实现逼真的侵蚀效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 岩石风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# 岩石风化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## 岩石风化

**在：** *基于网格的生成器**/Weathering*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

## 参数

### 输入

* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **正常WS**： *颜色输入*\
  用于内部效果和蒙版的烘焙世界空间正常映射。
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
  * **Dust**： *0.0 - 1.0*
  * **脏度**： *0.0 - 1.0*
  * **边缘磨损**： *0.0 - 1.0*
  * **使用的岩石**： *0.0 - 1.0*
  * **裂缝比例**： *1.0 - 60.0*
  * **裂缝强度**： *0.0 - 1.0*
  * **年龄**： *0.0 - 1.0*
  * **年龄阈值**： *0.0 - 1.0*
  * **锐边Scratches比例**： *1.0 - 32.0*
  * **锐边Scratches变形强度**： *0.0 - 1.0*
  * **已使用的岩石去饱和**： *0.0 - 1.0*
  * **使用的岩石亮度**： *0.0 - 1.0*
* **混合**
  * **扩散强度**： *0.0 - 1.0*\
    扩散的混合强度。
  * **基色强度**： *0.0 - 1.0*\
    混合基色的强度。
  * **正常强度**： *0.0 - 64.0*\
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

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>
