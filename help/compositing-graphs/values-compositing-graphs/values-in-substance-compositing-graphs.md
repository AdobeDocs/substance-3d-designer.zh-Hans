---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/values-in-substance-compositing-graphs.html"
breadcrumb-title: ""
description: 了解Substance合成图形中的值类型和数据处理，以便有效地创建材料。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Values in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 图形中的值
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%
---

# Substance 图形中的值

自2019.1.0版引入[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)引擎v7以来，现在可以处理Substance图形中的值，而不仅仅是[函数](../../function-graphs/function-graphs.md)中的值。 数值数据与“函数”（整数、Float和布尔值等）中使用的数据相同，因而与“颜色”或“灰度图像”数据（表示整个图像的像素值）截然不同。 具体来说，在提及值数据时，这表示&#x200B;*整数1、整数2、整数3和整数4、Float1、Float2、Float3和Float4和布尔值*。 每种颜色都有不同的颜色编码，并且大多不会相互交换。

这有几种用法，例如：

* 返回并处理非图像数据，如单值材料属性或额外的元数据。 例如材料的IOR值。
* 优化不需要按像素计算的图形计算（[像素处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)的替代方法）。 例如，随机纯色。
* 通过将图像数据处理为值来链接一个节点的属性到另一个节点。 例如，要调整色阶的图像的最小值和最大值。

## 新的价值节点和输入

两个新原子节点与“值”配合使用：

|                                                                                                                                                                                                                                                                                                                                                                                                                                       |  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| --- |
| <div><img alt="值处理器节点图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="values-in-substance-compositing-graphs.resources/valueprocessor.png" title="值处理器节点图标" width="100px"/></div>  <b>[值处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)</b> | [值处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)采用任意数量的灰度或彩色输入，并允许您从基于这些输入的计算中返回单个值。 |
| <div><img alt="值输入节点图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="values-in-substance-compositing-graphs.resources/inputnumeric.png" title="值输入节点图标" width="100px"/></div>  **[输入值](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-value/input-value.md)** | [值输入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-value/input-value.md)允许您在明确定义为“值”的子图形上创建输入槽。 |

此外，其他节点以特定的方式处理它们：

如果将“值”连接插入输出节点[&#128279;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)，则输出节点会自动调整为值输出，就像之前使用“灰度”和“颜色”时一样。

![输出值节点](values-in-substance-compositing-graphs.resources/values-output.gif "输出值节点"){width="512px"}

每个节点（[原子](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)和[库](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)/实例）上都有一个新选项卡，可用于定义值输入。

![在节点上添加输入值](values-in-substance-compositing-graphs.resources/values-inputs.gif "在节点上添加输入值")

## 使用值

使用“值”与常规图形工作略有不同：

只能从[值处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)、[输入值](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-value/input-value.md)或[子图](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)建立值连接。 这实际上意味着，值处理器是从头开始创建值连接的唯一方法，没有“静态值”节点或任何类似节点。 而应创建值处理器，放置一个静态值，并将其设置为输出，以获得相同的结果。

值处理器只能返回单个值，如果要返回多个值，或者要返回值集或值组，则必须创建[子图](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)。

要突出显示公开值或使用值的位置，任何具有“值输入”或“值输出”的“节点”都将以粗黄色边框突出显示：

![使用值](values-in-substance-compositing-graphs.resources/yellowhighlight.png "使用值")
