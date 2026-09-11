---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window.html"
breadcrumb-title: ''
description: 使用Substance 3D Designer中的“资源管理器”窗口浏览、整理和管理项目文件和资源。
helpx_creative_field: ""
helpx_description: Designer > Interface > Explorer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 资源管理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 16eb8a173e984f842c820f3b8f0c3e140040bdfa
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 2%

---


# 资源管理器

此页面描述了[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中的Explorer程序坞。 通过此停靠窗格，您可以管理包及其资源。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概述

资源管理器停放区是您管理当前在Substance 3D Designer中打开的文件和资源的地方。 它向您显示当前打开的所有包的列表，其中每个包都展开为层次结构，以显示其中的[资源](../../resources/resources.md)。

资源管理器是您开始和结束项目的位置，因为它允许您创建、保存和导出任何类型的资源。

</td>
<td style="border: 0;" valign="top">

![资源管理器停放](the-explorer-window.resources/explorer-3.jpg "资源管理器停放")

</td>
</tr>
</table>

您可以通过资源管理器停放区执行一些重要操作：

* 创建新包和图形
* 加载现有包
* 保存并关闭加载的包
* [导入和链接资源](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)
* [将图形结果导出到纹理](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)
* [将包Publish到Substance 3D资源(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)
* [将包发送到其他Substance 3D应用程序](send-to-interoperability/send-to-interoperability.md)
* [从网格中烘焙地图](../../bakers/bakers.md)

## 顶部工具栏

此工具栏可让您快速执行与整体工作流程相关的功能。 所有按钮均为&#x200B;*上下文识别*，这意味着它们会根据您在资源管理器中的当前选择激活并更改其行为。

![](the-explorer-window.resources/save.png) <b>保存</b>选定的包。

![](the-explorer-window.resources/sendto-icon.jpg) <b>Publish或[发送](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)</b>个所选元素：

* [将任何选定包Publish到Substance 3D资源(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)；
* 将所选包发送到[Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)、[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)或[Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html)。

![](the-explorer-window.resources/republish.png) <b>Publish或像以前一样发送：</b> Publish或发送所选元素的设置与以前相同。 此选项仅适用于已在&#x200B;*当前*&#x200B;会话中&#x200B;*至少*&#x200B;发布过一次的包。

![](the-explorer-window.resources/graph-cleaner.jpg) <b>删除选定图形中未使用的节点</b>。 该工具遵循以下规则：

* 仅当所选项目为&#x200B;*相同类型*&#x200B;时，该工具才可用：仅图形、文件夹或包；
* 当选择包含文件夹或包时，该工具以&#x200B;*递归*&#x200B;方式清理其中的所有图表；
* 如果目标图形之一是[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)，则可以使用第二个选项，它允许您清理该图形中节点上的所有参数函数。

在[图形视图](../../interface/the-graph-view/the-graph-view.md)页面的“移除未使用的节点”部分中了解有关该工具的更多信息。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Publish/发送下拉菜单](the-explorer-window.resources/explorer-sendto-displayed.jpg "Publish/发送下拉菜单")

*Publish/发送*

</td>
<td style="border: 0;" valign="top">

![删除未使用的节点下拉菜单](the-explorer-window.resources/explorer-graph-cleaner.jpg "删除未使用的节点下拉菜单")

*删除未使用的节点*

</td>
</tr>
</table>

## 上下文菜单

您与浏览器的大多数交互是通过上下文菜单进行的，上下文菜单通过在浏览器树形视图中的某个项目上单击RMB显示。

可用选项因选定和单击的项目而异：

+++空白空间

只有当前打开的任何包下方有空白空间可用。 单击现有项目旁边的不会视为空白。

<b>新建包</b>：创建一个新的空包；

<b>打开包</b>：打开文件对话框以打开SBS文件。

+++

+++包

<b>新建</b>允许您创建新图形([Substance图形](../../compositing-graphs/substance-compositing-graphs.md)、[位图](../../resources/bitmap-resource/bitmap-resource.md)和[矢量图形](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)资源，以及用于排序内容的&#x200B;*文件夹*

<b>导入</b>和<b>链接</b>允许您引入[资源](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

通过<b>重新加载</b>、<b>保存、另存为</b>和<b>将副本另存为</b>，可将以前保存的包版本保存到磁盘或从磁盘回调。

<b>Publish .sbsar文件</b>和<b>重新发布.sbsar文件</b>允许您[发布](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)未编译且未优化的Substance图形，以便在其他Substance应用程序和集成中提供给我们一个高效且便携的SBSAR文件。 Publish as Previous使用相同的选项重复以前的Publish操作，跳过选项对话框以加快迭代。 工具栏包含具有相同功能的按钮。

<b>带依赖项的导出</b>与保存和发布不同。 它将获取您的SBS文件，收集所有引用的资源和依赖项，并创建一个自包含包。 通过对话框，可以选择要收集哪些库，以及文件是否应为压缩存档(7-zip)。 与其他人共享SBS文件时最好选择此选项，而不用担心缺少依赖项。

<b>发送至……</b>可打开子菜单，允许您直接[发送包至](send-to-interoperability/send-to-interoperability.md)[Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)、[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)、[Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html)或[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)。

<b>复制</b>复制所选包。

<b>粘贴</b>将复制的图形和/或资源&#x200B;*粘贴到*&#x200B;选定的包中。

<b>关闭包</b>关闭所有选定的包

<b>计算输出</b>强制Designer计算包中所有图形的所有输出。

<b>在资源管理器中显示……</b>在操作系统的文件资源管理器窗口中打开包的位置

<b>依赖关系管理器</b>将打开选定包的“依赖关系管理器”窗口。

<b>打开依赖项</b>在资源管理器中打开所有依赖项（仅&#x200B;*[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)*）。

+++

+++Substance 图形

<b>打开：</b> （返回）在[图形视图](../../interface/the-graph-view/the-graph-view.md)中打开此图形。

<b>副本：</b> *(Ctrl-C)*&#x200B;将当前图形复制到剪贴板。

<b>删除：</b>（删除）从此包中删除图形。

<b>重命名：</b> (F2)重命名此图形。

<b>在3D视图中查看输出：</b>将此图表的输出发送到[3D视图](../../interface/3d-view/3d-view.md)，以显示为素材。

<b>计算输出：</b>计算此图表的输出并将它们保留在内存中。

<b>导出输出……：</b>打开[导出为位图的对话框。](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

+++

+++3D 场景资源

<b>打开：</b> （返回）在[3D 视图](../../interface/3d-view/3d-view.md)中使用此3D 网格，替换标准多维数据集或平面。

<b>复制：</b> (Ctrl-C)将此资源复制到剪贴板。

<b>粘贴：</b> (Ctrl-V)从剪贴板粘贴资源。

<b>删除：</b> (Del)从此包中删除资源。

<b>重命名：</b> (F2)重命名此资源。

<b>重新加载：</b>强制从磁盘重新加载此网格。

<b>在资源管理器中显示：</b>在磁盘上的资源位置打开系统文件浏览器窗口。

<b>重定位：</b>将此资源更改为链接到其他文件。

<b>烘焙模型信息……：</b>打开[烘焙对话框。](../../bakers/bakers.md)

+++

+++文件夹

<b>新建：</b>允许您在文件夹中创建新图形（[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)、[Substance函数图形](../../function-graphs/function-graphs.md)、[位图](../../resources/bitmap-resource/bitmap-resource.md)和[矢量图形](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)资源，以及用于排序的&#x200B;*文件夹*）。

<b>导入</b>和<b>链接： </b>允许您导入[资源](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)并将它们放入文件夹中。

<b>复制：</b> (Ctrl-C)将文件夹及其所有内容复制到剪贴板。

<b>粘贴：</b> (Ctrl-V)从剪贴板粘贴文件夹及其所有内容。

<b>重命名：</b> (F2)重命名此文件夹。

<b>移除：</b> *(Del)*&#x200B;从其包中删除文件夹及其所有内容。

<b>计算输出：</b>计算文件夹中包含的所有图形的输出并将它们保留在内存中。

+++

## 底部工具栏

资源管理器停靠区底部的工具栏提供有关程序包或程序包资源的信息：

<b>![](the-explorer-window.resources/explorer-dependencies.jpg)依赖关系：</b>选择某个包后，其包依赖关系将列在专用面板中。

<b>![](the-explorer-window.resources/explorer-information.jpg)信息：</b>提供与当前选定的包或资源相关的元数据：

* 包：包的完整文件路径
* [位图资源](../../resources/bitmap-resource/bitmap-resource.md)：资源的完整文件路径、其[ICC配置文件](../../color-management/color-management.md)、图像大小和[导入方法](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)（即&#x200B;*链接的*&#x200B;或&#x200B;*导入的*）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![依赖关系面板](the-explorer-window.resources/explorer-dependencies-displayed.jpg "依赖关系面板")

*依赖项*

</td>
<td style="border: 0;" valign="top">

![信息面板](the-explorer-window.resources/explorer-information-displayed.jpg "信息面板")

*信息*

</td>
</tr>
</table>
