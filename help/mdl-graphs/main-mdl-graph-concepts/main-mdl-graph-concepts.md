---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/main-mdl-graph-concepts.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer中用于材料创建的材料定义语言图形的主要概念。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Main MDL graph concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 主要MDL 图概念
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---


# 主要MDL 图概念

此页面介绍了&#x200B;*特定的*&#x200B;到[MDL 图](../../mdl-graphs/mdl-graphs.md)的主要概念，应充分理解这些概念，以便在Substance 3D Designer中充分利用此图形类型。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Iray

MDL 材质使用专为基于物理的渲染解决方案设计的说明，嵌入Designer中的[Iray](../../interface/3d-view/iray/iray.md)渲染器支持该说明。 因此，要在活动[3D视图](../../interface/3d-view/3d-view.md)面板中选择Iray渲染器&#x200B;*，才能显示MDL 图*&#x200B;的结果。

</td>
<td style="border: 0;" valign="top">

[![NVIDIAIray徽标](main-mdl-graph-concepts.resources/iray-logo.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>
</table>

创建或加载MDL 图时，Designer找到的第一个[未固定](../../interface/customizing-your-wor/customizing-your-workspace.md)个3D视图面板将&#x200B;*自动切换*&#x200B;到[Iray](../../interface/3d-view/iray/iray.md)渲染器。 如果没有可用的3D视图，将创建&#x200B;*新的*&#x200B;个3D视图面板，并将其切换到Iray渲染器，以承载正在编辑的MDL 材质的渲染。

在3D视图面板中选择Iray渲染器后，可通过该面板的“材料”菜单在可用MDL 材质（包括在“资源管理器”面板中加载的材料和Designer MDL材料库）之间切换。 请参阅本文档的[Iray](../../interface/3d-view/iray/iray.md)部分，了解有关在Iray中使用MDL 材质的更多信息。

## 根节点

MDL 图的结果由<b>根</b>节点定义。 图形的任何节点都可以设置为根，只要其输出类型为<b>材料</b>的数据，即&#x200B;*材料定义*&#x200B;即可。 一个MDL 图只能有&#x200B;*一个*&#x200B;根节点。

通常，可以设置为根节点的材料可以是&#x200B;*自给自足的*，因为它已经包含节点定义，可以通过将数据传递到其&#x200B;*输入*&#x200B;来自定义节点定义。\
例如，如果要处理类似玻璃的材料，您可能希望使用“玻璃”材料定义作为“根”节点，但这是&#x200B;*非强制性*。 通过大量的MDL材料可以生成复杂的材料。

根节点包括显示其当前输出预览的缩略图。

![MDL 图的根节点](main-mdl-graph-concepts.resources/mdl-root-hl.png "MDL 图的根节点")

*MDL 图中的根节点及其在[属性](../../interface/properties/properties.md)* *面板*&#x200B;中显示的属性

## 连接器和类型

由于MDL 图中的数据类型比Designer中的其他图形多得多，因此您可以看到节点连接器独特的外观。 以下列出了需要了解的重要概念。

连接器形状

连接器的&#x200B;*形状*&#x200B;指示数据类型是&#x200B;*一致*（圆形）还是&#x200B;*变化*（方形）。

“统一类型的变量只能设置为统一值。 可变类型的变量可以设置为可变值以及统一值。 因此，变量中的结果值始终被视为是变化的。” （来源： [MDL规范](https://raytracing-docs.nvidia.com/mdl/specification/MDL_spec_1.7.2_17Jan2022.pdf)的第6.3节）

以下是一些示例：

* <b>纹理</b>示例为&#x200B;*变化*，因为值受采样像素的影响
* <b>颜色</b>值为&#x200B;*一致*，因为无论上下文如何，它都会均匀传递
* <b>BRDF</b>为&#x200B;*变化*，因为值受入射角的影响
* <b>浮点</b>或<b>布尔值</b>为&#x200B;*一致*，因为无论上下文如何，都会平均地传递该值

连接器颜色

使用鼠标将连接器悬停在标识符/标签后面时，从输出连接器传入或输入连接器预期的&#x200B;*数据类型*&#x200B;会进行颜色编码并显示在括号之间。

>[!WARNING]
>
> 只有&#x200B;*匹配数据类型*&#x200B;的连接器可以链接在一起。 颜色编码的唯一目的是提高关于图表中传递的数据类型的可读性，以及哪些连接器可以链接在一起。

![MDL节点连接器类型](main-mdl-graph-concepts.resources/mdl-connector-types.png "MDL节点连接器类型"){width="512px"}

*连接器的长宽比因I/O值类型而异，I/O标识符后面用括号括起来*

## 已筛选节点创建

您可以向图形中添加<b>库</b>的<b>mdl</b>类别中的任何可用节点，方法是&#x200B;*将节点*&#x200B;从<b>库视图</b>拖动到<b>图形视图</b>中，或在&#x200B;*未选择任何内容*&#x200B;时按<b>空格键</b>在图形视图中打开<b>节点菜单</b>。 在这种情况下，将显示&#x200B;*未筛选的*&#x200B;节点列表。

但是，在某些情况下，“节点”菜单中的节点列表会过滤为仅显示与目标输入或输出匹配的数据类型的节点：

* 如果在图形视图中选择了&#x200B;*节点*&#x200B;并按下<b>空格键</b>
* 如果单击<b>LMB</b>，按住并&#x200B;*从*&#x200B;节点连接器&#x200B;*中拖出*&#x200B;链接

您可能要记住应用于筛选的&#x200B;*规则*：

* 如果在选择&#x200B;*单个*&#x200B;节点时按<b>空格键</b>显示“节点”菜单，则该列表包括其&#x200B;*第一输入*&#x200B;的数据类型与所选节点的&#x200B;*输出*&#x200B;数据类型匹配的节点
* 如果在选择&#x200B;*多个*&#x200B;节点时按<b>空格键</b>显示“节点”菜单，则此列表包含的节点中，*第一个输入*&#x200B;的数据类型与&#x200B;*最后一个选定的*&#x200B;节点的&#x200B;*输出*&#x200B;的数据类型相匹配
* 如果通过&#x200B;*将链接*&#x200B;拖出&#x200B;*输出*&#x200B;连接器来显示“节点”菜单，则该列表包括其&#x200B;*第一输入*&#x200B;的数据类型与所选&#x200B;*输出*&#x200B;的数据类型匹配的节点
* 如果通过&#x200B;*将链接*&#x200B;拖出&#x200B;*输入*&#x200B;连接器来显示“节点”菜单，则该列表包括其&#x200B;*输出*&#x200B;的数据类型与&#x200B;*选定的输入*&#x200B;数据类型匹配的节点

![已筛选的节点创建](main-mdl-graph-concepts.resources/mdl-filtered-node-creation.gif "已筛选的节点创建")

*在MDL图形中创建筛选的节点，请注意列表根据连接器的值类型更改*

## 图形输入和纹理

MDL材质可从外部源接收数据，例如以值和纹理的形式接收。 这是通过<b>公开节点</b>来实现的，而与[Substance图](../../compositing-graphs/substance-compositing-graphs.md)相反，在该图中存在用于此目的的专用输入节点。

根据公开节点的&#x200B;*类型*，可以将数据传递给该节点。 例如，可以将浮点值传递到公开的<b>浮点</b>节点，而将纹理传递到公开的<b>颜色</b>节点（在这种情况下，将采样像素的RGBA值作为颜色值传递）。

![公开图形输入](main-mdl-graph-concepts.resources/mdl-graph-inputs-samplers.png "公开图形输入")

*公开节点创建图形输入，这些输入是纹理的原始值输入和取样器*
