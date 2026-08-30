---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/publishing-substance-3d-asset-files-sbsar.html"
breadcrumb-title: ''
description: 了解如何从Designer发布Substance 3D资源文件(SBSAR)，以便在其他应用程序和引擎中使用。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Publishing Substance 3D asset files (SBSAR)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 发布 Substance 3D 资源文件 (SBSAR)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9505c371dff25c5d32a409abf76b95655b499571
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 2%

---


# 发布 Substance 3D 资源文件 (SBSAR)

此页面介绍了Substance 3D Designer如何将包发布为<b>Substance 3D资源</b>文件，这是一种扩展名为<b>SBSAR</b>的特殊文件格式，在Substance生态系统以及支持该格式的其他应用程序中使用。

通常最好使用Substance 3D资源而不是位图，因为它要灵活得多，重量也轻得多。 如果您在Substance 3D [Painter](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/home)、[Sampler](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-sampler/using/home)或[Player](https://helpx.adobe.com/substance-3d-player/home.html)中使用它们，则使用[“发送到……”功能](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)更快。

![简化了发布SBSAR文件](publishing-substance-3d-asset-files-sbsar.resources/exportflow.png "简化了发布SBSAR文件")

## 发布概念

发布图形时，最好记住以下几点：

* 您<b>发布包</b>，其中包含所有内容，而不是单个[图形](../../compositing-graphs/substance-compositing-graphs.md)。 然后，您可以使用Substance 3D资源从此包内的所有Substance图形生成内容。
* 已发布的包<b>完全独立</b>：所需的所有资源都嵌入到文件中。 这意味着它们比SBS文件更易于共享。
* Substance 3D Assets的输出可以<b>完全动态</b>。 [未设置分辨率；可以修改公开参数。](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) 但是，无法再编辑图形。
* 可在Designer之外、所有Adobe的Substance 3D产品、Adobe Dimension以及任何其他具有[Substance集成](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/ecosystem/home)的应用程序中使用Substance 3D资源。
* 发布与[导出](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)不同，请确保您充分理解其中的区别。

## 正在准备发布

发布比导出位图需要更多的准备。 这是因为您发布的Substance 3D资源是动态工具，而不仅仅是纹理当前状态的静态快照。 具体来说，您需要牢记以下事项：

* 确保将图形分辨率（[输出大小](../../compositing-graphs/output-size/output-size.md)）设置为&#x200B;*相对于父代* [继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，这意味着它们是动态的，可以动态更改。
* 确保使用名称、标签和使用标签正确设置[图形输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。
* 确保[参数（如果需要）已正确组织和命名](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)。
* 如果图形描述素材，请将其[材质模型](../graph-parameters/graph-parameters.md)属性设置为该素材的模型。
* 确保所有[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点的[输出大小](../../compositing-graphs/output-size/output-size.md)属性都设置为&#x200B;*绝对* [继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。 否则，它们引用的[位图资源](../../resources/bitmap-resource/bitmap-resource.md)将以默认的<b>256\*256</b>分辨率保存在已发布的Substance 3D资源文件中，这将*&#x200B;影响一个或多个输出的质量*。
* 如果包中存在不应在Designer外部提供的图形（例如，仅在特定上下文中工作的helper或“tool”子图形），请将其设置为在其属性中隐藏。 详情见下文。

## 发布方法

准备好发布后，有两种方法可访问发布对话框，两种方法都是通过[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)实现的。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

在资源管理器中，右键单击包并选择![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-9-39-58.png) **Publish .sbsar 文件...**，备用热键Ctrl + P。

通过对话框发布一次后，您还可以使用![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-11-15-35.png) **Publish .sbsar 文件作为早期版本**&#x200B;重复发布过程，而不看到对话框，而立即使用相同的设置发布。

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publish-rightclick.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

在资源管理器中，单击顶部工具栏中的“Publish”按钮![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-9-39-58.png)。

通过对话框发布一次后，您还可以使用“Publish”作为上一个按钮![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-11-15-35.png)重复发布过程，而不看到对话框，而立即使用相同的设置发布。

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publish-toolbutton.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 资源发布选项

在“资源Publish选项”出现之前，如果尚未保存Substance 3D文件(SBS)，系统将提示您保存位置，并提示您保存Substance 3D资源。 要避免看到文件提示和对话框并更快地导出文件，请使用<b>Publish作为上述</b>方法。

</td>
<td style="border: 0;" valign="top">

![资源发布选项](publishing-substance-3d-asset-files-sbsar.resources/publish-dialog.png "资源发布选项")

</td>
</tr>
</table>

您可以选择以下选项：

<b>文件路径</b>将打开一个文件对话框以选择保存Substance 3D资源文件的位置。 默认路径是系统的用户文档。 如果保存了包，则路径为包位置。 如果包已在会话期间发布，则路径为最后一个发布位置。

<b>存档文件压缩</b>设置存档文件的压缩选项，影响文件大小。

<b>生成缺少的图标</b>使用内置[PBR 渲染](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)技术为每个图表的属性创建缩略图。

<b>公开图形</b>列出此包中将公开的所有图形，有关排除图形的信息，请参阅下文。

>[!NOTE]
>
> **随机种子曝光**
> 
> Publish对话框中不再提供“随机种子曝光”设置。 而是将[图表的随机种子属性设置为“绝对”而不是“相对”，以避免它变为可用。](../../compositing-graphs/graph-parameters/graph-parameters.md)

## 从已发布资源中排除图形

包中的某些图形可能不适用于外部。 这些子图通常作为大型整体的一部分，而大型整体是主材质的子程序。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

要排除某个图形使其在Substance 3D资源文件中不可见或可用，请访问该图形的属性（双击图形视图中的空白区域或在Explorer中单击该图形），然后打开<b>属性</b>转出。 将<b>在SBSAR</b>中公开<b>否</b>设置为在发布时隐藏它。

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-10-40-21.png)

</td>
</tr>
</table>

### Publish对话框警告

Publish对话框有时会发出黄色警告。 下面列出了常见问题，并提供了相关说明和解决方案。

* 一个或多个图形没有输出\
  此警告表示您正在尝试发布包含一个或多个没有输出节点的图形的包。 解决方案是向图表添加[输出节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)，并添加一个黄色警告三角形。
* 一个或多个图形具有与父输出尺寸无关的参数\
  此警告表示一个或多个图形已设置为不正确的输出大小。 通常，它是指图形本身的属性。 此警告表示在发布时您对此图表没有动态分辨率控制。 解决方案是进入黄色三角形的图形属性，并将输出大小的[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)设置为&#x200B;*相对于父级*。

## Substance 3D资源限制

虽然Substance 3D资源是Substance生态系统中功能最强大、最动态的格式，但需要注意一些较小的技术限制。

* 发布的Substance 3D资源包是单向文件格式。 无法将Substance 3D资源“反编译”回Substance 3D文件(SBS)。 “编辑”Substance 3D资源的唯一方法是编辑原始Substance 3D文件。 您仍可以将Substance 3D资源包内容用作新Substance图表内的节点（打开并拖放），因此这并非一个巨大的限制。
* Substance 3D资源文件具有推断兼容性的版本。 核心Substance 引擎会不时通过新增功能进行更新。 使用这些功能的包需要由支持这些新功能的应用程序读取。 这不是所有Substance应用程序的问题，因为它们会同时更新，但增效工具和集成可能会产生更长的兼容性延迟。\
  使用[项目首选项](../../interface/preferences-window/project-settings/project-settings.md)中的Substance 引擎兼容性显示选项来跟踪任何潜在问题。
* 将图形作为Substance 3D资源的一部分发布后，某些公开的参数（如&#x200B;*静态*&#x200B;参数）将&#x200B;*隐藏*。 有关这些参数的列表，请参阅[公开参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)页的[限制](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)部分，并了解有关静态参数的详细信息。
