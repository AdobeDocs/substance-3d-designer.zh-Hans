---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: 了解如何将Substance合成图形导出为PSD文件，以便在Adobe Photoshop和其他图像编辑工作流程中使用。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出 PSD 文件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# 导出 PSD 文件

Substance 3D Designer允许将纹理导出为Adobe Photoshop文档或PSD文件。本页介绍用于将节点平移为层的特殊界面。图形&#x200B;**此过程不是自动的：您拥有很多控制权，但它是有限的，并且通常无法获得节点和图层之间的准确匹配。** 此外，无法保证您的PSD包含与图形相同的输出，除非您明确将其设置为这样做。 一般来说，您想要的越准确和正确，用户需要花费的精力就越多。 通常，唯一能够以非破坏性方式密切复制的内容是[混合节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)。 不支持调整图层，图层样式或图层混合模式之外的任何其他内容均不受支持。

[Substance 3D Designer也可以导出为位图文件。](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## PSD导出对话框

只能通过一种方法打开PSD导出对话框。 在要导出到PSD的图形的[图形视图](../../interface/the-graph-view/the-graph-view.md)中，单击![](exporting-psd-files.resources/image2019-9-17-14-44-17.png) <b>“工具”</b>按钮并选择<b>PSD 导出器</b>。 该界面在<b>图形视图</b>内变为可见。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![用户界面PSD 导出器](exporting-psd-files.resources/psd-dialog.png "用户界面PSD 导出器")

</td>
<td style="border: 0;" valign="top">

1. <b>文件名和位置：</b>设置文件夹和文件名以便在此处导出。 按“导出”按钮执行导出过程。
1. <b>添加组：</b>添加图层组
1. <b>添加图层下拉列表：</b>从以下两种方法中选择一种来添加图层。 也可以通过&#x200B;*使用鼠标右键将堆叠*&#x200B;拖动到节点来添加图层。
1. <b>移除图层下拉列表：</b>移除选定图层或所有图层。
1. <b>Layerstack：</b>如果在此处执行大多数设置工作。 界面镜像Photoshop中的有限选项。 在此处设置图层名称、混合模式和不透明度。 如果图层有两个缩略图，则第二个缩略图代表Alpha 通道。

</td>
</tr>
</table>

## 工作流

由于Photoshop不直接支持多输出材料，因此有多种方式可设置您的PSD。 以下是常用方法的简述。

* 为所有输出设置多个文件夹。 一个文件夹用于基色，一个文件夹用于普通，一个文件夹用于粗糙度等。
* 用鼠标右键将输出拖放到适当的组中。 如果要保持简单，可以只将PSD保留在此处。
* 要展开PSD更多：可按您的方式返回到图表左侧，将图表的相关中间步骤拖放到相应的组中。 无法在输出/组之间共享图层。

在极少数情况下，PSD是更重要的输出，您可以构建图表以便只使用混合模式。 在这种情况下，应该有可能将图形的可编辑性更高的版本重新创建为分层文档。
