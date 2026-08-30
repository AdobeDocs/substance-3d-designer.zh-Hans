---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: 使用风化节点根据网格弯曲和应力点向材料添加裂纹图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 风化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering.png){width="128px"}

<b>在</b>中基于网格的生成器>风化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这是一种同时适用于多个通道的完全素材效果。 它添加了一个随机裂纹图案，并控制扩展和深度。

在使用完整材料时，确保正确理解[链接创建模式](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰度输入</i> | 用于内部效果和蒙版的烘焙或生成的映射。 |
| <b>Height</b> <i>灰度输入</i> | 用于内部效果和蒙版的烘焙或生成的映射。 |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 |
| <b>高级</b> |  |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>蒙版</b> <i>False/True</i> | 启用或禁用蒙版图。 |
| <b>效果</b> |  |
| <b>裂缝传播</b> <i>0.0 - 1.0</i> | 裂缝应该扩散到多远。 这是此效果的主要控件。 |
| <b>深度</b> <i>0.0 - 1.0</i> | 裂纹效应的深度。 这主要影响Height，对视觉Thickness影响较小。 |
| <b>混合</b> | 控制效果与每个生成的通道的混合强度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-ex.gif" />
        </td>
    </tr>
</table>
