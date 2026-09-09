---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: 了解如何从Substance合成图导出纹理和位图以在外部应用程序和工作流程中使用。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出位图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# 导出位图

本页介绍Substance 3D Designer如何导出为多种不同的位图文件格式，以及如何批量导出多个UV磁贴。如果要[导出到PSD文件](../exporting-psd-files/exporting-psd-files.md)，请为此创建一个单独的专用页。

![导出简化](exporting-bitmaps.resources/exportflow.png "导出简化")

## 导出概念

导出位图时，最好记住下列要点：

* 您<b>从图形</b>导出，而不是从包导出。 包不会自行生成图像内容。
* 导出的位图数（和分辨率）由图形的<b>输出</b>决定。
* 已为所有输出/位图设置Filetype。
* 导出不同于[发布](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)，请确保您充分理解其中的差异！

## 导出方法

准备好导出后，可以通过两种方式访问导出对话框：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)窗口中，右键单击要导出的图形，然后选择&#x200B;**“将输出导出为位图”**

![](exporting-bitmaps.resources/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

在[图形视图](../../interface/the-graph-view/the-graph-view.md)中，单击“工具”按钮![](exporting-bitmaps.resources/image2019-9-17-14-44-17.png)并选择&#x200B;**“导出输出……”**

![](exporting-bitmaps.resources/export-graph.gif)

</td>
</tr>
</table>

## “导出”对话框

导出对话框为您提供了一些用于自定义导出的选项。

右侧显示的版本是标准对话框，在打开对话框之前，可在“图形”、“输出”或设置“父级”分辨率来更改分辨率。

1. <b>目标： </b>要保存的所有文件的位置。
1. <b>格式：</b>文件类型用于所有导出的文件。
1. <b>模式</b>：生成基于元数据关键字的文件类型的泛型方法。 为了验证，下面显示了基于第一个输出的文件名示例。\
   下面列出了所有可用选项：
   1. *$（图形）* — 当前图形的名称
   1. *$（标识符）* — 当前输出的标识符
   1. *$（描述）* — 当前输出的描述
   1. *$(label)* — 当前输出的标签
   1. *$(user\_data)* — 当前输出的自定义用户数据
   1. *$(group)* — 当前输出的输出组
   1. *$（色彩空间）* — 当前输出的色彩空间（仅适用于&#x200B;*OCIO*&#x200B;和&#x200B;*AdobeACE* [色彩管理](../../color-management/color-management.md)模式）
1. <b>输出：</b>打开或关闭图表中的特定输出和输出组。 按钮可以全部打开或关闭。 仅更改一个位图时有用。
1. <b>自动导出：</b>切换按钮用于在更改后立即启用图形输出的自动重新导出。 仅适用于当前图表。 可能很重且速度较慢，具体取决于设置。
1. <b>导出按钮：</b>使用当前设置导出，或关闭对话框。

![导出输出对话框](exporting-bitmaps.resources/fromgraph-1.png "导出输出对话框")

## “导出”对话框（批处理/UV磁贴）

在Designer中使用UV拼贴网格时，“导出”对话框的使用方式略有不同，允许一次批量导出多个UV拼贴。 确保您了解此工作流程，并已将[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)正确分配给一个或多个UV磁贴。\
使用批处理选项卡还可以更快地以不同于工作（父）分辨率的分辨率导出图形。

使用上面详述的相同方法启动对话框，只需确保右键单击资源管理器&#x200B;*中UV磁贴分配的图形*，或者已在使用“工具”按钮时&#x200B;*在图形视图中打开特定的UV磁贴分配的图形*。

1. <b>批处理选项卡</b>：确保选择此选项卡而不是标准<b>从图形</b>方法，否则选项2-3将不可用。
1. <b>UV拼贴：</b>与输出一样，允许您打开或关闭特定UV拼贴的导出。
1. <b>[输出大小](../../compositing-graphs/output-size/output-size.md)： </b>覆盖导出分辨率，允许您以最大大小导出时进行更小、更高效的工作。

![批量导出输出对话框](exporting-bitmaps.resources/batch.png "批量导出输出对话框")
