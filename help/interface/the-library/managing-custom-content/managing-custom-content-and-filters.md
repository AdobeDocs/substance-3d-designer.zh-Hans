---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Library中管理自定义内容和过滤器，以便有条不紊地访问资源。
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 管理自定义内容和过滤器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# 管理自定义内容和过滤器

本页介绍在库中创建类别和过滤器以管理自定义内容的方法。 它还包含基于项目的工作流程建议。

## 概述

[将自定义内容添加到库](../../../interface/preferences-window/project-settings/project-settings.md)后，您需要使其&#x200B;*可发现*。

库使用许多&#x200B;*数据点*&#x200B;来标识内容，以便筛选内容并在搜索中显示。 这些数据点包括：

* 名称
* 扩展名
* URL （即&#x200B;*文件名*）
* 属性

您可以将<b>库</b>组织为包含特定筛选器的类别，并根据项目的需要对其进行定制。\
事实上，自定义类别和筛选器可以&#x200B;*特定于项目*，并保存在[项目文件](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbsprj)中。 然后，可以将这些文件组合到[配置文件](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbscfg)中并分发给团队，以便艺术家们可以针对任何给定项目使用*&#x200B;相同的<b>库</b>类别*。

这意味着，对于一个或多个项目文件，您可以设置应添加到<b>库</b>中的内容的文件夹，以及将对内容进行排序和组织的类别和过滤器。

![库中的自定义内容](managing-custom-content-and-filters.resources/library-filters.png "库中的自定义内容")

## 图形属性

可以使用图表属性的[属性](../../../compositing-graphs/graph-parameters/graph-parameters.md)部分中的数据集，在库中&#x200B;*筛选和搜索*&#x200B;包含[SBS](../../../getting-started/overview/overview.md)和[SBSAR](../../../getting-started/overview/overview.md)文件中的图表。 也可以在某些其他[资源类型](../../../resources/resources.md)上设置其中一些属性。

## 自定义筛选器和文件夹

Filters是简单的布尔型(True/False)搜索参数，当选择<b>Filter</b>时，将导致资源显示在库中。 资源可以是任何保存在包中的资源。 请牢记下列事项：

* <b>筛选器</b>将与&#x200B;*所有监视路径*&#x200B;下的所有资源匹配。
* <b>筛选器</b>可以包含多个条件，*所有条件的计算结果必须为True* (AND-condition)，资源才会显示在该筛选器中。
* [资源](../../../resources/resources.md)可以显示在多个筛选器中，它&#x200B;*不专属于任何筛选器*。
* 通过使用<b>搜索</b>函数，监视路径中的[资源](../../../resources/resources.md)在<b>库</b>中&#x200B;*仍然可用*，即使它在任何<b>筛选器</b>下&#x200B;*不是*。

### 如何创建筛选器和文件夹

使用下列按钮创建和编辑类别（即文件夹）和过滤器：

<b>![](managing-custom-content-and-filters.resources/library-icon-new-folder.png)添加文件夹： </b>在库视图中创建一个可展开的文件夹。 您&#x200B;*无法*&#x200B;创建子文件夹。

<b>![](managing-custom-content-and-filters.resources/library-icon-new-filter.png)添加筛选器：</b>在所选文件夹中添加新的筛选器。 您&#x200B;*无法*&#x200B;将筛选器添加到现有的默认文件夹。

<b>![](managing-custom-content-and-filters.resources/library-icon-edit.png)编辑项：</b>编辑当前选定的文件夹或筛选器。 您&#x200B;*无法*&#x200B;编辑默认文件夹和筛选器的任何属性。

要&#x200B;*删除*&#x200B;文件夹或筛选器，请&#x200B;*右键单击该文件夹或筛选器*，然后从上下文菜单中选择<b>删除</b>选项。

### 编辑筛选器和文件夹

<b>文件夹</b>和<b>筛选器</b>由以下数据标识：

* <b>名称</b>显示在库树视图中。
* 存储此项的[项目配置文件(SBSPRJ)](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)。

>[!WARNING]
>
> *非常*&#x200B;重要的是正确设置这些项，以确保您正在编辑&#x200B;*正确的项目*！

![自定义筛选器版本](managing-custom-content-and-filters.resources/library-filters-edit.png "自定义筛选器版本")

**筛选器**&#x200B;通常需要设置&#x200B;*条件*&#x200B;才能达到其筛选目的。 可使用以下条件配置这些条件：

* **资源类型**：设置特定的[资源类型](../../../resources/resources.md)，如[图表](../../../compositing-graphs/substance-compositing-graphs.md)
* **属性**&#x200B;将条件应用于 — 请参阅上面的列表
* **条件逻辑**：允许筛选器包含正匹配、负匹配、部分匹配和完全匹配的结果
* **条件关键字：**&#x200B;用来测试&#x200B;**属性**&#x200B;和&#x200B;**条件逻辑**&#x200B;条件的字符串。 如果留空，则包含与这两个条件匹配的任何资源

您可以使用Condition关键字最右边的“**+**”和“**x**”按钮&#x200B;*添加或删除*&#x200B;条件。

>[!NOTE]
>
> 不设置任何条件的筛选器将导致显示&#x200B;*所有* **库**&#x200B;内容。

## 最佳实践

### 建议的准则

* 默认库的一般规则是<b>Folder</b>列在<b>Category</b>属性中，而<b>Filter</b>名称由<b>Tag</b>属性决定
* 不要创建与默认库混合的自定义节点，除非您&#x200B;*明确*&#x200B;希望它们这样做。 如果您的节点&#x200B;*将*&#x200B;显示在默认筛选器下（如果它们匹配），因此您必须确保使用&#x200B;*不同的标记/命名系统*&#x200B;以避免出现这种情况
* 使用&#x200B;*唯一*、*每个项目*&#x200B;标识符。 只要在所有项目之间&#x200B;*一致*，即可将这些内容放在您想要的任何位置（如<b>描述</b>、<b>类别</b>或<b>用户数据</b>）。 这使按项目&#x200B;*搜索和筛选内容*&#x200B;更加容易
* 使用<b>Author</b>属性可以跟踪最初负责内容的人员，而无需通过版本控制记录执行挖掘操作
* 创建<b>图标</b>的一种有效方法是使用[图标](../../../compositing-graphs/graph-parameters/graph-parameters.md)图形属性的<b>生成</b>选项，或创建用于生成图标的图形[模板](../../../interface/preferences-window/project-settings/project-settings.md)。 这样您就可以确保一致性，并保存创建它们的工作。 所有默认库图标都是通过这种方式在Designer中创建的！

### 管理不同范围的内容

* 如果这更有意义，您可以将资源添加到&#x200B;*现有类别*。 管理和维护滤镜将减少工作量，您可以使用特殊的图标样式&#x200B;*将它们区分开来*。
* 您可以在&#x200B;*全局*（studio级别）[项目配置文件](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)中定义文件夹和筛选器，然后仅通过从&#x200B;*连续* [项目文件](../../../interface/preferences-window/project-settings/project-settings.md)添加监视路径来向其添加内容
* 您可以为&#x200B;*每个项目*&#x200B;定义特定的文件夹和筛选器以保持它们分开
* 您可以混合、匹配和使用上述所有三种方法：使用现有过滤器、定义新的全局过滤器以及创建每个项目的独特过滤器
