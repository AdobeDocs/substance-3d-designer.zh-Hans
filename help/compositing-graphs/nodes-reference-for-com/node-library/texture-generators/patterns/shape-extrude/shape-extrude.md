---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: 使用“形状凸出”节点在Substance 3D Designer纹理中凸出形状并创建类似3D的深度效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状凸出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# 形状凸出

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## 形状凸出

**英寸：** *纹理生成器**/Patterns*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

一个高级节点，允许将2d二进制“形状”输入渲染为3D旋转的高图。 其工作方式与3D包中的凸出类似，沿其轴凸出形状，从而创建体积块。 结合使用轮廓渐变蒙版，还可以创建旋转/车床类型主体。 对于为高地图创建复杂的人工形状非常有用。

## 参数

### 输入

* **凸出形状输入**： *灰度输入*&#x200B;如果凸出形状设置为“自定义”，请在此处插入您自己的（最好是）二进制形状蒙版。
* **配置文件渐变**： *灰度输入\
  如果“截面梁类型”设置为“垂直渐变”，则可用于定义旋转主体的形状沿轴的比例。*
* **配置文件蒙版**： *灰度输入*\
  用于沿凸出形状的轴隐藏或显示凸出形状的蒙版槽。 可用于中断形状沿其轴的连续性。 仅解释为二进制：灰度put值四舍五入为0或1。

### 参数

* **凸出Height**： *0.0 -* 1.0\
  从中心向上拉伸形状的量。
* **凸出深度**： *0.0 - 1.0*&#x200B;从中心向下凸出形状的量。
* **凸出形状**： *立方体、圆柱体、自定输入*&#x200B;使用内置形状或在外部输入您自己的自定形状。
* **凸出形状大小**： *0.0 - 1.0*&#x200B;仅用于内置立方体和圆柱体，确定基本形状大小，可以缩放为非均匀形状。
* **缩放**： *0.0 - 1.0*\
  设置效果的全局比例。 对于内置形状，这是统一的基本形状比例，不影响Height或深度。\
  使用“自定义输入”时，这会以统一的方式缩放整个最终结果。
* **配置文件类型**：*直线、垂直渐变、蒙版*&#x200B;用于确定效果行为和使用可选额外输入映射的主控件。\
  “直接”是标准的凸出行为，“垂直渐变”允许沿整个轴自定义缩放值，“蒙版”允许通过蒙版隐藏沿轴的部分。
* **斜角Height**： *0.0 - 1.0*&#x200B;设置斜角沿凸出轴到达的距离。
* **斜角强度**： *0.0 - 1.0*&#x200B;设置斜角从原始形状缩进的程度。
* **斜角曲线**： *-1.0 - 1.0*&#x200B;设置斜角效果的凸曲线或凹曲线。 值为0表示直线，无曲线。
* **镜像斜角**： *False/True*&#x200B;切换以在形状的顶部和底部应用斜角。
* **降阶多倍器**： *0 - 2*&#x200B;内置的简化降阶控制功能。 可用于快速添加消除锯齿功能；请确保也提高节点分辨率。
* **位置**：\
  旋转的主控件导致3D空间。 在2D视图中与intervatice Gizmo关联。
* **输出范围**： *[0， 1]， [-1， 1]*设置输出最小值和最大值。 如果range设置为[-1,1]，则负值显示为黑色。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
