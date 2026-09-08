---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: 使用网格数据混合器节点混合材料网格数据，以便在不同的材料区域之间创建平滑的过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格数据混合器
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# 网格数据混合器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

<b>在</b>中基于网格的生成器>实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点旨在使基于烘焙数据添加细节更加容易。 它随附了许多滑块，可根据任何和所有材料来修改输入的完整已烘焙贴图。 尝试一下，因为有很多选项

它可以用于执行诸如基于弯曲或其他地图添加边缘突出显示、在某些AO中与Diffuse/基色混合、基于Specular和/或AO添加弯曲遮蔽等操作。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>完整材料输入（组“材料”）</b> | 一整套材料地图。<br><br>此节点将修改这些字段，然后再次将其作为输出返回。 |
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>曲率</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>Height</b> <i>灰度输入</i> |  |
| <b>正常</b> <i>颜色输入</i> |  |
| <b>顶点颜色</b> <i>颜色输入</i> |  |
| <b>世界空间正常</b> <i>颜色输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 影响以下参数的可用性。 |
| <b>已烘焙贴图</b> | 是否使用列出的已烘焙贴图进行计算。 影响以下参数的可用性。 |
| <b>DiffuseAO</b> <i>0.0 - 1.0</i> | 要混合到Diffuse中的Ambient occlusion量。 |
| <b>锐边Diffuse</b> <i>0.0 - 1.0</i> | 要混合到Diffuse中的弯曲图量。 |
| <b>Diffuse</b> <i>0.0 - 1.0</i> | 要混合到Diffuse中的顶点烘焙量。 |
| <b>Diffuse预照明</b> <i>0.0 - 1.0</i> | 基于世界空间法线的预照量（虚假）。 |
| <b>卡通光照平衡Diffuse</b> <i>0.0 - 1.0</i> | 在Diffuse的逼真和卡通光线之间切换。 |
| <b>动画预光照图层Diffuse</b> <i>0 - 10</i> | 控制卡通光线计算的外观。 |
| <b>Diffuse卡通轮廓</b> <i>0.0 - 1.0</i> | 控制卡通光线计算的外观。 |
| <b>Base colorAO</b> <i>0.0 - 1.0</i> | 要混合为基色的Ambient occlusion量。 |
| <b>锐边Base color</b> <i>0.0 - 1.0</i> | 要混合为基色的弯曲图量。 |
| <b>Base color来自顶点颜色</b> <i>0.0 - 1.0</i> | 要混合为基色的烘焙量。 |
| <b>正常材料强度</b> <i>0.0 - 1.0</i> | 混合烘焙(正切)正常映射的强度。 |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | 在Specular中混合AO强度。 |
| <b>Specular明亮的锐边缘</b> <i>0.0 - 1.0</i> | 在Specular中混合弯曲的强度。 |
| <b>Specular卡通轮廓</b> <i>0.0 - 1.0</i> | 基于弯曲混合卡通Specular边缘轮廓效果的强度。 |
| <b>光泽度深色锐化边缘</b> <i>0.0 - 1.0</i> | 在光泽度中混合弯曲的强度。 |
| <b>粗糙度明亮的锐边缘</b> <i>0.0 - 1.0</i> | 在粗糙度中混合弯曲的强度。 |
| <b>粗糙度卡通轮廓</b> <i>0.0 - 1.0</i> | 基于弯曲混合卡通粗糙度边缘轮廓效果的强度。 |
| <b>金属明亮的锐边缘</b> <i>0.0 - 1.0</i> | 在金属中混合弯曲的强度。 |
| <b>金属卡通轮廓</b> <i>0.0 - 1.0</i> | 基于弯曲混合卡通金属边缘轮廓效果的强度。 |
| <b>AO材料强度</b> <i>0.0 - 1.0</i> | 已烘焙贴图AO与材料生成AO的混合强度，二者结合的程度。 |
| <b>Height的材料强度</b> <i>0.0 - 1.0</i> | Height与材料生成Height的混合强度，二者结合的程度。 |
| <b>材料混合类型</b> <i>增强，插值</i> | 用于合并两个高度图的混合模式。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/blenddata-ex.gif" />
        </td>
    </tr>
</table>
