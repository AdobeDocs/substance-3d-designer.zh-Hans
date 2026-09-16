---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/properties.html"
breadcrumb-title: ""
description: 使用Substance 3D Designer中的“属性”面板查看和编辑节点属性和图形参数。
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 属性
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%
---

# 属性

此页面显示Substance 3D Designer的<b>“属性”</b>面板、其布局以及您可以在其中找到的不同转出次数和类别及参数。 它关注[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)的属性。 [函数图](../../function-graphs/function-graphs.md)和[FX-Map图](../../function-graphs/fxmaps/fxmaps.md)的布局更简单。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概述

<b>属性</b>面板是一个上下文相关面板，它根据您在[图形视图](../../interface/the-graph-view/the-graph-view.md)和[资源管理器](../the-explorer-window/the-explorer-window.md)窗口中的选择而发生变化。

</td>
<td style="border: 0;" valign="top">

![属性程序坞](properties.resources/image2020-11-9-13-49-48.png "属性程序坞")

</td>
</tr>
</table>

它允许您更改所选节点和资源的属性以及[图形视图](../../interface/the-graph-view/the-graph-view.md)，这大概是您在Designer中第二常用的UI面板。

“Properties”（属性）面板根据您的选择拆分为几个不同的发布，例如：

* 节点的<b>基本参数</b>和<b>输入 — </b>或<b>特定参数</b>
* 大多数节点和包的<b>属性</b>和<b>元数据</b>

Substance生态系统的一个关键功能[公开参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)是通过“属性”面板完成的。

>[!NOTE]
>
> 大多数数字字段支持&#x200B;*基本数学公式*&#x200B;作为输入 — 例如，`17+3.5`、`7/3`、`(4+2)*3`。 按&#x200B;*Enter*&#x200B;验证公式，结果将输入到字段中。 如果公式无效，则字段将恢复为以前的值。\
> 应用程序其他部分中的某些数字字段（如[公开参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)对话框）也支持此功能。

## 节点和Substance图

节点和[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)具有稍微重叠的一组属性类别，并且它们的功能相似。

节点和图形之间的<b>基本参数</b>和<b>属性</b>相同。

节点提供<b>特定参数</b>或<b>实例参数</b>（取决于它们是[原子节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)还是[实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)）以及<b>输入值</b>，用于处理[值](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)。

[输入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md)和[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)原子节点是例外，因为它们具有<b>集成属性</b>和<b>条件</b>以提高可见性。 这两组属性也可以在“图形”属性中的“输入”和“输出”下集中访问。

图表有几个额外的类别。 <b>输入参数</b>列出了[公开的参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)、<b>输入</b>和<b>输出</b>列出输入和输出节点的所有属性。 [您可以在专用页面上找到所有详细说明的图形属性。](../../compositing-graphs/graph-parameters/graph-parameters.md)

## 资源和包

“属性”面板还会响应[资源管理器](../the-explorer-window/the-explorer-window.md)中的选择更改。 它可以作为选择图表的另一种方式（而不是双击空白区域），并允许您更改包和[资源](../../resources/resources.md)属性。

包包含&#x200B;**信息**、**属性**&#x200B;和&#x200B;**元数据**&#x200B;部分。 [包元数据是在专用页面上描述的。](../../package-metadata/package-metadata.md)

资源具有特定于其类型的属性，[详细描述专用页](../../resources/resources.md)。
