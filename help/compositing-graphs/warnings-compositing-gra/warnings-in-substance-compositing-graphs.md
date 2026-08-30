---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: 了解Substance合成图表中的警告，并了解如何解决常见问题和错误。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 图形中的警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---


# Substance 图形中的警告

此页面列出了Substance 3D Designer中的[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)可能触发的警告和错误消息，并且提供了针对每个警告和错误消息的常见故障排除步骤。

警告显示在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中图形资源的警告图标的工具提示中，如果加载了图形，则也会显示在[图形视图](../../interface/the-graph-view/the-graph-view.md)的左下角。

## ![（错误）](warnings-in-substance-compositing-graphs.resources/error.svg)未定义输出节点

图形没有[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。

**![（刻度）](warnings-in-substance-compositing-graphs.resources/check.svg)解决方案**

向图形添加一个或多个[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点，并将流中最后一个节点的输出连接到该节点。

>[!NOTE]
>
> 通过[新建图形](../creating-compositing-gra/creating-a-substance-compositing-graph.md)对话框可用的图形模板具有准备好使用的预设输出节点。

![修复“未定义输出节点”警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-output.gif "修复“未定义输出节点”警告"){width="512px"}

### ![（错误）](warnings-in-substance-compositing-graphs.resources/error.svg) *[x]*&#x200B;参数的函数有一些警告

应用于指定节点的指定参数的[函数图形](../../function-graphs/function-graphs.md)至少有一个警告。\
节点参数在节点标签后面的方括号之间指定，位于模板Node[Parameter]之后。

E.g. 均匀颜色[输出颜色]，像素处理器[每个像素函数]

**![（刻度）](warnings-in-substance-compositing-graphs.resources/check.svg)解决方案**

在[图形视图](../../interface/the-graph-view/the-graph-view.md)中按其标签和警告徽章找到发出警告的节点，然后选择它以在[属性](../../interface/properties/properties.md)面板中显示其属性。 找到发出警告的参数并通过单击&#x200B;**编辑函数**&#x200B;按钮打开其函数。

然后，评估图形视图左下角列出的警告并解决问题。 您可以参阅[函数图形中的警告](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md)页，以解决函数图形中报告的警告。

![修复“Parameter函数有一些警告”警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-param-function.gif "修复“Parameter函数有一些警告”警告")

### ![（错误）](warnings-in-substance-compositing-graphs.resources/error.svg)引用的数据有一些警告

节点引用的资源具有一个或多个警告。 以下是引用资源的一些节点：

* [图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)节点引用了图形
* [位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点引用[位图资源](../../resources/bitmap-resource/bitmap-resource.md)
* [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)节点引用[SVG资源](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [文本](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)节点引用[字体资源](../../resources/font-resource/font-resource.md)

**![（刻度）](warnings-in-substance-compositing-graphs.resources/check.svg)解决方案**

在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中，查找引用的资源，并解决该资源引发的所有警告：

* 有关图表，请参阅本页中的其他项目
* 有关任何其他类型的资源，请参阅[来自依赖项的警告](../../resources/warnings-from-dep/warnings-from-dependencies.md)页

![修复“引用的数据有一些警告”警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-data.gif "修复“引用的数据有一些警告”警告")

### ![（错误）](warnings-in-substance-compositing-graphs.resources/error.svg)未找到引用资源

在[Substance 3D](https://www.adobe.com/cn/products/substance3d/3d-augmented-reality.html)文件(SBS)中保存的路径中找不到节点引用的资源。 以下是引用资源的一些节点：

* [图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)节点引用了图形
* [位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点引用[位图资源](../../resources/bitmap-resource/bitmap-resource.md)
* [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)节点引用[SVG资源](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [文本](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)节点引用[字体资源](../../resources/font-resource/font-resource.md)

**![（刻度）](warnings-in-substance-compositing-graphs.resources/check.svg)解决方案**

对于[图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)节点

检查源图形是否存在于包中，该包位于保存在其&#x200B;**包**&#x200B;属性中的路径中。\
否则，请删除该实例节点，并将其替换为引用有效包的实例节点。 或者，您可以重新创建实例节点引用的包和图形，然后通过在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中单击主机包上的RMB并在上下文菜单中选择&#x200B;**重新加载**&#x200B;选项来重新加载该主机包。

对于[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)、[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)或[文本](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)节点

在“资源管理器”面板中查找引用的资源，并检查这些资源存在于保存在其&#x200B;**文件路径**&#x200B;属性中的位置。\
否则，请单击资源管理器中的资源项上的RMB，然后在上下文菜单中选择&#x200B;**重新定位……**&#x200B;选项，以设置该资源的新有效目标文件。

![修复“未找到引用资源”警告](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-resource.gif "修复“未找到引用资源”警告")

### ![（错误）](warnings-in-substance-compositing-graphs.resources/error.svg)文本节点使用了无效的字体

[Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)节点引用了无法加载或无法正确分析的字体。

<b>！[(tick)](warnings-in-substance-compositing-graphs.resources/check.svg)解决方案</b>

选择[文本](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)节点并记下其<b>字体</b>属性的值。 在系统上查找该字体的源文件，并确保其&#x200B;*正常*，例如，在其他应用程序（如文本编辑器）中使用它。 根据需要使用正常字体文件替换字体，或将“文本”节点切换到其他字体。
