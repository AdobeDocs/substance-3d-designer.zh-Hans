---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: 使用材质选择器节点，根据网格数据选择材质，以创建多材质纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质选择器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# 材质选择器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector.png){width="128px"}

<b>在</b>中基于网格的生成器>实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将全色ID映射转换为二进制、黑白蒙版。 允许将不同的颜色混合并组合到一个蒙版中。

如果您不想使用[多材质混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)并且更喜欢手动使用蒙版，或者如果您想在其他位置手动使用这些相同的蒙版，这样做将非常方便。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>材质</b> <i>1 - 16</i> | 设置为其启用合并的材质数。 |
| <b>启用#1-16</b> <i>False/True</i> | 将颜色混合和组合切换到最终输出蒙版。 可以启用任意多个要组合的颜色。 |
| <b>#1-16</b> <i>（颜色值）</i> | 将转换为黑白的素材颜色的拾色器。 |
| <b>拾色器参数</b> | 修改颜色混合以及将颜色转换为黑白色。 |
| <b>模糊</b> <i>0.01 - 1.0</i> | 与相邻颜色混合的程度。 |
| <b>填充</b> <i>0.0 - 1.0</i> | 过渡的锐度，如对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/matselector-ex.png" />
        </td>
    </tr>
</table>
