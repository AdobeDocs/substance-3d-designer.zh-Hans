---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: 使用边缘检测节点检测纹理的边缘，以创建轮廓和基于边缘的蒙版效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘检测
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# 边缘检测

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## 边缘检测

**范围：** *滤镜/效果*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

检测黑白图像中的对比度，然后创建黑白蒙版以突出显示对比度。

适用于需要边缘某种蒙版的许多情况。 请记住，它最适合用于高对比度输入；如果需要，在传递到此节点之前调整对比度。

## 参数

* **边缘宽度**： *1.0 - 16.0*&#x200B;边缘周围检测到的区域的宽度。
* **边缘圆度**： *0.0 - 16.0*&#x200B;对生成的蒙版进行圆化、模糊和平滑处理。
* **反转**： *False/True*\
  反转结果。
* **容差**： *0.0 - 1.0*&#x200B;用于边缘应显示位置的容差阈值因子。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
