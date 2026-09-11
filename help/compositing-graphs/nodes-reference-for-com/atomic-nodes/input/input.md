---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input.html"
breadcrumb-title: ''
description: 使用“输入”节点创建可由用户公开和调整的Substance图表的输入参数。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 输入
user-guide-description: ''
user-guide-title: ''
source-git-commit: 65a0ec6dc38e7595406c0c531be72ad1670dfb86
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---


# 输入

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![原子节点：输入颜色](input.resources/comp_inputcolor_1.png "原子节点：输入颜色"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![原子节点：输入灰度](input.resources/comp_inputgrayscale_1.png "原子节点：输入灰度"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![原子节点：输入值](input.resources/comp_inputnumeric_1.png "原子节点：输入值"){width="200px"}

</td>
</tr>
</table>

输入节点是一种特殊类型的节点，可在图形中创建动态槽，允许一旦在另外的上下文中使用“图形”就连接任何输入。

与[输出节点](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)不同，您必须显式放置彩色、灰度或值输入。 您不可能创建自己的“不可知”输入，这些输入会根据与它们关联的内容更改类型。

输入节点不像[输出节点](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)那样重要：您可以拥有完全正常运行的高级图形，这些图形不需要输入。 仅当希望将图形或节点实例的结果基于外部输入时（例如，为Substance 3D Painter创建[实例](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)或[筛选器](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/effects/filter)时），才会使用输入。

## 参数

默认情况下，如果未插入任何对象，“输入颜色”或“灰度”会返回黑色。 您可以设置其他默认值，或将现有[位图资源](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)从[资源管理器](../../../../interface/the-explorer-window/the-explorer-window.md)拖动到图形中的输入节点上，以便在槽中预览此数据。 这仅适用于颜色和灰度输入。 默认值在其它上下文中使用时是永久性的，预览位图将在任何其他位置被丢弃。

如果要用另一个图形的输出来查看它，则必须将该图形导出为上述方法的位图，或使用“In-Context”编辑。

|  |  |
| --- | --- |
| <b>PKG资源路径</b> *字符串* | 指向用于预览的自定义位图资源。 |
| <b>默认值</b> *颜色/灰度/值* | 如果这个插槽没有连接任何设备，则允许使用除黑色以外的其他值作为默认输入。 |

## 属性

|  |  |
| --- | --- |
| <b>标识符</b> *字符串* | 唯一的必填唯一属性。 不能包含空格。   如果未设置Label，则用于标记输入，并用于区分不同的输出。 不要将这些项留在“input\_1”！ |
| <b>描述</b> *字符串* | Designer的工具架和Painter库中使用的可选说明。 |
| <b>标签</b> *字符串* | UI标签，用于在Designer和Painter UI中方便地添加标签。 可以包含空格。   建议使用与标识符类似的名称设置，只使用空格键而不是下划线。 |
| <b>用户数据</b> *字符串* | 可用于特定筛选操作的附加可选用户数据，基本上是通配符自定义数据字段。 |
| <b>组</b> *字符串* | 用于为Designer的[链接创建模式](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)将输入进行分组的组属性。   具有相同（区分大小写）组属性的输入将作为单个连接显示在紧凑材质模式中。 |

## 继承

<table>
<tr style="border: 0;">
<td style="border: 0; vertical-align: top">

当存在多个输入时，您需要注意图形将如何从这些输入[继承其基本参数](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。\
基本参数包括<b>输出大小</b>、<b>输出格式</b>和<b>拼贴模式</b>等。

可将输入定义为[主要输入](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。 然后，此输入驱动所有输入的属性，继承方法设置为&#x200B;*相对于父代*。 这是输入节点上默认设置的继承方法&#x200B;**。

</td>
<td width="25%" style="border: 0;" valign="top">

![图形中的主要输入](input.resources/node-primary-input.png)

</td>
</tr>
</table>

您可以将输入节点设置为图形的主要输入，方法是单击该节点上的&#x200B;*RMB*，然后在上下文菜单中选择<b>设置为主要输入</b>选项。\
节点的主输入在连接器&#x200B;*中用*&#x200B;小黑点标记（在本节旁边的示例中，用红色圈起）。

或者，设置为&#x200B;*相对于输入*&#x200B;继承方法的任何输入都将从其所连接的节点继承属性，而不管主输入的&#x200B;**。

最后，可以通过将给定属性的继承方法设置为&#x200B;*绝对*&#x200B;来覆盖该属性的任何值。

>[!TIP]
>
> 要了解有关继承的更多信息，请转到本文档的[Substance图形中的继承](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)页。

>[!IMPORTANT]
>
> [Substance 3D资源(SBSAR)](../../../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中输入节点的&#x200B;*相对于输入*&#x200B;继承方法&#x200B;*不受支持*。 在发布包之前，将所有输入节点的继承方法设置为&#x200B;*相对于父代*。

## 集成属性

输入不会直接发送到3D 视图，但[Substance 3D Painter](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/home)会使用它们的使用情况属性自动为某些映射填充槽（主要与[筛选器](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/effects/filter)一起使用）。

此外，[链接创建模式](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)也使用使用情况属性，以匹配正确的输入和输出插槽。

<b>用法</b>

|  |  |
| --- | --- |
| <b>组件</b> *字符串* | 这决定了生成的输入中实际包含哪些通道。   这是旧版设置，集成和图形不再使用它。 |
| <b>用法</b> *字符串* | 定义此输入的类型或用法。 它指示其他节点应如何连接到此输入。 |
| <b>色彩空间</b> *字符串* | 设置应解释此输入的色彩空间。 |
