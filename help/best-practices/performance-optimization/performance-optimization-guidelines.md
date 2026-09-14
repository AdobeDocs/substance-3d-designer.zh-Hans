---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer的性能优化准则，以提高图形性能并减少处理时间。
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 性能优化准则
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---


# 性能优化准则

## Substance 图形

[Substance图表](../../compositing-graphs/substance-compositing-graphs.md)越复杂，渲染它们所需的处理能力就越强。 您应尝试<b>在复杂性和渲染速度之间找到平衡</b>。\
如果您将在实时图形应用程序（如游戏）中使用它们，则这是&#x200B;*尤其是*&#x200B;重要信息。

一般来说，公开自定义参数（可在运行时修改）的节点<b>应尽可能靠近图表的末尾</b>。

这是因为每个节点的输出会尽可能进行缓存。 因此，可补间节点在图形上的位置越靠上，只要修改这些公开参数中的一个，就需要处理更多的输出。 如果公开节点靠近图形的末尾，则只需重新计算它与输出节点之间的少数节点。

例如，如果在图形的开头微调统一颜色，则将重新计算以下所有节点。 如果微调输出前放置的HSL节点，则只有此节点会被重新计算，从而大大提高图形的性能。

请注意以下准则：

### 常规性能相关设置

+++GPU引擎比CPU引擎快得多
除非您拥有不受支持的（集成）图形卡，否则请使用GPU Substance引擎（通过热键F9更改）。

+++

+++切换图表的父分辨率时速度缓慢
它重新计算图形、缓存和所有缩略图。 最好使用[导出对话框的<b>“批处理”</b>](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)选项卡，因为它可避免大量不必要的重新计算（例如，导出为8192分辨率时）。

+++

+++在极端情况下，可能需要增加内存缓存
应用程序[限制可用于图像缓存的RAM量](../../interface/preferences-window/preferences-window.md)，但您可以覆盖并增加此值（请小心）。

+++

### 图优化

+++请注意节点解析度和一般继承！
较高的值将严重影响性能，因此请考虑可能如何使用素材以及是否可以减小涉及的数据大小。

我们建议您进一步了解[节点分辨率（输出大小）](../../compositing-graphs/output-size/output-size.md)和[Substance图表的继承](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。

+++

+++当不需要颜色时使用灰度
颜色操作比灰度操作耗时四倍。 此外，请尝试最大限度地减少颜色和灰度之间的类型转换。

+++

+++当不需要16位时使用8位
Substance 引擎(SSE2) *的CPU版本*&#x200B;实际上不支持16位颜色或8位灰度。 GPU引擎支持所有4种8/16位和灰度/彩色组合。 *目前，在Unity和虚构引擎增效工具中仅使用CPU引擎*。

+++

+++尽可能最小化节点输出大小
有时，缩减某些节点的规模不会影响最终结果，但会影响性能。 例如，使用设置为与文档相同的输出大小的统一颜色节点是没有意义的：统一颜色应设置为“绝对[16px x 16px]”，后续节点设置为“相对于父代”。 通常，这种技巧适用于低频图像，如Perlin噪声。

+++

+++请勿使用小于16*16像素的图像
这会降低渲染性能。

+++

+++使用混合节点时，在不需要时禁用Alpha 值混合处理


+++

+++模糊和变形是最消耗处理器资源的节点


+++

+++某些噪声生成器受绘制的图案数量影响
例如，[Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)节点处理添加到它的更多模式的速度将变慢。

+++

+++某些噪声受比例因子的影响
事实上，这个因素会形成更多模式。 受影响的节点包括噪声、细胞模式等。如果需要白色噪声图案，请不要使用具有非常高缩放值的噪声，而应使用[白色噪声](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md)或[白色噪声快速](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md)节点。

+++

+++相反，有一些非常快速的噪声生成器
其中包括[白噪声快速](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md)、[分形求和基](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md)和[各向异性噪声](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md)。

+++

+++在某些情况下使用大量的图像采样功能时需要注意
在CPU引擎上执行函数，但[像素处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)中除外。 如果您在[值处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)或[FXmaps](../../function-graphs/fxmaps/fxmaps.md)中执行大量大量图像取样（更改$pos坐标），则在VRAM和CPU RAM之间可能会进行大量交换，从而导致性能延迟。

+++

### 针对移动设备的使用优化

+++建议不要使用变形和FX映射
它们的性能非常昂贵。

+++

+++避免模糊节点
请改用缩减变换功能。

+++

+++尽量使用灰度
在图形末尾切换到彩色模式。

+++

+++在输出之间尽可能共享节点


+++

### 针对嵌入位图的大小优化

默认情况下，[位图](../../resources/bitmap-resource/bitmap-resource.md)的[输出大小](../../compositing-graphs/output-size/output-size.md)设置为[“绝对”](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。 这意味着，如果位图通过节点链连接到输出，它将强制最终输出为嵌入位图的大小。\
在位图之后插入的节点的输出大小将设置为[“相对于输入”](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。 这意味着节点本身也会具有位图的大小，并将此大小沿节点链向下传递到输出。 若要更正此问题，您需要将位图后面的节点设置为将其“输出大小”设置为[“相对于父代”](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。

如果将图形设置为具有动态分辨率，则可以将嵌入位图上的“输出大小”更改为相对于父代。\
这样，位图大小将根据父图形进行更改，您不会遇到图形处理比所需分辨率更高的位图分辨率的情况。

>[!WARNING]
>
> 将[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点设置为“相对于父代”并将[发布](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)图形到Substance 3D资源(SBSAR)将以&#x200B;**256x256**&#x200B;的分辨率保存位图，而不是其原始大小。 建议将Bitmap nodes的[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)“[输出大小](../../compositing-graphs/output-size/output-size.md)”保留为“绝对”，并在Bitmap node之后使用设置为“相对于父代”的[变换 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)节点。

![嵌入的位图优化1](performance-optimization-guidelines.resources/input-1.jpg "嵌入的位图优化1")

![嵌入式位图优化2](performance-optimization-guidelines.resources/relativetoparent.jpg "嵌入式位图优化2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

此外，建议将位图资源的格式设置为Jpeg，以最大限度地减少发布的Substance 3D资源(SBSAR)的大小。

</td>
<td style="border: 0;" valign="top">

![嵌入的位图优化3](performance-optimization-guidelines.resources/format.jpg "嵌入的位图优化3")

</td>
</tr>
</table>
