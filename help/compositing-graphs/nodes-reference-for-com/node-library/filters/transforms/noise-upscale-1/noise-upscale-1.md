---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: 使用噪声Upscale 1纹理，使用基于噪声的算法放大节点，以便在提高纹理分辨率时保留细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪声放大1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# 噪声放大1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## 噪声放大1

**在：** *筛选器/变换*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

程序化获取输入噪声并将其放大到双分辨率，保留细节但不会引入过多的拼贴。 使用“X”类型的蒙版并与原始输入图像类似的对比度进行混合（内部混合模式为“复制”）。

此节点主要用于优化使用重型、大噪声的慢图形。 它允许您使用更高的分辨率，而不会引入过多的额外计算时间。

另请参阅[噪声放大2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)和[噪声放大3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md)，了解此过程的不同变化。

## 参数

* **偏移1X**： *0.0 - 1.0*&#x200B;将顶部和底部滑过X轴。
* **偏移1Y**： *0.0 - 1.0*\
  在Y轴上滑动顶部和底部。
* **偏移2X**： *0.0 - 1.0*&#x200B;将左右部分滑过X轴。
* **偏移2Y**： *0.0 - 1.0*&#x200B;在Y轴上左右滑动部件。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise1ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
