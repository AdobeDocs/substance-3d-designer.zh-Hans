---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# 替换颜色范围

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## 替换颜色范围

**范围：** *滤镜/调整*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

用其他控件按目标颜色替换源颜色。 例如，可用于对素材ID映射的各个部分重新着色（烘焙）。

有关更高级的版本，请参阅[颜色匹配。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## 参数

* **源颜色**： *（颜色值）*要替换的颜色。
* **目标颜色**： *（颜色值）*要替换的颜色。
* **源范围**： *0.0 -* 1.0\
  所选的源的范围或容差。 可以增加，以便进一步相邻颜色也发生色相偏移。
* **阈值**： *0.0 - 1.0*&#x200B;范围的衰减/对比度。 设置为“低”将仅替换源颜色，设置为“高”将替换混合到“源”中的颜色。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
