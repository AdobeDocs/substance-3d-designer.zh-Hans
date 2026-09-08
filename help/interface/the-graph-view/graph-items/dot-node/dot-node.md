---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/the-graph-view/graph-items/dot-node.html"
breadcrumb-title: ''
description: 在Substance 3D Designer中使用点节点和门户节点创建连接点并组织图形流。
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 点节点（也称为门户）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---


# 点节点（也称为门户）

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![点节点图标](../../../../assets/graphatomic-dot_1.png "点节点图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>点</b>节点是一个帮助程序，它允许您通过重新路由和分组连接来简化和清理图表。 对于许多长连接运行在其他连接或节点上的图形，此选项特别有用。

一对“点”节点可以作为<b>门户</b>来隐藏远距离连接，或用于路由连接可能具有挑战性的地方。

</td>
</tr>
</table>

## 创建点节点

可以通过以下任何方式以任意图形类型添加点节点：

+++在链接上插入
悬停连接时按住<b>Alt</b>键可显示“点”节点预览，然后单击LMB可在该位置的连接上添加“点”节点。

![插入点节点](../../../../assets/dot-node-insert-optim.gif "插入点节点"){width="512px"}



+++

+++节点连接器
从节点连接器拖动新连接时按<b>Alt</b>键，以便在该位置插入点节点。

您可以继续拖动新连接，并重复该操作以您喜欢的方式路由该连接。

![点：从连接器创建](../../../../assets/graph-dot_create-from-connector.gif "点：从连接器创建")



+++

+++节点菜单
按<b>空格键</b>显示<b>节点菜单</b>，然后选择“点”项或在搜索字段中键入“点”以呈现该项并更快地找到它。

![节点菜单中的点节点](../../../../assets/dot-node-insert-menu.png "节点菜单中的点节点")



+++

>[!TIP]
>
> 创建“点”节点时，其“名称”属性会自动获得焦点，以便您可以立即编辑节点的名称。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 合并链接

按ALT并在链接上移动点节点可将多个节点连接合并在一起。

</td>
<td style="border: 0;" valign="top">

![合并链接](../../../../assets/dot-node-congrenate-links-optim.gif "合并链接"){width="512px"}

</td>
</tr>
</table>

## 门户

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![点节点作为入口 — 图标](../../../../assets/DotNode_Portal-1.png "点节点作为入口 — 图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

点节点可以作为<b>门户</b>用于在图表中远距离发送数据，而不会具有妨碍可读性的繁琐的长链接。 这有效地隐藏了Dot节点之间的链接。

</td>
</tr>
</table>

![点节点作为门户](../../../../assets/DotNode_Portal.gif "点节点作为门户")

### 创建门户

当发射机点节点被命名时，在两个点节点（发射机和接收机）之间自动创建入口。 点节点命名是通过在其<b>名称</b>属性中设置唯一标识符完成的。

当图中存在一个或多个命名的Dot节点时，可通过以下方式将任何Dot节点作为接收器连接到该节点：

* 在接收机的输入和发射机的输出之间建立链路；
* 在接收方的<b>输入门户</b>属性中选择发射方的名称。

复制或复制接收器可将它们与发射器的连接保留为入口。

### 正在识别门户

用作入口的点节点在用作入口的连接器旁有一个无线信号图标。

选择用作入口的任何“点”节点时，会以虚线的形式显示与其他入口的隐藏连接。

### 删除门户

当发射器的<b>名称</b>被清除或隐藏的连接被删除时，入口将被删除：

* 选择一个门户，然后选择隐藏的连接并将其删除；
* 选择接收器，然后按“属性”中<b>输入门户</b>下拉列表旁边的<b>X</b>按钮。

>[!IMPORTANT]
>
> [FX-Map graphs](../../../../function-graphs/fxmaps/fxmaps.md)不支持将点节点用作门户。

查看此教程，了解将“点”节点作为门户：
