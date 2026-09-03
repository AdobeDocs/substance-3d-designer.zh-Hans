---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/warnings-and-errors.html"
breadcrumb-title: ''
description: 在Substance 3D Designer中查找常见警告和错误的解决方案，以快速解决问题。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Warnings and errors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 警告和错误
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 6%

---


# 警告和错误

此页面解释了[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中可能显示的警告和错误消息的报告，以及指向基于警告源的警告疑难解答的链接。

## 概述

在Designer中处理项目时，您可能会遇到警告和错误消息，这些消息会通知您项目中存在一个问题：

* **警告**&#x200B;以&#x200B;*黄色*&#x200B;文本显示，并提请您注意由于缺少输入或配置错误而可能导致不良结果的问题。 他们通常&#x200B;*不屏蔽*&#x200B;您的工作。
* **错误**&#x200B;以&#x200B;*红色*&#x200B;文本显示，表示计算失败、结果意外或无法执行任务。 他们通常&#x200B;*阻止*&#x200B;您的工作。

通常，警告和错误会显示在触发警告和错误的项上，并且&#x200B;*将显示在该项的每个主页*&#x200B;中。 以下是报告警告和错误的常见位置列表：

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 资源管理器

对于[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中有警告的任何项目，该警告在列表中项目的最右边缘显示有一个![](warnings-and-errors.resources/warnings-and-errors-01.png)图标。 将光标置于该图标上几秒钟，以显示&#x200B;*工具提示*，其中详细列出了所有警告。

它们遵循以下规则：

* 如果项目嵌套在任何其他项目（如文件夹）下，则折叠该项目时会显示警告。
* 警告列表是&#x200B;*累计*，因为它们是项警告&#x200B;*和*&#x200B;所有已显示其子项警告的总和。
* 包的内容报告的所有警告都出现在&#x200B;*包*&#x200B;项中，并添加到包的&#x200B;*自己的*&#x200B;警告中。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warnings-and-errors-02.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 图形视图

对于[图形视图](../../interface/the-graph-view/the-graph-view.md)面板中有警告的任何项目，该警告在视区的&#x200B;*左下角*&#x200B;以彩色文本显示。 如果警告是由特定节点触发的，则该节点将具有![](warnings-and-errors.resources/warnings-and-errors-03.png)警告标记。 将光标置于该徽章上几秒钟，以显示&#x200B;*工具提示*，其中详细列出了所有警告。

它们遵循以下规则：

* 如果源图形&#x200B;*实例化*&#x200B;到任何其他主机图形中有一个或多个警告，则该源图形的[实例节点](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)将有&#x200B;*单个* `The referenced data has some warnings`警告。
* 警告列表是&#x200B;*累积*，因为它们是图形警告&#x200B;*和*&#x200B;其子节点的所有警告的总和。
* 在“资源管理器”面板中表示该图表的项上报告该图表的所有警告。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warnings-and-errors-04.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 属性

对于[属性](../../interface/properties/properties.md)面板中带有警告的任何项目，该警告在列表中该项目的最右边缘显示有一个![](warnings-and-errors.resources/warnings-and-errors-01.png)图标。 将光标置于该图标上几秒钟，以显示&#x200B;*工具提示*，其中详细列出了所有警告。

它们遵循以下规则：

* 如果项目嵌套在任何其他项目（例如，节标题）下，则折叠该项目时会对该项目显示警告。
* 警告列表是&#x200B;*累计*，因为它们是项警告&#x200B;*和*&#x200B;所有已显示其子项警告的总和。
* 如果应用于[输入参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)的[函数图形](../../function-graphs/function-graphs.md)有一个或多个警告，则参数项将有&#x200B;*单个* `The [x] parameter's function has some warnings`警告。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warnings-and-errors-05.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### 控制台

在&#x200B;**控制台**&#x200B;面板中报告警告和错误，可通过[主菜单](../../interface/the-main-toolbar/the-main-toolbar.md)中的&#x200B;**Windows**&#x200B;菜单访问该面板。 通过将&#x200B;**通道**&#x200B;设置设为`ErrorMgr`，可以将警告和错误从控制台的其余条目中分离出来。

>[!NOTE]
>
> 由于控制台中的所有文本均为&#x200B;*可选*，因此您可以使用此面板来&#x200B;*轻松复制警告和错误消息*，并将其粘贴到此文档的&#x200B;**本地搜索**&#x200B;工具或任何Internet搜索引擎中。 这样可加快查找有关故障排除问题的指导的速度。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warnings-and-errors-06.png){width="256px"}

</td>
</tr>
</table>

### 具有“（#次）”的消息

在&#x200B;*完全相同*&#x200B;的警告或错误在项&#x200B;*和*&#x200B;的任何子项上&#x200B;*多次*&#x200B;触发时，这些警告将&#x200B;*合并到一个*&#x200B;中，并显示`(# times)`后缀，以让您了解此警告或错误报告了多少次。

## 类别

以下是Designer中可能遇到的警告和错误的列表，按源进行排序。 类别标题链接到其专用页面，该页面提供了用于解决每个问题的说明和故障排除指南。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Substance 图形中的警告

* 未定义输出节点
* `[x]`参数的函数有一些警告
* 参考数据有部分警告
* 未找到引用资源
* 文本节点使用无效的字体

</td>
<td style="border: 0;" valign="top">

### 函数图表中的警告

* 未定义输出节点
* 当前输出节点返回x类型的值
* 某些Get节点没有变量名称
* 某些“集”节点没有变量名称

</td>
</tr>
</table>

### 依赖项中的警告

* 依赖包无效
* 检查项目中是否定义了别名“x”
* 无法找到与此资源匹配的文件
* 未找到链接的文件
* 未找到色彩空间
* 未找到引用资源
* UV磁贴被分配多次
* 无效的UV磁贴
