---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: 使用图形实例和子图创建可重复使用的图形组件和模块化材料工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图形实例和子图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# 图形实例和子图

![](graph-instances-sub-graphs.resources/sub-graph.png)

图形实例是<b>引用其他图形</b>的节点。 主机图形中的实例化引用的图形可以称为主机图形的<b>子图</b>。

使用实例可使图形在一个或多个图形中多次重复使用，甚至跨不同的包重复使用。

## 为什么应使用图形实例？

<b>将图形拆分为多个子图</b>可让您更有效&#x200B;*工作*<b>。</b>

任何时候在Designer中复制节点链时，您都可能会将该链拆分为一个子图，以便更轻松地重复使用和更新。

>[!NOTE]
>
> 在本文档的[示例图形](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)部分提供了演示&#x200B;*自定义*&#x200B;筛选器的子Substance的简单设置的项目文件。

### 如何创建图形实例？

将图形A从资源管理器拖动到另一个图形B中，以创建引用图形A的<b>实例化</b>。

通过选择节点并使用上下文菜单中的“从所选对象创建图形”可将图形快速拆分为新节点。 然后，系统会提示您设置新图形的标识符（应该是唯一的）。

请注意，如果所选节点已连接到图形中的其他节点，则您还应在新图形中创建[输入](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)和[输出](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点，以便将这些连接传递到子图。

此外，用引用新图形的实例化替换原始节点之后应手动执行。

最后，您应决定在将项目发布到可共享的Sbsar 文件时是否将子图公开给用户。 请参阅[图形属性](../../../compositing-graphs/graph-parameters/graph-parameters.md)中的“公开于SBSAR”参数。

### 关于继承的一句话

使用子图的另一个好处是，子图的每个实例都可以<b>适应要用到的上下文</b>。 换句话说，同一图形的两个实例可以具有不同的输出分辨率、位深和拼贴模式。

这是在图形中工作的<b>基本概念</b>，当您准备好进一步处理Substance时，我们强烈建议您详细了解[在实例图形中继承](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。

请注意，虽然图形实例和子图概念也适用于Substance功能图形，但该页中所讨论的继承仅适用于Substance图形。

### 能否将自己的图形实例添加到节点库？

<b>可以，可以</b>，但需要进行一些特定设置。 在本文档的[管理自定义内容和筛选器](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)页面中了解详情。

### 是否可以检查图形实例的源图形？

![（刻度）](graph-instances-sub-graphs.resources/check.svg)是，对于从&#x200B;**Substance 3D文件(SBS)**&#x200B;加载的图形实例，*仅*。 这些实例化具有&#x200B;*深红色*&#x200B;标签。\
右键单击节点以打开其上下文菜单，然后选择&#x200B;**打开引用**&#x200B;选项。

>[!NOTE]
>
> 检查源图形时，如果[首选项](../../../interface/preferences-window/preferences-window.md)的&#x200B;**图形**&#x200B;部分中的&#x200B;**In-context editing**&#x200B;选项为&#x200B;*已选中*，则可以使用实例图形的输入数据。

![（减号）](graph-instances-sub-graphs.resources/forbidden.svg) *不能*&#x200B;检查从&#x200B;**Substance 3D资源(SBSAR)**&#x200B;图形加载的实例，因为这些实例已编译。 您只能在&#x200B;**资源管理器**&#x200B;面板中加载资源以检查公开的图形列表及其参数。 这些实例化具有&#x200B;*绿色*&#x200B;标签。\
右键单击节点以打开其上下文菜单，然后选择&#x200B;**加载包**&#x200B;选项。

>[!NOTE]
>
> **原子节点**
> 
> *原子*&#x200B;节点是通过代码在引擎中直接实现的，并且是&#x200B;*不是*&#x200B;图形的实例，因此其名称为atomic：它们是[Substance图形](../../../compositing-graphs/substance-compositing-graphs.md)中&#x200B;*所有*&#x200B;其他节点的&#x200B;*最小构造块*。
