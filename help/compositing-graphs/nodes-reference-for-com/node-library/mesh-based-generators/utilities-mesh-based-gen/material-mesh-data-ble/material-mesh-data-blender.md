---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: 使用“材质网格数据混合器”节点来混合材质网格数据，以便在不同的材质区域之间创建平滑过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质网格数据混合器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# 材质网格数据混合器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

## 材质网格数据混合器

**在：** *基于网格的生成器**/Utilities*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点旨在使添加基于烘焙数据的细节更加容易。 它随附了许多滑块，可根据任何和所有已烘焙贴图来修改输入的完整素材。 尝试一下，因为有很多选项

可用于执行诸如基于曲率或其他映射添加边缘突出显示、在某些AO中与扩散/基色混合、添加基于曲率和/或AO的遮蔽等操作。

## 参数

### 输入

* **完整素材输入（组“素材”）：**&#x200B;完整素材映射集。\
  此节点会修改这些属性，然后再次将其作为输出返回。
* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **Height**： *灰度输入*
* **正常**： *颜色输入*
* **顶点颜色**： *颜色输入*
* **正常世界空间**： *颜色输入*

### 参数

* **频道**
  * 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 影响以下参数的可用性。
* **已烘焙贴图**
  * 是否使用列出的已烘焙贴图进行计算。 影响以下参数的可用性。
* **扩散AO**： *0.0 - 1.0*&#x200B;要混合到扩散中的环境遮蔽量。
* **扩散锐边**： 0.0 - 1.0\
  要混合到漫射中的曲率映射量。
* **从顶点颜色扩散的颜色**： 0.0 - 1.0\
  要混合到漫射区域中的顶点颜色烘焙量。
* **漫射预照明**： 0.0 - 1.0\
  基于世界空间法线的（虚假）预光照量。
* **漫射卡通光照平衡**： 0.0 - 1.0\
  在“漫射”滑块的实际光照和卡通光照之间切换。
* **漫射卡通预光照图层**： 0 - 10\
  控制卡通光线计算的外观。
* **漫射卡通轮廓**： 0.0 - 1.0\
  控制卡通光线计算的外观。
* **基色AO**： 0.0 - 1.0\
  要混合为基色的环境遮蔽量。
* **基色锐化边缘**： 0.0 - 1.0\
  要混合到基色的曲率映射量。
* **基于顶点颜色的基色**： 0.0 - 1.0\
  混合为基色的顶点颜色烘焙量。
* **正常材质强度**： 0.0 - 1.0\
  烘焙（切线）正态映射的混合强度。
* **SpecularAO**： 0.0 - 1.0\
  在Specular中混合AO的强度。
* **明亮的锐边缘** Specular：0.0 - 1.0\
  混合Specular中曲率的强度。
* **Specular卡通轮廓**： 0.0 - 1.0\
  基于曲率，混合卡通Specular边缘轮廓效果的强度。
* **光泽深色锐化边缘**： 0.0 - 1.0\
  混合光泽度中曲率的强度。
* **明亮锐边的粗糙度**： 0.0 - 1.0\
  在粗糙度中混合曲率的强度。
* **粗糙度卡通轮廓**： 0.0 - 1.0\
  基于曲率，混合卡通粗糙度边缘轮廓效果的强度。
* **金属明亮的锐边缘**： 0.0 - 1.0\
  金属质感中曲率的混合强度。
* **金属卡通轮廓**： 0.0 - 1.0\
  基于曲率，混合卡通金属边缘轮廓效果的强度。
* **AO材料强度**： 0.0 - 1.0\
  已烘焙贴图AO与材料生成的AO混合强度，二者结合程度如何。
* **Height材质强度**： 0.0 - 1.0\
  将Height的强度与素材生成的Height混合，两个高度图的组合度如何。
* **Height材质混合类型**：增强，插值\
  用于合并两个高度图的混合模式。

## 示例图像

![](../../../../../../assets/blenddata-ex.gif)

</td>
</tr>
</table>
