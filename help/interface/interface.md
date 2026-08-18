---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer工作区界面，包括视图、面板和自定义选项。
helpx_creative_field: ""
helpx_description: Designer > Workspace
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 工作区
user-guide-description: ''
user-guide-title: ''
source-git-commit: 163ef15c862c56a1b59a4ccd47f4396c825be18f
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 1%

---


# 工作区

工作区被分成单独的区域，称为<b>停靠</b>，该区域可以[调整Designer主窗口的大小、移动和取消停靠](../interface/customizing-your-wor/customizing-your-workspace.md)到浮动停靠区中。

Designer的默认停放布局如下：

![Substance 3D Designer主窗口](../assets/interface-overview.jpg "Substance 3D Designer主窗口")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>1</b>主菜单和工具栏

<b>2</b>资源管理器

<b>3</b>图形视图

</td>
<td style="border: 0;" valign="top">

<b>4</b>属性

<b>5</b> 2D视图

</td>
<td style="border: 0;" valign="top">

<b>6</b>个3D视图

<b>7</b>库

</td>
</tr>
</table>

>[!NOTE]
>
> 界面缩放
> 
> Designer从OS *获取用户界面元素*&#x200B;的特定比例。 因此，对用户界面缩放比例的任何调整都应在操作系统的显示设置中完成。
> 
> 为确保在Designer中正确应用显示设置，请在更改这些设置后&#x200B;*注销您的OS用户会话*&#x200B;并重新登录。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 主菜单和工具栏

主工具栏可让您访问额外的菜单，如[首选项窗口](../interface/preferences-window/preferences-window.md)，并且有几个按钮可用于快速创建新的Substance图形和包。

</td>
<td style="border: 0;" valign="top">

![主菜单和工具栏](../assets/mainmenu-1.png "主菜单和工具栏")

</td>
</tr>
</table>

* <b>文件： </b>用于创建新的包和资源，以及保存和关闭当前正在处理的包。 此菜单中的功能也可用作此工具栏上的快速按钮。
* <b>编辑： </b>提供“撤消”和“重做”功能（可通过下面的“快速”按钮使用），以及对[首选项](../interface/preferences-window/preferences-window.md)的访问权限，用于深度内自定义。
* <b>工具：</b>控制Substance 引擎并允许您访问插件管理器。
* <b>Windows：</b>用于隐藏或显示任何窗口（某些窗口默认处于隐藏状态），并将窗口布局重置回默认设置。
* <b>帮助： </b>提供对额外信息和在线资源的访问，例如Substance学院或此文档网站。

## 资源管理器

[资源管理器窗口](the-explorer-window/the-explorer-window.md)是与任何类型的文件和资源交互的主要方式。 它提供了比主工具栏中的“文件”菜单更多的选项。这是开始和结束每个工作会话的位置。

![资源管理器](../assets/explorer-4.png "资源管理器")

## 图形视图

[图形视图停放](../interface/the-graph-view/the-graph-view.md)是Substance 3D Designer中最重要的窗口。 它显示Designer中可用的任何类型图形的节点网络（[Substance图形](../compositing-graphs/substance-compositing-graphs.md)、[Substance函数图形](../function-graphs/function-graphs.md)、[FX-Map图形](../function-graphs/fxmaps/fxmaps.md)），并允许您构建和编辑这些图形。

![图形视图](../assets/graph-6.png "图形视图")

## 属性

[属性停放](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)是最具技术性的窗口。 它始终与上下文相关，并且将显示可更改选定资源或节点行为的滑块、下拉菜单和其他元素。

![属性](../assets/properties-15.jpg "属性")

## 2D 视图

[2D视图](../interface/2d-view/2d-view.md)是最简单的预览工具。 它与图形紧密配合使用：双击图形视图中的任何节点将在2D视图中显示可视化结果。

![2D视图](../assets/2d-view-1.jpg "2D视图")

## 3D 视图

[3D视图](../interface/3d-view/3d-view.md)是最交互式、最高级的预览窗口。 与2D视图不同，它使用许多不同的输出映射来渲染完整的材质。 这意味着您将看到所有显示的通道，如“基色”、“正常”和“粗糙度”。

![3D视图](../assets/3dview-3.jpg "3D视图")

## 库

默认情况下，[通过库程序坞](../interface/the-library/the-library.md)，可访问Designer库中包含的所有内容，以及[自定义内容](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)。 为了更好地了解库中原子节点和实例节点之间的差异，请确保阅读[节点概述](https://helpx.adobe.com/substance-designer/using/nodes-overview.html)。

![库](../assets/library-3.jpg "库")
