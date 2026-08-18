---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: 使用“杂色放大2”节点，可以使用基于杂色的插值来放大纹理，以保持较大尺寸的纹理质量。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪声放大2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# 噪声放大2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## 噪声放大2

**英寸：** *筛选器/变换*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

对输入噪声进行程序化处理并将其放大到双分辨率，保留细节但不会引入过多拼贴。 使用“X”类型的蒙版并以比原始输入更低对比度进行混合（内部混合模式为“最大”和“最小”）。

此节点主要用于优化使用重噪声、大噪声的慢速图。 它允许您使用更高的分辨率，而不会引入过多的额外计算时间。

有关此过程的不同变化，另请参阅[Noise Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md)和[Noise Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md)。

## 参数

* **偏移1X**： *0.0 - 1.0*&#x200B;在X轴上滑动顶部和底部。
* **偏移1Y**： *0.0 - 1.0*\
  在Y轴上滑动顶部和底部零件。
* **偏移2X**： *0.0 - 1.0*&#x200B;在X轴上左右滑动零件。
* **偏移2Y**： *0.0 - 1.0*&#x200B;在Y轴上左右滑动零件。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise2ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
