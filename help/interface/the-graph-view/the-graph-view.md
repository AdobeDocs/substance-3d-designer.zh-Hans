---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/the-graph-view.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Designer中的图形视图创建和编辑基于节点的材质图形。
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图形视图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '3558'
ht-degree: 0%

---


# 图形视图

此页面显示Substance 3D Designer的“图形”视图停靠区。

图表视图是[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)的主窗口，您可以在其中创作和编辑图表。 图形视图有两个主要区域：顶部有一个工具栏，可快速访问某些功能，还有放置节点的实际图形区域。

图表视图用于所有图表类型，但[Substance图表](../../compositing-graphs/substance-compositing-graphs.md)、[函数图表](../../function-graphs/function-graphs.md)和[FX-Map图表](../../function-graphs/fxmaps/fxmaps.md)之间略有不同，主要是在工具栏区域。

## 视区导航

可使用以下操作导航图形：

* <b>声像：</b> MMB / Ctrl+RMB
* <b>缩放：</b>鼠标滚轮/Alt + RMB

使用触控板（仅限macOS）

* <b>平移： </b>两指轻扫
* <b>缩放：</b>两指捏合/在按住Cmd时两指轻扫

>[!NOTE]
>
> 缩放方向
> 
> 每种缩放方法都会与另一种方法反转：
> 
> * 鼠标滚轮&#x200B;*拉近*&#x200B;图形视图的距离
> * 按住Alt+RMB并向上拖动&#x200B;*推移*&#x200B;图形视图
> 
> 可在[首选项](../../interface/preferences-window/preferences-window.md)中反转缩放方向。

![视区导航](the-graph-view.resources/the-graph-view-01.gif "视区导航")

使用F键将<b>焦点</b>聚焦所选节点，如果未选择任何内容，则聚焦整个图形。

也可以使用<b>导航图钉</b>和F2键进行导航，请参阅下面的[图形项](#graph-items) [。](../../interface/the-graph-view/graph-items/graph-items.md)

## 移动对象

单击对象（即节点或图形项）上的LMB，然后按住并拖动光标以在图形周围<b>移动节点</b>。 如果选择了多个对象，则所有选定对象都将随光标下的对象一起移动。

如果光标<b>在移动对象时到达图形视图的边框</b>，则视图将沿光标的方向平移。 请注意，当光标远离边框时，平移速度会更快。\
这同样适用于跨图形视图边框绘制选择框。

默认情况下，对象在移动时将<b>对齐到网格</b>。 在移动对象时按住Ctrl (Windows) / ⌘ (macOS)可禁用该捕捉。

## 图形项目

有几个辅助对象可用于帮助组织和导航图形，尤其是在图形增长为复杂的节点网络时，这种复杂网络可能难以读取：

<b>点节点</b>允许您重新路由和合并连接，并可用作<b>门户</b>来隐藏长连接或笨重的连接；

<b>帧</b>可帮助您对具有可见标题和颜色编码的节点进行分组；

通过<b>注释</b>，您可以跟踪节点或节点组的用途，并创建任何其他有用的批注；

<b>导航图钉</b>使您能够快速跳转到图表中的目标点。

>[!NOTE]
>
> 请参阅本文档的[图形项](../../interface/the-graph-view/graph-items/graph-items.md)部分中了解更多信息。

## 图形上下文菜单

在图形的空白区域单击RMB时，会出现上下文菜单，并可包含以下选项：

<b>添加节点：</b>打开“节点”菜单以在图形中添加节点；

<b>添加注释：</b>添加无父级的[注释](../../interface/the-graph-view/graph-items/graph-items.md)图形对象；

<b>添加帧：</b>添加[帧](../../interface/the-graph-view/graph-items/graph-items.md)图形对象；

<b>添加pin：</b>添加[Pin](../../interface/the-graph-view/graph-items/graph-items.md)图形对象；

<b>添加点节点：</b>添加[点](../../interface/the-graph-view/graph-items/graph-items.md)节点；

<b>在3D视图中查看输出：</b>通过匹配的使用情况将所有图形的输出分配给[3D视图](../../interface/3d-view/3d-view.md)中的材料，请参阅下面的[与3D视图交互](#interacting-with-the-3d-view)；

<b>在3D视图中重置和查看输出：</b>在[3D视图中重置素材](../../interface/3d-view/3d-view.md)并通过匹配使用实例将图形的所有输出分配给该素材，请参阅下面的[与3D视图交互](#interacting-with-the-3d-view)；

<b>以2D视图查看输出：</b>在[2D视图](../../interface/2d-view/2d-view.md)中显示图形的一个输出，请参阅下面的[与2D视图交互](#interacting-with-the-2d-view)；

<b>计算节点缩略图：</b>触发对图形中所有节点（将存储在[图像缓存](../../interface/preferences-window/preferences-window.md)中）的结果的计算，并使用它们的第一个输出作为其缩略图；

<b>清除节点缩略图：</b>清除包含图形中所有节点结果的[图像缓存](../../interface/preferences-window/preferences-window.md)，这又会清除节点的缩略图；

<b>保存包：</b>保存包含此图表的包；

<b>粘贴：</b>将当前复制到剪贴板中的节点（包括其上游连接）粘贴到光标所在位置。 如果光标不在“图形视图”视口中，则节点将被置于视口的中心。

<b>不带链接粘贴：</b>将当前复制到剪贴板中的节点（不包括其上游连接）粘贴到光标所在位置。 如果光标不在“图形视图”视口中，则节点将被置于视口的中心。

<b>全选：</b>选择图表中的所有节点；

<b>上一个图钉：</b>导航到图形中的上一个[上一个图钉](../../interface/the-graph-view/graph-items/graph-items.md)对象；

<b>下一个图钉：</b>导航到图形中的下一个[图钉](../../interface/the-graph-view/graph-items/graph-items.md)对象；

<b>复制选择：</b>将所选节点、连接和参数值复制到剪贴板；

<b>删除选择：</b>删除所选节点；

<b>删除并重新链接：</b>删除所选节点，如果可能，通过从上游节点到下游节点的直接连接来替换它们；

<b>重复选择：</b>在光标所在位置复制同一图形中的选定节点，包括其上游连接。 如果光标不在“图形视图”视口中，则节点将被置于视口的中心。

<b>重复选择但不包含链接：</b>在光标所在位置复制同一图形中的选定节点（不包括其上游连接）。 如果光标不在“图形视图”视口中，则节点将被置于视口的中心。

<b>选择上游节点：</b>选择所选节点上游的所有节点；

<b>选择下游节点：</b>选择所选节点下游的所有节点；

<b>交换链接\*：</b>交换所选一对输入和输出连接器之间的连接；

<b>禁用节点/选择：</b>禁用选定的节点，以便这些节点对流的结果没有影响，请参阅下面的<b>禁用节点</b>。

<b>\*：</b>仅当选择包含两个链接或三个节点（其中两个节点连接到同一第三个节点的输入）时才可用。

## 使用节点

图主要是节点的容器，节点可以采集、生成和修改数据，然后将其输出为图的结果。 使用节点涉及以下概念和操作。

### 创建和管理节点

无论图形类型如何，节点都可以以5种方式放置到图形中：

* 从节点工具栏上的图标单击或拖动（请参阅下文）。 只能以这种方式放置[原子节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)。
* 右键单击图形的空白区域，然后选择<b>添加节点</b>。 只能以这种方式放置[原子节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)。
* 将缩览图从“库视图”拖动到图形视图中。 此方法适用于[所有类型的节点，包括节点实例](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)。
* 按<b>空格键</b>访问<b>节点菜单</b>。 请参阅以下内容。
* 使用映射到节点的键盘快捷键。 映射在[首选项窗口](../../interface/preferences-window/preferences-window.md)中执行。

![放置节点](the-graph-view.resources/the-graph-view-02.gif "放置节点")

如果在选择另一个节点时放置了某个节点，则Designer将尝试自动将新节点连接到旧节点。\
此自动连接始终将新节点&#x200B;*置于*&#x200B;工作流中的旧节点之后。

删除节点有两种方法，具体取决于您希望如何处理丢失的链接：

* 选择一个节点并按Delete键，或右键单击并选择<b>删除选区</b>。 这将断开所有现有连接，从而可能导致功能损坏。
* 选择一个节点并按Backspace键，或右键单击并选择<b>删除并重新链接</b>。 这将在可能的情况下尝试保留链接，从而防止功能损坏。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 节点菜单

按图表视图中的<b>空格键</b>可显示“节点”菜单。

此菜单通过搜索界面提供对[库](../../interface/the-library/the-library.md)中所有节点的访问，并允许收藏的节点显示在列表顶部。

您可以使用箭头键浏览搜索结果。 列表&#x200B;*循环*，这样在第一个项目上使用“向上”箭头键就可以转到最后一个项目。

搜索为&#x200B;*模糊*，这意味着它原谅搜索词中的细微差异。 例如，“颜色”与“颜色”、“标准化”与“标准化”等。

如果在图形中选择了&#x200B;*单个*&#x200B;节点，或通过拖动节点连接器生成“节点”菜单，则搜索结果将根据输出类型自动&#x200B;*筛选*。\
例如，对于“灰度”类型的输出，仅列出具有“[主输入](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)”类型的“灰度”节点。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![图形视图：节点菜单](the-graph-view.resources/the-graph-view-03.png "图形视图：节点菜单")

</td>
</tr>
</table>

### 选择节点

您可以选择一个或多个节点来复制它们、删除它们、在图形上移动它们等。

若要选择&#x200B;*单个*&#x200B;节点，请将光标置于该节点上，然后单击LMB。

要选择&#x200B;*多个*&#x200B;节点，有以下几种方法可用：

* <b>逐个：</b>按住Ctrl并单击节点上的LMB。 未选中的节点&#x200B;*已添加*&#x200B;到选择中，而选中的节点已从选择中&#x200B;*已删除*；
* <b>选择框：</b>单击图表中空白处的LMB，*按住然后拖动*&#x200B;光标以绘制选择框。 释放LMB时，会选择框中至少部分包括的节点&#x200B;**；
* <b>上游：</b>单击某个节点上的RMB并选择<b>选择上游节点</b>选项：选中该节点以及属于连接到该节点的&#x200B;*输入*&#x200B;的流的所有节点；
* <b>下游：</b>单击某个节点上的RMB并选择<b>选择下游节点</b>选项：将选中该节点以及作为连接到该节点的&#x200B;*输出*&#x200B;的流的一部分的所有节点。

![选择节点](the-graph-view.resources/the-graph-view-04.gif "选择节点")

### 节点上下文菜单

在节点上单击RMB时，会出现上下文菜单，其中可包含以下选项：

<b>以2D视图查看输出：</b>在[2D视图](../../interface/2d-view/2d-view.md)中显示某个节点的输出，请参阅下面的[与2D视图交互](#interacting-with-the-2d-view)；

<b>在3D视图中查看</b>：通过匹配使用实例，将节点的所有输出分配给[3D视图](../../interface/3d-view/3d-view.md)中的材质，请参阅下面的[与3D视图交互](#interacting-with-the-3d-view)；

<b>在3D视图中重置和查看：</b>在[3D视图中](../../interface/3d-view/3d-view.md)重置素材，并通过匹配使用实例将节点的所有输出分配给该素材，请参阅下面的[与3D视图交互](#interacting-with-the-3d-view)；

<b>在3D视图中查看输出\*：</b>通过匹配用法将特定节点输出分配给[3D视图](../../interface/3d-view/3d-view.md)中的材质；

<b>添加注释：</b>创建[注释](../../interface/the-graph-view/graph-items/graph-items.md)图形对象并将其父级到此节点；

<b>添加帧：</b>创建[帧](../../interface/the-graph-view/graph-items/graph-items.md)图形对象并使其适合选定的节点；

<b>将信息复制到剪贴板：</b>将节点的唯一标识符(UID)复制到剪贴板；

<b>公开参数：</b>显示此节点的[公开节点参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)对话框；

<b>创建\*：</b>为此节点的每个输入和/或输出创建输入和/或输出节点；

<b>打开引用\*：</b>将此图形[&#128279;](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)引用的Node 加载为单独的图形视图选项卡；

<b>在上下文中打开引用\*\*：</b>在当前图形的上下文中将此图形[&#128279;](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)引用的节点加载为现有图形视图选项卡中的痕迹导航；

<b>从所选对象创建图形：</b>将所选节点复制到新图形中；

<b>复制选择：</b>将所选节点、连接和参数值复制到剪贴板；

<b>删除选择：</b>删除所选节点；

<b>删除并重新链接：</b>删除所选节点，如果可能，通过从上游节点到下游节点的直接连接来替换它们；

<b>复制选择：</b>在同一图形中复制所选节点，包括其上游连接；

<b>重复选择但不包含链接：</b>重复同一图形中的选定节点（不包括其上游连接）；

<b>选择上游节点：</b>选择所选节点上游的所有节点；

<b>选择下游节点：</b>选择所选节点下游的所有节点；

<b>交换链接\*\*\*\*：</b>交换选定输入和输出连接器对之间的连接；

<b>禁用节点/选择：</b>禁用节点或选定的节点，以便它们不会对流的结果产生影响，请参阅下面的<b>禁用节点</b>。

<b>\*</b>：仅适用于[图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)节点。\
<b>\*\*：</b>仅适用于[图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)节点，并且已在[首选项](../../interface/preferences-window/preferences-window.md)中选中<b>启用上下文编辑</b>选项。\
<b>\*\*\\*：</b>仅当选择包含两个链接或三个节点（其中两个节点连接到同一第三个节点的输入）时才可用。

>[!IMPORTANT]
>
> 如果在将光标&#x200B;*放在节点*&#x200B;上时单击了&#x200B;*人民币*，则无论当前节点中是否选择了其他图形&#x200B;**，这些上下文菜单选项中的几个都将以该&#x200B;*节点*&#x200B;为目标。
> 
> 因此，为了获得一致的可预测结果，建议始终将光标放在节点上，该节点是您实际要用上下文菜单操作作为目标的选择的一部分。

### 连接节点

一个节点A的&#x200B;*输出连接器*&#x200B;可以连接到另一个节点B的&#x200B;*输入连接器*，这将导致节点B使用A的数据输出执行其计算。

>[!NOTE]
>
> 所有连接器都&#x200B;*不必*&#x200B;连接。 将连接器保留为空会导致以下情况：
> 
> * 对于&#x200B;*输入*&#x200B;连接器：节点将回退到为该输入设置的默认值；
> * 对于&#x200B;*输出*&#x200B;连接器：计算图形时会忽略并丢弃数据。

![连接节点](the-graph-view.resources/the-graph-view-05.gif "连接节点")

您可以按&#x200B;*任意顺序*&#x200B;单击每个连接器上的LMB，以<b>创建</b>一个新链接。\
此外，如果在选择节点A的同时创建节点B，则节点A的&#x200B;*第一输出*&#x200B;将自动连接到节点B的&#x200B;*主输入*。

可以在&#x200B;*现有*&#x200B;链接上执行以下操作：

<b>删除：</b>通过单击链接上的LMB并按&#x200B;*Delete*<b>、</b>删除链接，或者按住Alt键并单击任何包含链接的连接。 按住Alt键单击可删除该连接上的所有链接；

<b>复制：</b>通过按住Ctrl键、单击连接器上的LMB并拖动光标来复制链接。 单击另一个连接器上的LMB以连接该链接；

<b>移动：</b>按住Shift键，单击连接器上的LMB并拖动光标，即可选取链接并将链接从连接器移动到另一个连接器。 单击另一个连接器上的LMB以连接链接。

### 正在禁用节点

>[!NOTE]
>
> 这仅适用于[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)。

可以禁用节点，这样它们在图形中&#x200B;*没有效果*，但不需要断开连接或删除。

禁用的节点具有下列行为：

* 它们具有![](the-graph-view.resources/the-graph-view-06.png) <b>已禁用</b>徽章&#x200B;*、*&#x200B;一个&#x200B;*虚线轮廓*&#x200B;和一个内部*重路由*链接，而不是缩略图；
* 节点将输出在其&#x200B;*主输入*&#x200B;中接收的数据；
* 禁用的节点可以&#x200B;*链接在一起*；
* 它们的属性和连接是&#x200B;*未修改的*；
* 其禁用状态为&#x200B;*已保存*，并且在会话间持续存在；
* 在发布到SBSAR时，生成的文件将&#x200B;*考虑了*&#x200B;节点的禁用状态 — 即，您所看到的是您获得的内容。

您可以使用<b>Shift+D</b>击键，或者右键单击图形并选择上下文菜单中的<b>禁用节点/禁用选择</b>项，来禁用一个节点或一组选定的节点。

>[!IMPORTANT]
>
> 只能禁用符合以下条件的节点：
> 
> * 节点至少具有&#x200B;*一个输入*
> * 节点只有&#x200B;*一个输出*
> * 主输入和输出的&#x200B;*类型*&#x200B;必须&#x200B;*匹配* — 即灰度到灰度，颜色到颜色
> * 所有选定节点都必须具有&#x200B;*相同状态* — 即，必须启用所有节点，相同的规则适用于启用节点

![正在禁用节点](the-graph-view.resources/the-graph-view-07.gif "正在禁用节点"){width="512px"}

## 与2D视图交互

>[!NOTE]
>
> 这仅适用于[图形](../../compositing-graphs/substance-compositing-graphs.md)。

要在[2D 视图](../../interface/2d-view/2d-view.md)中显示节点输出，请双击节点上的LMB，或单击节点上的RMB，然后在上下文菜单中选择[在2D 视图中查看输出](#interacting-with-the-2d-view)选项。 如果节点有多个输出，请在子菜单中选择所需的输出。

您可以通过单击[图形视图](https://substance3d.adobe.com/)中的空白区域上的RMB，然后在上下文菜单中选择[在2D视图中查看输出](#interacting-with-the-2d-view)选项，在2D视图中显示任何图形输出。 如果图形有多个输出，请在子菜单中选择所需的输出。

## 与3D视图交互

>[!NOTE]
>
> 这仅适用于[图形](../../compositing-graphs/substance-compositing-graphs.md)。

若要在[3D视图](../../interface/3d-view/3d-view.md)中应用节点输出，请在节点上单击RMB，然后在上下文菜单中选择<b>在3D视图中视图</b>选项。 如果节点有多个输出，请在子菜单中选择所需的输出。 然后，选择当前在3D视图中使用的着色器的目标通道。

（*[仅限图形](../../compositing-graphs/substance-compositing-graphs.md)*）您可以通过单击图形视图中空白区域的RMB，然后在上下文菜单中选择<b>在3D视图中查看输出</b>选项，来应用3D视图中的所有图形输出。 确保图形中存在一个或多个[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点，并且该节点[设置正确](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。

## 工具栏

>[!NOTE]
>
> 完整列表仅适用于[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)。 其他图形类型具有这些选项中的&#x200B;*有限集*。

### 图形工具

主工具栏可以在每种图形类型中找到，并提供常规功能以及切换其他工具栏的可见性。 您可以找到以下函数：

![](the-graph-view.resources/the-graph-view-08.png) <b>焦点选择</b> (F)\
将视图集中在选区上，如果选区为空，则聚焦整个场景。

![](the-graph-view.resources/the-graph-view-09.png) <b>重置缩放</b> (Z)\
将当前缩放级别恢复到默认状态，并将视图置于图形的中间。 可能意味着放大或缩小。

![](the-graph-view.resources/the-graph-view-10.png) <b>导出图形视图\
</b>以1:1的分辨率将完整图形导出为图像。 用于共享整个图形的屏幕截图。

![](the-graph-view.resources/the-graph-view-11.png) <b>节点信息\
</b>*— 显示连接器名称：*&#x200B;切换节点上每个单独连接器的名称显示。\
*— 显示节点徽章：*&#x200B;在所有节点上切换节点徽章。\
*— 显示节点大小：*&#x200B;切换节点分辨率显示（仅[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)）。\
*— 显示计时：*&#x200B;切换每个节点的毫秒计时的显示（仅[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)）。\
*— 缩小时限制文本缩放：*&#x200B;使[图形项](../../interface/the-graph-view/graph-items/graph-items.md)的文本保持固定的屏幕大小，超过缩放阈值，这样在缩小时文本仍清晰可见。

![](the-graph-view.resources/the-graph-view-12.png)<b>节点查找器</b> (Ctrl+F)\
启用工具以在图形中查找节点、公开的参数和其他变量。 在[专用页面](../../interface/the-graph-view/node-finder/node-finder.md)中了解更多信息。

![](the-graph-view.resources/the-graph-view-13.png) <b>高光流\
</b>突出显示当前所选节点之前或之后连接的所有节点。 适用于跟踪节点的复杂路径。

![](the-graph-view.resources/the-graph-view-14.png) <b>节点调板\
</b>显示或隐藏节点工具栏，请参阅下文。

![](the-graph-view.resources/the-graph-view-15.png) <b>矩形链接\
</b>在节点之间的圆角或矩形链接之间切换。 不适用于[FX-Maps。](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)

![](the-graph-view.resources/the-graph-view-16.png) <b>节点对齐工具\
</b>启用工具在图表中排列选定节点。 在[专用页面](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md)中了解更多信息。

仅在[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)上：

![](the-graph-view.resources/the-graph-view-17.png) <b>主页大小\
</b>切换显示父分辨率控制设置，请参阅下文。

![](the-graph-view.resources/the-graph-view-18.png) <b>链接创建模式</b> (1， 2， 3)\
在“标准”(1)、“材料”(2)和“紧凑材料”(3)链接创建模式之间进行选择，以单独或批量链接节点连接器。 在[专用页面](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)中了解更多信息。

![](the-graph-view.resources/the-graph-view-19.png) <b>计时控件\
</b>允许您重置所有节点和重置所有计时。

![](the-graph-view.resources/the-graph-view-20.png) <b>工具\
</b>*— 清理：*&#x200B;删除属于未连接到[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点的流的所有节点。\
*— 导出输出：*&#x200B;打开[位图导出接口](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)。\
*— 重新导出输出：*&#x200B;再次执行上一个导出操作。\
*-PSD 导出器：*&#x200B;打开[PSD 导出器](../../compositing-graphs/exporting-psd-files/exporting-psd-files.md)接口。

![](the-graph-view.resources/the-graph-view-21.png) <b>节点映像缓存\
</b>切换节点图像缓存切换的显示，请参阅下文。

![](the-graph-view.resources/the-graph-view-22.jpg)删除未使用的节点\
</b>显示用于删除图形中未使用的节点的选项，请参阅下文。

### 节点调板

节点工具栏因图形类型而异：

[![节点调板](the-graph-view.resources/the-graph-view-23.png)](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)<br>
<b>[图形](../../compositing-graphs/substance-compositing-graphs.md)：</b>查看[原子节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)和[图形项](../../interface/the-graph-view/graph-items/graph-items.md)。


![图形项调色板](the-graph-view.resources/the-graph-view-24.png "图形项调色板")<br>
<b>[函数图形](../../function-graphs/function-graphs.md)Substance：</b>请参阅[图形项](../../interface/the-graph-view/graph-items/graph-items.md)。


![FX-Map调色板](the-graph-view.resources/the-graph-view-25.png "FX-Map调色板")<br>
<b>[图形](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)：</b>查看[图形项。](../../interface/the-graph-view/graph-items/graph-items.md)

### 主页大小

![主页大小工具栏](the-graph-view.resources/the-graph-view-26.png "主页大小工具栏")

此工具栏仅在[图形](../../compositing-graphs/substance-compositing-graphs.md)中可用，并设置了图形&#x200B;*父级*&#x200B;的[输出大小](../../compositing-graphs/output-size/output-size.md)，如果它使用&#x200B;*相对于父代* [继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，则会影响图形的输出大小。

默认情况下，水平和垂直大小是链接的，但对于非正方形纹理，大小可以&#x200B;*未链接*。 也可以将值重置为默认值256 x 256。

### 节点映像缓存

![节点映像缓存设置](the-graph-view.resources/the-graph-view-27.png "节点映像缓存设置")

这样可在计算[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)中的节点时切换缓存的使用。

计算某个节点时，其输出图像存储在内存（即缓存）中，因此如果该节点不受更改的影响，则重新计算图表时可以&#x200B;*重新使用它们*。 这意味着只重新计算图表中实际发生更改的部分。

此缓存的内存存储限制可在[首选项](../../interface/preferences-window/preferences-window.md)的<b>常规</b>部分的<b>内存</b>部分下更改。

启用此选项将导致图形计算的整体响应性大幅提升，但代价是显着增加Designer的内存使用量。

### 移除未使用的节点

![删除未使用的节点下拉菜单](the-graph-view.resources/the-graph-view-28.jpg "删除未使用的节点下拉菜单")

在图形中进行迭代并尝试操作时，某些对最终结果没有影响的节点可能会落在后面。 这增加了杂乱和浪费计算，因为所有节点在图形绘制的第一阶段都被评估。

![](the-graph-view.resources/the-graph-view-22.jpg)移除未使用的节点</b>工具将删除&#x200B;*在输出*&#x200B;节点中结束的流中&#x200B;*不是*&#x200B;的所有节点。 唯一的例外是&#x200B;*输入*&#x200B;节点，因为删除这些节点将更改引用此图形的[实例节点](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)的接口。

![移除未使用的节点](the-graph-view.resources/the-graph-view-29.gif "移除未使用的节点")

第一个选项仅将清理应用于&#x200B;*当前*&#x200B;图形。

如果当前图形是[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)，则会启用第二个选项，使您可以在清理过程中&#x200B;*包括所有节点参数函数*。 这意味着，如果控制节点参数值的[函数图形](../../function-graphs/function-graphs.md)具有未使用的节点，则还将按照相同的规则清除该图形。

完成清理后，将显示报告对话框。 您将在<b>控制台</b>中找到更多详细信息，如标记为`GraphCleaner`的日志。 这些日志将包括每个图形和参数函数中已删除的节点数。

可作为&#x200B;*单个*&#x200B;操作在所有受影响的图形上撤消清理。
