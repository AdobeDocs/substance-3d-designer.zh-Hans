---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: 使用马赛克节点通过将纹理分为像素化的块和图案来创建马赛克拼贴效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 马赛克
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# 马赛克

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mosaic-1.png){width="128px"}

![](../../../../../../assets/mosaic-grayscale.png){width="128px"}

## 马赛克（灰度）

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

通过执行多程[变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)效果来“刻画”现有、平滑、倾斜的渐变映射。 当对两个输入使用同一地图时，它实际上会增长并突出最亮的区域。

这对于为灰度图（如Heightmap）添加更多定义非常有用，因为它可以增加形状的定义。

## 参数

### 输入

* **颜色**： *彩色/灰度输入*
* **马赛克地图**： *灰度输入*\
  变形驱动程序映射。 可以与第一个输入项相同。

### 参数

* **取样**： *0 - 16*&#x200B;确定多取样品质。
* **强度**： *0.0 - 1.0*&#x200B;效果的强度。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mosaci-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
