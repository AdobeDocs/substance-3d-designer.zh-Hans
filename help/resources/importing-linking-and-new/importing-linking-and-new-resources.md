---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中为您的素材项目导入、链接和创建新资源。
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导入、链接和新资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 2%

---


# 导入、链接和新资源

[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)支持3种导入或创建新资源以在图表中使用的模式。 这些资源可以是许多不同类型的资源，包括但不限于[位图](../../resources/bitmap-resource/bitmap-resource.md)、[矢量图形](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)、[3D场景](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)和[字体](../../resources/font-resource/font-resource.md)。 本页介绍各种方法以及每种方法的最佳使用时机。

通过在资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)[中单击包上的RMB [，可以访问所有方法。](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)

下表简要概述了这两种方法的功能差异。

|                                                                                                                                                                         | 新建 | 导入 | 链接 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| 图表([Substance的图表](../../compositing-graphs/substance-compositing-graphs.md)，[Substance的函数图表](../../function-graphs/function-graphs.md) | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| [位图](../../resources/bitmap-resource/bitmap-resource.md)，[矢量图形(SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| [3D场景](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)，[字体](../../resources/font-resource/font-resource.md) | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 在SBS文件旁边创建 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 可在Designer中编辑 | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 自动同步外部编辑 | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（错误）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 嵌入已发布的SBSAR | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（刻度）" data-preserve-html="true" src="../../assets/check.svg"/></div> |

## 新资源

创建新资源意味着将从头开始创建包中的资源。 所有仅限Designer的资源只能通过这种方式创建，例如Substance图表和Substance函数图表。

创建新的[位图](../../resources/bitmap-resource/bitmap-resource.md)或[SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)时会出现一个特殊情况：这些文件将显示在资源管理器中，其行为类似于导入的资源，但不需要外部文件。 可在Designer中修改它们。 当您不需要依赖外部编辑器时（例如，当您只需要快速且简单的矢量形状或简单的绘制2D位图蒙版时），用这种方法创建的新位图和SVG就很棒。

## 导入的资源

导入资源意味着将在您的SBS文件（在&#x200B;*图形名称*.resources文件夹中）旁边创建资源文件的副本，但SVG文件](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)除外。 [它有时也称为“嵌入的”资源。

导入的资源放入图形后，即可在Designer中使用[2D视图](../../interface/2d-view/2d-view.md)中的[位图绘画工具](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)或[矢量编辑工具](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)进行编辑。 导入的资源不再链接到其原始源文件：这意味着如果您更改、删除或更新最初导入的文件，则这对Designer中的资源没有影响。

对于[AxF文件](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)，此过程会更加复杂；Substance图形和位图资源是从AxF包创建的。 但是，所有这些文档仍然可以在各自的编辑器中编辑：“图形”视图或2D视图。

>[!WARNING]
>
> 对于新包，在保存包之前，导入资源和新资源不会保存到磁盘上。

## 链接的资源

链接资源意味着Designer将引用磁盘上其原始位置的源文件，但仍将该文件作为包的一部分存在于资源管理器中。 您将无法直接在Designer中编辑实际资源，只能将其用作图表中的组件或作为生成地图的源。

如果您知道在Designer中同时工作时，需要使用外部编辑器更新资源，则适合使用链接。 烘焙图是一个主要示例：您可以让Designer参考位图形成外部烘焙应用程序，该应用程序将在更改这些文件时自动重新加载和更新图形。 同样，3D场景只能链接，因此每次从3D应用程序导出新的FBX文件时，Designer都会自动更新3D视图中使用的网格。 如果要从此网格中绘制地图，您必须手动重新开始绘制过程，最好是单击“人民币”并选择“刷新所有已烘焙贴图”。

## 正在删除资源

从包中删除资源时，将显示<b>确认项删除</b>对话框。 如果正在移除的任何项被&#x200B;*其他资源引用* — 如[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)中使用的[图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)和[位图资源](../../resources/bitmap-resource/bitmap-resource.md) — 则对话框将包括这些项中的&#x200B;*警告和列表*。

>[!NOTE]
>
> 我们建议注意这些项目，并采取必要的操作以&#x200B;*预测因从包中删除项目而造成的任何依赖关系损坏*。\
> 这些操作包括&#x200B;*删除这些资源的所有使用者*。

![“正在使用的已删除资源”警告](../../assets/confirm-item-removal.png "“正在使用的已删除资源”警告"){width="512px"}
