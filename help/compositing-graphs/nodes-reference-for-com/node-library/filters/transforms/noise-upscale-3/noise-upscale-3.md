---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: 使用噪声Upscale 3纹理，使用基于噪声的高级算法来放大节点，以便在更高分辨率下保留细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪声放大3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# 噪声放大3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## 噪声放大3

**英寸：** *筛选器/变换*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

程序化获取输入噪声并将其放大到双分辨率，保留细节但不会引入过多的拼贴。 使用用户定义的蒙版在噪声原始比例之上混合颜色。

此节点主要用于优化使用重型、大噪声的慢图形。 它允许您使用更高的分辨率，而不会引入过多的额外计算时间。

另请参阅[噪声放大1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md)和[噪声放大2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)，在大多数情况下，它们往往在隐藏拼贴方面稍好一些。

## 参数

### 输入

* **灰度**： *灰度输入*\
  目标噪声图像。
* **蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

*无参数。*

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise3ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
