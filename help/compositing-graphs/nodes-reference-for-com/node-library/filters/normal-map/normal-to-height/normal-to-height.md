---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: 使用“法向于Height”节点将法线图转换为高度图以提取表面深度信息。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常到Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# 正常到Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height.resources/normal-to-height.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一个反向转换节点，尝试将正切空间正常映射转换回Heightmap。 这是稍简单的版本；[正常于HeightHQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md)有更多选项。

当您只有一个正常映射源，但仍要执行将其与高度映射相结合的操作时非常有用。 请记住，这永远无法提供100%的正确结果，因为将Height转换为正常格式时，由于过程的本质而丢失信息。 如果您相应地调整设置，则这个非总部版本在转换简单细节方面做得不错。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>浮雕平衡</b> <i>0.0 - 1.0</i> | 调整不同频率对最终结果的影响程度。 这在很大程度上取决于输入图，需要稍加调整。 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>全局不透明度</b> <i>0.0 - 1.0</i> | 调整效果的全局不透明度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height.resources/normal2heightex.png" />
        </td>
    </tr>
</table>
