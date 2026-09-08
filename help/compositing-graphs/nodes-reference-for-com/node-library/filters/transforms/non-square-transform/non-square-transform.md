---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: 使用“非正方形变换”节点，可以将变换应用于具有独立X和Y缩放的非正方形纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非方形变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# 非方形变换

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 非方形变换（灰度）

**英寸：** *筛选器/变换*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

[变换2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的非方形安全版本。 自动检测非方形比例，并可以将正方形变换到非方形画布上。

确保您完全理解[图形参数](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)以充分利用此节点，因为您需要正确设置一些设置：

* 您的&#x200B;**图形**&#x200B;大小应为非方形，否则不需要此节点。
* 将非正方形变换&#x200B;**节点的**&#x200B;输出大小设置为“*相对于父代*”。
* 如果只想将输入变换到单个位置，请将&#x200B;**节点的**&#x200B;拼贴模式设置为“*无拼贴*”。

## 参数

* **磁贴模式**：*自动、手动*&#x200B;是否启用自动非方形补偿。
* **磁贴**： *1 - 16*&#x200B;仅当“磁贴模式”设置为“手动”时可访问。 允许您以拼贴安全的方式更改比例。
* **偏移**： *0.0 - 1.0*\
  移动或转换结果。 双击滑块以输入负值。
* **旋转**： *0.0 - 1.0*&#x200B;旋转输入图像。
* **安全旋转（仅限正方形）**： *False/True*&#x200B;捕捉安全值以保持像素的锐度。
* **背景颜色**： *（颜色值）*要用来填充图像的背景颜色。 仅当Base Parameters中的[拼贴模式设置为“*无拼贴*”](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)时可见。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
