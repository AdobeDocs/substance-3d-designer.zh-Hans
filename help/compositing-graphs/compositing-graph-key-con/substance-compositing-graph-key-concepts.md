---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ""
description: 了解Substance合成图形的关键概念，包括节点、连接和工作流程基础知识。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 图形关键概念
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%
---

# Substance 图形关键概念

本页列出了在Substance 3D Designer中使用Substance图形时需要了解的重要概念。

## 子图形/发布

[发布图形](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)或创建子图形是两个非常相似的抽象概念。 这意味着，任何图形或节点网络都可以“打包”在一起，变成一个可重复使用、独立的资源。 创建[子图形](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)主要在应用程序内完成，以便以高效、智能的工作流程重复使用某些内容，因为这可避免反复复制一组节点。 发布涉及一个额外的步骤来导出为Substance 3D资源(SBSAR)格式，使您的Node网络图形可在应用程序外部使用，例如在为Unreal引擎创建材料时。

输入、输出和公开参数对于这一概念极为重要，因为它们是将图形用作子图形或用作已发布的Substance 3D资源后仍与其交互的唯一方式。 原因如下：

* 没有输出将意味着您的图形<b>不生成任何数据，</b>没有任何数据。
* 没有公开参数表示无法以任何方式自定义图形<b></b>。 您将无法设置效果的强度、要混合的图像的不透明度、特定区域的颜色等事项。
* 无输入意味着在某些情况下，您将无法使用<b>自己的图像数据</b>自定义图形的结果，例如从中生成效果的烘焙网格图、执行模糊的输入图像或用于隔离图像特定区域的自定义蒙版。

## 输入和输出

[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)是生成单个2D结果的节点。 它是终结点，是您图形的终结点，是最终结果。 只能将连接到输出的数据导出到Designer外部，甚至可以在其他图形中使用。

关于输出，您应该了解以下几点：

* 您可以拥有任意多个输出，但必须拥有<b>至少一个输出</b>。
* 输出可以是<b>任何分辨率</b>，宽度或高度最大为8192px，颜色或灰度可以是<b></b>，并且可以导出为任何支持的文件类型。
* 输出可以且应该是<b>唯一命名</b>以标识它们，在导出时很有帮助。
* 任何连接器右侧的每个节点实际上都是一个输出（有关更多信息，请参见“子图形”）

[输入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md)类似于输出，它是一个空的开放插槽，可供您或其他用户将您自己的数据连接到。 它允许创建外部用户定义的图像数据中的图形，如修改输入图像的滤镜（如模糊或对比度调整）。

关于输入，您应了解以下几点：

* 输入完全是<b>可选的</b>，您应该仅在需要时添加它们。 没有最小或最大金额。
* 输入具有您定义的设置分辨率（通常链接到图表），以及它们是灰度还是彩色。 与之关联的任何内容都将转换为匹配此项。
* 输入可以是来自硬盘的位图文件、其他图形、来自Painter或Alchemist的图层等。
* 任何节点左侧的每个连接器都是一个“输入”（有关更多信息，请参阅“子图表”）

## 继承

当图像和值从节点传递到其他图像时，这些图像中的某些&#x200B;*属性*（即其<b>基本参数</b>）也将在图形中&#x200B;*传播*，例如分辨率、精度（即位深度）、拼贴和随机植入。

此传播由[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)定义，每个节点都应用于这些属性。 实际上，节点可以&#x200B;*继承来自其他节点或它们所在图表的属性*。\
继承方法可以是：

* *相对于主页*
* *相对于输入*
* *绝对* — 即无继承

继承可能很抽象并且难以管理，因此我们强烈建议您查看[专用页面](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)来详细讨论它。

## 公开参数

公开参数是一个非常深入的概念，但可以概括为选择图表中节点的特定属性，并为它们创建专用的UI控制元素，一旦将图表用作子图或将其发布为存档，即可轻松使用该元素。 因为无法再快速或轻松地选择节点并调整其属性，所以目标是创建另一个主控制面板，将与此特定图形相关的任何和所有属性分组。

关于公开参数，您应该了解以下几点：

* 公开参数<b>将控件从节点移动到图形</b>，实质上是在层次结构中的上一层。
* 因此，无法再更改节点上的公开参数，只能更改图形上的公开参数。
* 公开参数可使用名称、标签、值、UI编辑器类型进行完全自定义，在某些情况下甚至可隐藏和显示。

对于初学者来说，公开参数是一个抽象而困难的概念，[关于此主题的专用文档较多](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)，但建议在深入了解“公开参数”之前，先充分熟悉软件的其他基本方面。
