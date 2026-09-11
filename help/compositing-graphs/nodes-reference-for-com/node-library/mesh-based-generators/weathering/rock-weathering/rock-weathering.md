---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: 使用岩石风化节点，根据风化几何形状在岩石表面生成网格图案，以实现逼真的侵蚀效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 岩石风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 16%

---


# 岩石风化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rock-weathering.resources/rock-weathering.png){width="128px"}

<b>在</b>中基于网格的生成器>风化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Ambient occlusion</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>弯曲</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>正常WS</b> <i>颜色输入</i> | 用于内部效果和蒙版的世界空间标准映射。 |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭材料声道，例如，在使用Specular/光泽度映射而非金属/粗糙度时。 |
| <b>高级</b> |  |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>蒙版</b> <i>False/True</i> | 启用或禁用蒙版图。 |
| <b>效果</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>污迹</b> <i>0.0 - 1.0</i> |  |
| <b>边缘磨损</b> <i>0.0 - 1.0</i> |  |
| <b>已使用的岩石</b> <i>0.0 - 1.0</i> |  |
| <b>裂缝比例</b> <i>1.0 - 60.0</i> |  |
| <b>裂缝强度</b> <i>0.0 - 1.0</i> |  |
| <b>年龄</b> <i>0.0 - 1.0</i> |  |
| <b>年龄阈值</b> <i>0.0 - 1.0</i> |  |
| <b>锐边Scratches缩放</b> <i>1.0 - 32.0</i> |  |
| <b>锐边Scratches变形强度</b> <i>0.0 - 1.0</i> |  |
| <b>已使用的岩石去饱和度</b> <i>0.0 - 1.0</i> |  |
| <b>使用的岩石亮度</b> <i>0.0 - 1.0</i> |  |
| <b>混合</b> |  |
| <b>Diffuse强度</b> <i>0.0 - 1.0</i> | 混合强度。 |
| <b>Base color强度</b> <i>0.0 - 1.0</i> | 混合强度。 |
| <b>正常强度</b> <i>0.0 - 64.0</i> | “正常”混合强度。 |
| <b>Specular强度</b> <i>0.0 - 1.0</i> | 混合强度。 |
| <b>光泽度强度</b> <i>0.0 - 1.0</i> | 混合强度。 |
| <b>粗糙度强度</b> <i>0.0 - 1.0</i> | 混合粗糙度的强度。 |
| <b>Ambient occlusion强度</b> <i>0.0 - 1.0</i> | 混合环境遮蔽的强度。 |
| <b>Height强度</b> <i>0.0 - 1.0</i> | 混合Height的强度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rock-weathering.resources/rock-ex.gif" />
        </td>
    </tr>
</table>
