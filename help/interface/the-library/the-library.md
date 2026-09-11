---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/the-library.html"
breadcrumb-title: ''
description: 使用Substance 3D Designer中的库访问和管理节点预设、素材和自定义内容。
helpx_creative_field: ""
helpx_description: Designer > Interface > Library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 库
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---


# 库

此页面显示Substance 3D Designer的&#x200B;**库**&#x200B;面板、其布局以及它提供的用于搜索和筛选内容的工具。

![库](../../assets/library-main.png "库")

## 概述

<b>库</b>面板是一个拆分视图&#x200B;*资源管理器*，您可以在其中查找和收集您需要在图表中使用的所有&#x200B;*资源*。

它监视硬盘驱动器上的&#x200B;*文件夹*，或通过网络监视添加到[项目设置](../../interface/preferences-window/project-settings/project-settings.md)中的[库监视路径](https://docs.substance3d.com/display/SDDOC/Project+Settings#ProjectSettings-proj-libraryLibrary)列表中的文件夹。 这些文件夹中发生的任何更改（添加、删除和更新内容）都&#x200B;*会转移*&#x200B;到<b>库</b>。

>[!WARNING]
>
> **关于自定义内容**
> 
> 虽然您的自定义资源将添加到&#x200B;**库**&#x200B;中，但由于为现有类别设置了筛选规则，它可能不可见。 我们建议创建您自己的按文件夹组织的过滤器，以确保在处理项目时可靠地找到您的内容。\
> 有关详细信息，请参阅文档的[管理自定义内容和筛选器](./managing-custom-content/managing-custom-content-and-filters.md)部分。

**库**&#x200B;可以监视支持[资源](../../resources/resources.md)的所有资源：

* [Substance包](../../getting-started/overview/overview.md) (SBS)和[Substance存档](../../getting-started/overview/overview.md) (SBSAR)中的图形
* [位图图像](../../resources/bitmap-resource/bitmap-resource.md)
* [矢量图像](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [函数图表](../../function-graphs/function-graphs.md)
* [AxF文件](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)
* [字体](../../resources/font-resource/font-resource.md)
* [3D](../../resources/3d-scene-resource/3d-scene-resource.md)

该面板分为两个主要部分：

* 左侧的&#x200B;**类别**&#x200B;部分
* 右侧的&#x200B;**内容**&#x200B;部分

## 类别

<b>类别</b>部分位于<b>库</b>面板的左侧，以树形视图形式包含所有资源&#x200B;*类别*（即文件夹）和&#x200B;*筛选器*。\
您可以单击此树视图中的任何项以显示其内容以及&#x200B;*其所有子项*&#x200B;的内容。

### 类别

默认类别和过滤器包含Designer随附的所有资源。 无法编辑或删除它们。\
默认类别包括：

* 收藏夹：收集所有已标记为“收藏夹”的资源
* [图形项](../../interface/the-graph-view/graph-items/graph-items.md)：列出用于组织图形的特殊对象
* [原子节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)：列出[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)的原子节点
* [FX-Map节点](../../function-graphs/fxmaps/fxmaps.md)：包括特定于[FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)节点计算的图形的节点
* [函数节点](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/atomic-function-nodes.md)：列出[函数图形](../../function-graphs/function-graphs.md)的原子节点
* [纹理生成器](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/texture-generators.md)：包含表示可自动生成Substance的[内容图表](../../compositing-graphs/substance-compositing-graphs.md)的节点
* [筛选器](../../compositing-graphs/nodes-reference-for-com/node-library/filters/filters.md)：包含表示修改输入的[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)的节点
* [样条和路径工具](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-paths-tools.md)： [样条](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md)和[路径](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md)节点的目录
* [SDF 函数](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions)：包括用于创作3DSDF 函数的节点，可与[形状飞溅v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)和[3D查看器](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)节点一起使用
* [函数](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md)：包括表示[函数图形](../../function-graphs/the-function-graph/the-function-graph.md)的节点
* [3D视图](../3d-view/3d-view.md)：提供与3D场景中用于基于图像的光照的地图相关的内容，例如[3D视图](../../interface/3d-view/3d-view.md)中的内容，例如环境地图和创作环境地图的节点
* PBR素材：可用作占位符的预制素材，用于测试其他节点、“菜谱”或自定义工作区设置。 要了解创作素材，我们建议您查看我们专门的[素材示例](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)。
* [值](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md)：用于在Substance图表中生成简单值的节点。

## 内容

<b>库</b>的内容显示为&#x200B;*标记的缩览图*。 根据以下因素，这些缩览图具有不同的外观：

* [SBS](../../getting-started/overview/overview.md)和[SBSAR](../../getting-started/overview/overview.md)文件中的[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)用其&#x200B;*第一输出*&#x200B;表示，如果图形的作者设置了自定义图标，则用其&#x200B;*自定义图标*&#x200B;表示
* [位图](../../resources/bitmap-resource/bitmap-resource.md)和[矢量图形(SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)由位图本身的&#x200B;*微型渲染*&#x200B;表示
* [3D场景](../../resources/3d-scene-resource/3d-scene-resource.md)、[函数图形](../../function-graphs/the-function-graph/the-function-graph.md)、[字体](../../resources/font-resource/font-resource.md)和[AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)文件由每种类型的&#x200B;*通用图标*&#x200B;表示

>[!WARNING]
>
> **如果缩略图出现问题**
> 
> 对于与库缩览图相关的任何问题（图像不正确、渲染卡在刷新图标上等），我们建议的故障排除步骤 是手动触发&#x200B;*缩略图刷新*。\
> 为此，请使用[首选项窗口](../../interface/preferences-window/preferences-window.md)的[库](../../interface/preferences-window/preferences-window.md)部分中的&#x200B;**重新生成缩略图**&#x200B;按钮。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 使用库中的资源

要使用库中的资源，请&#x200B;*将其拖放*&#x200B;到所需位置。\
在单击项目时按住<b>Ctrl</b>键，可在<b>内容</b>部分中选择&#x200B;*多个*&#x200B;项目。 在这种情况下，拖放操作会将节点放在&#x200B;*整个选区*&#x200B;的图形中。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![从库中删除节点](../../assets/library-create-node.gif "从库中删除节点")

</td>
</tr>
</table>

### 按名称搜索资源

使用<b>搜索</b>栏（位于<b>内容</b>部分的左上角），可以按名称&#x200B;*搜索*&#x200B;任何资源。 以这种方式搜索内容时，将忽略<b>类别</b>部分中的当前选择，并搜索<b>库</b>中的&#x200B;*整个内容*。\
您可以使用<b>搜索</b>栏旁边的![](../../assets/library-icon-search-filter.png) <b>筛选依据……</b>图标，按&#x200B;*图形类型*&#x200B;筛选搜索结果。

>[!NOTE]
>
> 搜索栏将考虑您正在查找的资源的名称，但也会考虑资源可包含的&#x200B;*标记*&#x200B;或其所属的&#x200B;*类别*。\
> 例如，键入“*Normal*”将列出可用于生成或修改法线图的所有资源。 这是发现新节点的好方法，从而发现新的可能性！

![库中资源搜索](../../assets/library-search-2.png "库中资源搜索")

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 正在可视化库资源

使用![](../../assets/library-icon-view-mode.png) <b>显示模式</b>下拉按钮，您可以选择内容项的显示大小。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![库资源查看模式](../../assets/library-display-modes.png "库资源查看模式")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

使用![](../../assets/library-icon-toggle-label.png) **切换标签**&#x200B;按钮可显示或隐藏节点的标签。

</td>
<td style="border: 0;" valign="top">

![标签切换](../../assets/library-toggle-label.png "标签切换")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

将光标放在内容项上时，如果项的作者已提供项&#x200B;*说明*，则短时间后会显示工具提示。\
*右键单击该项目*&#x200B;以显示其他信息，包括该项目源文件的路径。

</td>
<td style="border: 0;" valign="top">

![资源信息工具提示](../../assets/library-item-tooltip.png "资源信息工具提示")

</td>
</tr>
</table>

>[!NOTE]
>
> 对于[实例化](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) — 即非原子节点，此路径是&#x200B;*超链接*，它将在系统的文件浏览器中显示文件。\
> 原子节点使用特殊的别名路径（例如，`graphatomic://`、`structure://`、...） 无法单击，因为它指向内部库。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 收藏

您可以使用![](../../assets/library-icon-favoritepng.png) <b>添加到收藏夹</b>按钮，将<b>内容</b>分区中的任何项添加到您的<b>收藏夹</b>列表。 如果已经添加了该内容，该按钮还允许您将内容从此列表中&#x200B;*删除*。\
将内容添加到此列表后，该内容在<b>库</b>的<b>收藏夹</b>类别中可用，并且在搜索图形中的节点时，该内容将显示在<b>节点</b>菜单列表的&#x200B;*顶部*&#x200B;处（如果搜索项与该节点匹配）。

</td>
<td style="border: 0;" valign="top">

![库中的收藏夹](../../assets/library-favourites.png "库中的收藏夹")

</td>
</tr>
</table>
