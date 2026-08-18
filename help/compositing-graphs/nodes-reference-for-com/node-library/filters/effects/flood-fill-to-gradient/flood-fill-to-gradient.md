---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: 使用“Flood Fill到渐变”节点，用渐变值填充区域，以创建平滑的颜色过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渐变Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# 渐变Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## 渐变Flood Fill

**范围：** *滤镜/效果*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

将[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)基转换为（随机方向）渐变。 对于创建拼贴随机倾斜和倾斜的高度图非常有用。

## 参数

### 输入

* **Flood Fill**： *颜色输入*&#x200B;基本Flood Fill数据。
* **角度输入**： *灰度输入*\
  可选映射，用于确定每个单元格与外部映射的角度。
* **输入斜率**： *灰度输入*&#x200B;用于确定每个单元格渐变斜率强度的可选映射。

### *参数*

* **角度**： *0.0 - 1.0*&#x200B;为所有拼贴设置统一的全局角度/方向。
* **角度变化**： *0.0 - 1.0*&#x200B;分别随机分布每个拼贴的角度。 这是最有用且最强大的参数！
* **乘以定界框大小**： *0.0 - 1.0*&#x200B;按拼贴单个定界框大小缩放整个线性效果。 这意味着较小的拼贴最终会比较大的拼贴暗。
* **角度图像输入乘数**： *0.0 - 1.0*&#x200B;设置可选角度输入映射对生成的渐变方向的影响
* **斜率的图像输入乘数**： *0.0 - 1.0*\
  设置可选斜率输入映射对生成的渐变斜率强度的影响。
* **乘以斜率强度**： *0.0 - 1.0*
* **平面斜率颜色**： *（灰度值）*允许为平面斜率设置纯色值。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
