---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: 使用“斜面滤镜”节点在形状和图案上创建斜边以添加深度和维度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜面（滤镜节点）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# 斜面（滤镜节点）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## 斜面

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在输入灰度高图上执行边缘斜切效果。 基于该Heightmap返回斜面的Heightmap和Normalmap。

在理想二进制（高收缩黑白）的基本Heightmap上，这是应用精确曲线配置文件的一个有用的节点。

## 参数

### 输入

* **输入**： *灰度输入*\
  要转换的高度映射。
* **自定义曲线**： *灰度输入*\
  确定确切曲线/斜率的渐变。 理想情况下为渐变线性节点，您可以在其中执行任何类型的调整，如[色阶](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)或[曲线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)。 仅当“使用自定义曲线”为True时处于活动状态。

### 参数

* **距离**： *-1.0 - 1.0*&#x200B;斜角效果应达到的距离。
* **圆角类型**： *圆形，Angular*&#x200B;斜面配置文件是圆形还是直线。
* **平滑**： *0.0 - 5.0*&#x200B;在斜角后要额外执行多少平滑（模糊）。
* **使用非均匀模糊**： *False/True*&#x200B;是否应该以非均匀方式执行平滑处理。
* **使用自定义曲线**： *False/True*&#x200B;切换使用您自己的自定义Height曲线。 有关更多信息，请参阅上文。
* **正常强度**： *0.0 - 50.0*&#x200B;生成的正常映射的强度。
* **普通格式**： *DirectX，OpenGL*\
  在不同正常映射格式之间切换（反转绿色通道）。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
