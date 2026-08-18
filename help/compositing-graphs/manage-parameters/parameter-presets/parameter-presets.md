---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中创建和使用参数预设来保存和应用参数配置。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 参数预设
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---


# 参数预设

参数预设使用户能够存储和传输一组参数的大量预配置值。它们在许多情况下都有帮助，并且在存在大量带有多种可能性的参数时最有用。

存储和加载预设有两种方法，这两种方法都有不同的用例，详见下文。

![加载/保存预设下拉菜单](../../../assets/preset-menu.gif "加载/保存预设下拉菜单"){width="512px"}

## 外部预设

外部预设涉及磁盘上的外部文件，即\*.SBSPRS文件。 它们可以在不同的图形和节点之间传输，但只能在应用程序内传输。 它们的主要目的正是这样的：转移大量值，无法逐个复制。

外部预设适用于[图形实例](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)上的所有特定参数、[原子节点](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)上的大多数特定参数（[例外是那些无法公开的参数](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)）以及[图形属性](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)中公开的输入参数。

它们通过此菜单简单保存和加载。 保存的SBSPRS文件可以加载到任何其他节点或图形上。

>[!NOTE]
>
> 即使部分匹配也会起作用：存储在加载的节点上不存在的SBSPRS中的参数将被忽略。 这意味着您可以在基本相似的节点之间转移属性，[，例如平铺Sampler的彩色和灰度版本](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)！ 将加载所有共享参数。 标识符和类型匹配。

![嵌入的预设编辑](../../../assets/preset-embed.gif "嵌入的预设编辑"){width="512px"}

## 嵌入的预设

嵌入预设的工作方式与外部预设不同。 它们的主要优点是包含在SBS或SBSAR文件中，因此可以在Substance Painter、Maya和3DS Max中轻松传输和加载它们（目前在Substance 3D Sampler、UE4和Unity中不可用）。 用户也不必乱用SBSPRS文件。

它们具有不同的用途：无法在节点和图形之间传输它们（为此，必须使用外部预设）。 也只能在“图形属性”的“输入参数”上创建预览模式。

工作流程如下：

1. 为<b>输入参数</b>切换到<b>预览模式</b>
1. 将值设置为所需的结果
1. 单击预设下拉列表旁边的<b>+</b>以创建新的嵌入预设，然后会立即创建并存储预设

嵌入的预设之后无法修改，但可以重命名。 单击下拉菜单旁边的齿轮图标和+图标，即可修改和删除它们。 按预设旁边的减号可将其移除。

无需执行其他操作即可启用预设：发布为SBSAR后，导入后即可在Substance Painter中使用您的预设。

>[!IMPORTANT]
>
> 使用[上下文编辑](../../../interface/preferences-window/preferences-window.md)时，<b>预设</b>选项卡处于禁用状态。
