---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: 使用“法线到Height”节点将法线映射转换为Height映射以提取表面深度信息。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常到Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# 正常到Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## 正常到Height

**范围：** *筛选器/法线图*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

一个反向转换节点，尝试将切空间正常映射转换回高度映射。 这是稍简单的版本；[正常于HeightHQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md)有更多选项。

当您只有一个正常映射源，但仍要执行将其与高度映射相结合的操作时非常有用。 请记住，这永远无法提供100%的正确结果，因为将Height转换为正常格式时，由于过程的本质而丢失信息。 如果您相应地调整设置，则这个非总部版本在转换简单细节方面做得不错。

## 参数

* **浮雕平衡**： *0.0 - 1.0*&#x200B;调整各频率对最终结果的影响程度。 这在很大程度上取决于输入图，需要进行一些调整。
* **普通格式**： *DirectX，OpenGL*\
  在不同正常映射格式之间切换（反转绿色通道）。
* **全局不透明度**： *0.0 - 1.0*&#x200B;调整效果的全局不透明度。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
