---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中创建材料定义语言图形，以创建自定义材料。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建MDL图形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2a6e26cc03e887569a518cadd171ae1b51ae6abd
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# 创建MDL图形

本页介绍了在Substance 3D Designer中创建用于创作MDL 材质的MDL 图的过程。

![MDL 图创建路径](creating-an-mdl-graph.resources/mdl-new-graph-hl.png "MDL 图创建路径")

*在Designer界面中创建新MDL 图的路径*

## 创建MDL 图的方法

您可以使用以下任一方法创建MDL 图：

* 在&#x200B;*主菜单栏*&#x200B;中选择&#x200B;**文件>新建>MDL 图**&#x200B;选项
* 单击&#x200B;*主工具栏*&#x200B;中的![](creating-an-mdl-graph.resources/mdl-new-graph-icon.png) **添加MDL 图**&#x200B;按钮
* 右键单击&#x200B;**资源管理器**&#x200B;面板中的&#x200B;*现有包*，然后选择&#x200B;**新建>MDL 图**&#x200B;选项

您将看到&#x200B;**新建MDL 图**&#x200B;对话框，请参阅下文。

![新建MDL 图对话框](creating-an-mdl-graph.resources/mdl-templates.png "新建MDL 图对话框")

*新建MDL 图对话框*

## “新建MDL 图”对话框

无论使用哪种方法创建新MDL 图，您都会看到<b>新建MDL 图</b>对话框，您可以使用该对话框配置新图形。

### 模板

通过<b> Templates</b>部分，您可以选择图形模板，其中包括预配置的节点，以便您更快地开始使用图形。 预配置节点包括“输出”节点、用于将值传递到这些输出的简单节点（例如，统一颜色）以及取决于模板的输入节点。

若要从完全为&#x200B;*空白*&#x200B;的图形开始，请选择<b>空白</b>模板。

使用<b>项目</b>选项，您可以按项目文件筛选模板列表。 这样，在项目文件的“项目设置”的<b>“常规”</b>部分下添加的位置中可以轻松找到自定义模板。

>[!WARNING]
>
> 如果选择了错误的模板，则在创建模板后&#x200B;*无法*&#x200B;切换到其他图形。\
> 要将现有图形移植到其他模板，您可以使用适当的模板创建新图形，并将图形复制粘贴到新图形。 根据需要重新连接节点，包括[根](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)节点。

可以使用&#x200B;**项目**&#x200B;组合框旁边的&#x200B;*按钮*&#x200B;以不同模式显示模板列表：

* **![](creating-an-mdl-graph.resources/mdl-template-recent-icon.png)显示最近使用的模板**：筛选列表以显示最近使用的模板，其顺序为&#x200B;*最近到最近最少*，顶部项是最近使用的项
* **![](creating-an-mdl-graph.resources/mdl-template-graphs-icon.png)显示图形**：模板按其&#x200B;*仅标签*&#x200B;显示，按模板目录中的[Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html)文件的顺序
* **![](creating-an-mdl-graph.resources/mdl-template-packages-icon.png)显示Substance 3D文件**：按照模板目录中文件的顺序，模板按其标签显示为&#x200B;*它们所属的Substance 3D文件的子级*
* **![](creating-an-mdl-graph.resources/mdl-template-directory-icon.png)显示目录**：模板按其标签显示为其所属目录的&#x200B;*子级*，顺序为模板目录中的文件

### 属性

<b>图形属性</b>部分允许您设置有关新图形的基本信息。 您可以随时更改这些设置，但是首先关注这些设置并根据您的用例进行适当设置是有意义的。

* <b>图形名</b>：图形的标识符。 它对于给定的包需要是唯一的，并且不能包含空格和某些特殊字符。
* <b>在包中创建图形</b>：您可以使用此组合框为新图形创建&#x200B;*新*&#x200B;包，或将新图形添加到已在“资源管理器”面板中加载的任何&#x200B;*现有*&#x200B;包。\
  注意：如果使用方法<b>4</b>启动创建进程（请参阅上文），则此参数是启动该进程时所使用的现有包的&#x200B;*预设*。
* <b>模板详细信息</b>：此部分提供了一个简短文本，用于说明模板的特性和用途
