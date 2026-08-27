---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中导入、创建和使用位图资源以创建基于纹理的材质。
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 位图资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# 位图资源

位图资源是Substance包中的资源。 它与[原子位图节点不同。 原子位图节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)是[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)内该位图的特定表示形式。

位图是Substance 3D Designer中最常见的一些非图形资源，其使用通常归入以下类别之一：

* 一个已烘焙贴图，[由Designer](../../bakers/bakers.md)内部烘焙，或者由另一个应用程序在外部烘焙。
* 辅助纹理，如图案、污渍地图或贴花。
* 用于混合的简单灰度蒙版，可以在内部使用[位图节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)创建，也可以使用外部应用程序创建。

## 位图存储

位图通常是Designer处理的最大的资源。 因此，您最好了解Designer如何处理这两个主要文件类型的文件。

### 在Substance 3D文件(SBS)中

位图在SBS中的存储方式取决于您是否[链接或导入这些位图，请确保您首先熟悉概念。](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) 可以使用[位图绘画工具](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)编辑导入的位图。

与SVG（矢量图形）资源不同，位图始终存储在外部，即使作为新资源创建或导入时也是如此。 对于新Substance包，它们会保留在内存中，直到.SBS文件保存到磁盘为止。 存储到磁盘后，位图将存储在SBS文件旁边的&#x200B;*/resources*&#x200B;文件夹中。

### 在Substance 3D资源中(SBSAR)

在[SBSAR文件](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中，嵌入了位图，这意味着位图对最终SBSAR文件大小有重大影响。 您可以在此页面上进一步了解对文件大小的影响。 发布SBSAR文件时，仅嵌入用于计算图形输出的位图。 任何未使用的位图都将得到优化并从最终SBSAR包中排除，而不会影响文件大小。

## 文件类型、颜色模式和分辨率

Substance 3D Designer可以轻松编辑和重新排列位图中的数据，但最好记住以下几点：

* 将分辨率设置为2的次幂兼容，这意味着遵循标准的实时纹理大小，如<b>256、512、1024、2048、</b>等。Designer会将超出此范围的纹理重新缩放到最接近的匹配分辨率。 请注意，它们不必是方形比例。
* 支持许多文件类型，但请选择最适合您的用例的文件类型。 <b>无损压缩甚至未压缩</b>文件类型（如PNG或TGA）的品质优于JPG或DDS。
* 确保<b>正确设置颜色模式</b>，具体取决于您需要的是彩色、灰度还是Alpha通道。

## 位图属性

包中的位图资源具有许多可以自定义的属性。 大多数属性没有主要用途，用于库过滤器，但少数属性会影响文件大小。

| 属性名称 | 目的 |
| --- | --- |
| 标识符 | 用于引用包中的位图资源，必须是唯一的。 |
| 文件路径 | 资源引用的位图的磁盘路径。 |
| 描述 | 此资源的[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)和[库](../../interface/the-library/the-library.md)工具提示中显示的说明。 |
| 类别 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 标签 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 作者 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 作者 URL | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 标记 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 用户数据 | 可选的额外数据，不用于位图。 |
| 在图库中显示 | 确定是否应在[库视图](../../interface/the-library/the-library.md)中隐藏位图。 |
| 位图格式 | 无论是Raw还是Jpeg，都对SBSAR文件的大小有着非常大的影响。 请参阅我们的[文件大小缩减准则](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)以了解详情。 |
| 位图压缩品质 | 仅对Jpeg压缩产生影响，决定品质/文件大小平衡。 |

## 减小文件大小

有关最小化嵌入到[已发布的Substance 3D资源(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中的位图的文件大小的建议，请参阅[最佳实践](../../best-practices/best-practices.md)部分中的[文件大小缩减准则](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)页。
