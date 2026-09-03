---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: 使用“垂直于Height”HQ节点将法线图转换为高品质高度图以进行表面细节提取。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常到Height总部
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# 正常到Height总部

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq-01.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一个反向转换节点，尝试将切空间正常映射转换回高度映射。 这是较高级的Height；[与Node相同](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md)的选项较少，并且使用不同的计算。

当您只有一个正常映射源，但仍要执行将其与高度映射相结合的操作时非常有用。 请记住，这永远无法提供100%的正确结果，因为将Height转换为正常格式时，由于过程的本质而丢失信息。 它永远无法替换正确生成的高图！

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>浮雕平衡</b> <i>0.0 - 1.0</i> | 混合低频和高频偏置。 |
| <b>Height强度</b> <i>0.0 - 1.0</i> | 高度图的强度或乘数有点像全局不透明度。 |
| <b>Height标准化</b> <i>False/True</i> | 自动缩放高度映射范围以使用完全对比度，如[自动色阶](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)。 |
| <b>质量</b> <i>正常，高</i> | 在速度或质量之间切换。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal-to-height-hq-02.png" />
        </td>
    </tr>
</table>
