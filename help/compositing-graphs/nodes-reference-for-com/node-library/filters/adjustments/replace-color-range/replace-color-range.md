---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: 使用“替换颜色范围”节点，可用新颜色替换指定范围内的颜色以进行颜色校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 替换颜色范围
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# 替换颜色范围

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

用其他控件按目标颜色替换源颜色。 例如，可用于对素材ID映射的各个部分重新着色（烘焙）。

有关更高级的版本，请参阅[颜色匹配。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>源颜色</b> <i>（颜色值）</i> | 要替换的颜色。 |
| <b>目标颜色</b> <i>（颜色值）</i> | 要替换的颜色。 |
| <b>源范围</b> <i>0.0 - 1.0</i> | 所选的源的范围或容差。 可以增加，以便进一步相邻颜色也发生色相偏移。 |
| <b>阈值</b> <i>0.0 - 1.0</i> | 范围的衰减/对比度。 设置为“低”将仅替换源颜色，设置为“高”将替换混合到“源”中的颜色。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-example.png" />
        </td>
    </tr>
</table>
