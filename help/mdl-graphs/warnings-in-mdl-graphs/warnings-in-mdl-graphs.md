---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/warnings-in-mdl-graphs.html"
breadcrumb-title: ''
description: 了解并解决MDL图形中的警告，以确保正确的材料定义和渲染。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Warnings in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL图表中的警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# MDL图表中的警告

此页面列出了[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中的MDL图形可能触发的警告和错误消息，并且提供了针对每个警告和错误消息的常见故障诊断步骤。

警告显示在[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中图形资源的警告图标的工具提示中，如果加载了图形，则也会显示在[图形视图](../../interface/the-graph-view/the-graph-view.md)的左下角。

>[!NOTE]
>
> 此部分中的插图记录在<b>Substance模型图表</b>中，这些图表在Substance 3D Designer版本<b>13.0.0</b>中&#x200B;*已弃用*。 但是，它们也适用于MDL图形。

## ![（错误）](../../assets/error.svg)未定义输出节点

图形未定义输出节点。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

选择图形中任何输出类型与此函数的预期类型匹配的值的节点（如果有），然后单击RMB并选择上下文菜单中的<b>设置为根</b>选项或双击节点上的LMB。\
Substance模型图表的输出节点被着色&#x200B;*橙色*。

![“未定义输出节点”解决方案](../../assets/warnings-model-output.gif "“未定义输出节点”解决方案")

### ![（错误）](../../assets/error.svg)至少有一个输入值被拒绝

为参数提供的值不会导致节点的有效计算。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

调整该值，使其与目标参数相符。

![“至少有一个输入值已被拒绝”解决方案](../../assets/warnings-model-rejected-value.gif "“至少有一个输入值已被拒绝”解决方案")

### ![（错误）](../../assets/error.svg)没有输入值

未提供节点预期执行其计算的输入值。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

如果未向某些节点的输入连接器提供数据，则这些节点参数无法回退到默认值。 场景输入通常就是这种情况。

将节点输入连接到另一个节点的匹配类型的输出连接器。

![“无输入值”解决方案](../../assets/warnings-model-no-input-value.gif "“无输入值”解决方案")

### ![（错误）](../../assets/error.svg)节点未计算

提供给节点的信息不完整或无效，因此节点无法执行计算。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

在图形中转到上游，并检查由问题触发的警告，这些问题导致节点无法提供有效输出。

![“Node not computed”解决方案](../../assets/warnings-model-no-input-value.gif "“Node not computed”解决方案")

### ![（错误）](../../assets/error.svg)引用的数据有一些警告

节点引用的资源具有一个或多个警告。 以下是引用资源的一些节点：

* 图形实例节点引用图形
* 场景资源节点引用位图3D场景资源

<b>！[(tick)](../../assets/check.svg)解决方案</b>

在资源管理器面板中，查找引用的资源，并解决该资源引发的所有警告：

* 有关图表，请参阅本页中的其他项目
* 有关任何其他类型的资源，请参阅“来自依赖项的警告”页

![&#39;引用的数据有一些警告&#39;解决方案](../../assets/warnings-model-referenced-data.gif "&#39;引用的数据有一些警告&#39;解决方案")

### ![（错误）](../../assets/error.svg)未找到引用的资源

在Substance 3D文件(SBS)中保存的路径中找不到节点引用的资源。 以下是引用资源的一些节点：

* 图形实例节点引用图形
* 场景资源节点引用位图3D场景资源

<b>！[(tick)](../../assets/check.svg)解决方案</b>

对于图形实例节点

检查源图形是否存在于包中，该包位于保存在其<b>包</b>属性中的路径中。\
否则，请删除该实例节点，并将其替换为引用有效包的实例节点。 或者，您可以重新创建实例节点引用的包和图形，然后通过在[资源管理器](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion)面板中单击该主机包上的&#x200B;*RMB*&#x200B;并在上下文菜单中选择<b>重新加载</b>选项来重新加载该主机包。

对于场景资源节点

在[资源管理器](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion)面板中查找引用的资源，并检查这些资源存在于保存在其<b>文件路径</b>属性中的位置。\
否则，请在资源管理器中单击资源项上的&#x200B;*RMB*，然后选择<b>迁移……上下文菜单中的</b>选项为该资源设置新的有效目标文件。

![“未找到引用的资源”解决方案](../../assets/warnings-model-referenced-resource.gif "“未找到引用的资源”解决方案")

### ![（错误）](../../assets/error.svg)软范围不包含值

公开参数的默认值不包括在为该参数定义的可变范围中。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

调整默认值或软范围，使前者包含在后者中。

>[!NOTE]
>
> 此警告无法通过用户界面触发，因为它&#x200B;*自动调整*&#x200B;软范围以包含默认值。 仅直接修改Substance 3D文件(SBS) **&#x200B;中的数据，会导致触发此警告。

![&#39;软范围不包含值&#39;解决方案](../../assets/warnings-model-ranges.gif "&#39;软范围不包含值&#39;解决方案")

### ![（错误）](../../assets/error.svg)软范围超出硬范围

和公开参数的软范围并不完全包含在为该参数定义的硬范围中。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

调整软范围或硬范围，使前者完全包含在后者中。

>[!NOTE]
>
> 此警告无法通过用户界面触发，因为它&#x200B;*自动调整*&#x200B;软范围以完全包含在硬范围中。 仅直接修改Substance 3D文件(SBS) **&#x200B;中的数据，会导致触发此警告。

![“软范围”超出硬范围“解决方案](../../assets/warnings-model-ranges.gif "”软范围“超出硬范围”解决方案")

### ![（错误）](../../assets/error.svg)值超出硬范围

公开参数的默认值不包括在为该参数定义的硬范围中。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

调整默认值或硬范围，使前者包含在后者中。

>[!NOTE]
>
> 此警告无法通过用户界面触发，因为它&#x200B;*自动调整*&#x200B;要包括在硬范围中的默认值。 仅直接修改Substance 3D文件(SBS) **&#x200B;中的数据，会导致触发此警告。

![“值超出硬范围”解决方案](../../assets/warnings-model-ranges.gif "“值超出硬范围”解决方案")
