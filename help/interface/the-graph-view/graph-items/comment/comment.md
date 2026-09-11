---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: 向Substance 3D Designer图表添加注释，以记录您的工作流程并解释节点连接。
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 注释
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4b938349fed501f5f6b3e3a70a1006519749e4e1
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# 注释

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![注释图标](comment.resources/graphatomic-comment_1.png "注释图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

注释只是可放置在图表中任意位置的一段自由浮动文本。

用于注释和解释图表的各个部分。 其<b>Description</b>属性包含要显示的文本。

</td>
</tr>
</table>

>[!NOTE]
>
> 注释具有自动换行功能，旨在最大程度地减少它们在图表中的占用空间。

## 创建注释

默认类型的注释独立于图形中的节点放置。

可以通过以下方式创建它：

+++节点菜单
在图形视图中按<b>空格键</b>以打开<b>节点菜单</b>，然后在列表中选择“注释”项。

在搜索字段中键入“comment”以显示项目并更快地找到它。

+++

+++快捷键
如果将键盘快捷键映射到[首选项](../../../../interface/preferences-window/preferences-window.md)中的“注释”项，请在图形视图具有焦点时按该快捷键。

+++

+++上下文菜单
在图表视图中，按任何对象或空白空间上的<b>RMB</b>并选择<b>添加注释</b>选项。

+++

+++图形工具栏
在“图形视图”工具栏中，单击<b>节点调板</b>中的“注释”按钮。

+++

+++库
在“库”中，选择<b>图形项目</b>类别，然后将“注释”项目拖放到图形视图中。

+++

>[!TIP]
>
> 创建注释后，其“描述”属性会自动获得焦点，因此您可以立即编辑注释的文本。

## 父注释

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

带父级的注释是一条&#x200B;*附加到图形中特定节点*&#x200B;的注释，这样在移动节点时，该注释会随之出现，并且在删除节点时，该注释也会随之删除。

当前选择&#x200B;*单个*&#x200B;节点时或通过单个节点的上下文菜单创建的注释是该节点的父级。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![注释：父注释](comment.resources/graph-comment_parented.gif "注释：父注释")

</td>
</tr>
</table>

## HTML格式设置

可以使用HTML标记设置文本的格式。 在注释的<b>Description</b>属性中，使用![](comment.resources/graph-frames_html-markup-button.png) <b>HTML标记</b>按钮切换此格式。

>[!TIP]
>
> 请在[帧](../../../../interface/the-graph-view/graph-items/frame/frame.md)文档的<b>描述</b>部分中了解有关此功能的更多信息。

![注释：HTML标记](comment.resources/graph-comment_html-markup.gif "注释：HTML标记")
