---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ""
description: 使用SVG节点将SVG矢量图形作为创建可缩放图形元素的纹理导入和渲染。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---

# SVG

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子节点：SVG](svg.resources/comp_svg_1.png "原子节点：SVG"){width="100%"}

<b>进入：</b>个原子节点

</td>
<td style="border: 0;" valign="top">

将[SVG图像](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)渲染为位图。 换句话说，将矢量形状映射到像素。

创建此节点有几种方法，所有这些方法都需要您了解[链接和导入资源之间的区别](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="svg.resources/svg-tooltip.gif" alt="svg工具提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

您可以从头开始创建节点，也可以将SVG文件放到图形视图中。


>[!TIP]
>
> 可以使用[2D 视图](../../../../interface/2d-view/2d-view.md)停靠栏中的[矢量编辑工具](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)来编辑生成或导入的SVG图像。

>[!IMPORTANT]
>
> 此节点依赖于外部资源，因此在使用它们时需要注意以下几点：
> 
> * SVG节点可以返回彩色或灰度，但即使资源是灰度矢量，颜色节点也默认为彩色。 这可能会影响图形性能和复杂性，因此请始终确保根据需要切换到“灰度”[颜色模式](#parameters)。
> * 删除SVG节点不会删除[包](../../../../glossary/glossary.md)中的[SVG资源](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)，您必须在[资源管理器](../../../../interface/the-explorer-window/the-explorer-window.md)中手动执行此操作。
> * SVG形状[网格化](../../../../glossary/glossary.md)为几何/多边形，然后&#x200B;*栅格化*，以便在Substance图形中用作位图。 用于这些操作的技术不支持多个矢量属性，如轮廓。 在[此处](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)了解有关这些限制的更多信息。

>[!WARNING]
>
> SVG形状[网格化](../../../../glossary/glossary.md)为几何/多边形，然后&#x200B;*栅格化*，以便在Substance图形中用作位图。
> 
> 用于这些操作的技术不支持多个矢量属性，如轮廓。
> 
> 在[此处](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)了解有关这些限制的更多信息。


## 参数

|  |  |
| --- | --- |
| <b>颜色模式</b> *布尔值* | 确定节点的输出类型，以返回彩色或灰度。 |
| <b>背景颜色</b> *彩色/灰度* | 设置要在矢量形状未覆盖的区域中使用的输出图像的背景色。   *在连接该输入时被“[Background](#inputs)”输入覆盖。* |
| <b>PKG资源路径</b> *字符串* | 指向节点正在引用的[SVG资源](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)的路径。   建议不要手动键入，而是从资源管理器中复制资源并将其粘贴到参数文本字段中，或者将位图资源直接从[资源管理器](../../../../interface/the-explorer-window/the-explorer-window.md)拖放到图形中的SVG节点上。 |

## 矢量编辑工具

可以在Designer中编辑矢量形状。 了解有关[此部分](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)中编辑工具的更多信息。

## 输入连接器

|  |  |
| --- | --- |
| <b>背景</b> *灰度/颜色*&#x200B;主要 | 设置要在矢量形状未覆盖的区域中使用的输出图像的背景色。   *连接时覆盖“[背景颜色](#parameters)”参数。* |


## 示例

*即将推出。*
