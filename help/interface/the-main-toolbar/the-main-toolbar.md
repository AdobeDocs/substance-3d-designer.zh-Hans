---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer中的主工具栏，以访问工作流程的常用工具和命令。
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 主工具栏
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# 主工具栏

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

此页面描述了[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)的主工具栏和菜单，它们出现在主窗口的左上方。它由两部分组成：下拉式主菜单和快速访问按钮。 也可以通过<b>文件</b>和<b>编辑</b>菜单访问所有快速访问按钮功能。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![主工具栏](../../assets/mainmenu.png "主工具栏")

</td>
</tr>
</table>

## 快速访问按钮

![](../../assets/newsubstance.png) <b>新Substance图形……：</b> (Ctrl+N)为您显示[新图形](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)窗口，然后使用[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)创建新包。

![](../../assets/open.png) <b>打开……：</b> (Ctrl+O)打开现有的[Substance包(.SBS、.SBSAR、.SBSASM)](../../getting-started/overview/overview.md)。

![](../../assets/saveall.png) <b>保存全部：</b> (Ctrl+⇧+S)保存[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中列出的所有包。

![](../../assets/undo.png) <b>撤消：</b> (Ctrl+Z)撤消上一个操作。

![](../../assets/redo.png) <b>重做：</b> (Ctrl+Y)重做上一个撤消的操作。

## 文件

<b>新建：</b>打开子菜单以创建图表或包：

* <b>新Substance图形……：</b>(Ctrl+N)为您显示[新图形](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)窗口，此窗口允许您设置新的[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)；
* <b>新建Substance函数图表：</b>使用[Substance函数图表](../../function-graphs/function-graphs.md)创建新包；
* <b>空：</b>创建空包。

<b>打开……：</b> (Ctrl+O)打开现有的[Substance包(.SBS、.SBSAR、.SBSASM)](../../getting-started/overview/overview.md)。

<b>最近打开的包：</b>显示最近打开的包的列表。 单击条目将其打开。

<b>打开上一个会话包(#)</b>：打开上一个会话关闭或结束时打开的所有包。

<b>全部保存：</b> (Ctrl+⇧+S)保存所有打开的包，包括在后台加载的包。

<b>全部关闭：</b>关闭所有打开的包。

<b>重新加载资源：</b>强制Designer重新加载[所有资源，包括位图和SVG数据](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)。

<b>退出：</b> (Ctrl+Q) — 关闭Substance 3D Designer。

## 编辑

<b>撤消：</b> (Ctrl+Z)撤消上一个操作。

<b>重做：</b> (Ctrl+Y)重做上一个撤消的操作。

<b>首选项……：</b>打开“首选项”窗口。

>[!NOTE]
>
> 此对话框可从macOS任务栏上的Substance 3D Designer菜单访问。

## 工具

<b>取消渲染：</b> (Esc)停止Substance 引擎的当前操作。 可用于中止不需要的繁重操作。

<b>挂起引擎：</b> (⇧+Esc)挂起渲染引擎。 这可以加快编辑复杂的[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)。

<b>切换引擎……： </b>(F9)提供多种渲染引擎选择，包括GPU引擎（Windows上为“DirectX”，macOS上为“OpenGL”）和CPU引擎（Apple Silicon上为“NEON”，所有其他上为“SSE”）。

<b>Substance Player：</b>管理Designer与Substance Player的集成：

* <b>查找播放器……：</b>让Designer知道Player的安装位置；
* <b>下载播放器……：</b>打开Substance Player文档的[登陆页面](https://helpx.adobe.com/substance-3d-player/home.html)，在其中可以下载播放器。

<b>增效工具管理器……</b>：打开“增效工具管理器”窗口，您可以在其中安装、加载和卸载[适用于Substance 3D Designer的Python增效工具。](../../scripting/scripting.md)

## Windows

<b>新建资源管理器：</b>打开新的资源管理器停靠。 您可以打开多个Explorer坞站。

<b>新的3D视图：</b>打开新的3D视图停靠区。 您可以打开多个3D视图停放区。

<b>新建库视图：</b>打开新的库停靠。 您可以打开多个库停放区。

<b>Python编辑器：</b>打开用于[评估和创建脚本](../../scripting/scripting.md)的Python编辑器。

<b>重置布局：</b>将工作区重置为默认布局。 所有窗口将重新排列，某些窗口可能会再次隐藏。 在程序布局有问题时使用。

<b>取消最大化窗口：</b>当任何面板为&#x200B;*最大化*&#x200B;时，此选项会取消最大化窗口并恢复布局，就像&#x200B;*在*&#x200B;窗口最大化之前一样

<b>资源管理器：</b>显示/隐藏[资源管理器](../the-explorer-window/the-explorer-window.md)。

<b>图形：</b>显示/隐藏[图形窗口](../../interface/the-graph-view/the-graph-view.md)。

<b>参数：</b>显示/隐藏[属性](../properties/properties.md)。

<b>控制台：</b>显示/隐藏控制台窗口。

<b>3D视图：</b>显示/隐藏[3D视图](../../interface/3d-view/3d-view.md)。

<b>依赖关系管理器：</b>显示/隐藏[依赖关系管理器](../../interface/dependency-manager/dependency-manager.md)。

<b>2D视图：</b>显示/隐藏[2D 视图](../2d-view/2d-view.md)。

<b>库：</b>显示/隐藏[库窗口。](../../interface/the-library/the-library.md)

<b>主工具栏：</b>显示/隐藏主工具栏（仅限快速访问按钮）。

>[!NOTE]
>
> 要了解有关Designer的面板管理、其自定义功能和工作流程增强功能的更多信息，请转至本文档的[自定义您的工作区](../../interface/customizing-your-wor/customizing-your-workspace.md)页面。

## 帮助

<b>Tutorials：</b>打开[Substance 3D教程](https://substance3d.adobe.com/tutorials/)网站（以前是Substance学院）。<b>\
</b>

<b>发行说明：</b>打开包含最新版本更改日志的窗口。

<b>技术要求：</b>为您显示运行应用程序的技术要求。

<b>文档：</b>在[此文档](https://www.adobe.com/go/Substance-3D-doc-Designer_cn)上打开您的默认Web浏览器。

<b>脚本文档：</b>在本地Python API文档中打开Web浏览器。

<b>论坛……：</b>在我们的[支持社区](https://forum.substance3d.com/)论坛上打开Web浏览器，与社区联系并提问。

<b>报告错误……：</b>打开错误报告窗口。

<b>导出日志……：</b>将当前日志文件导出为压缩(.zip)文件，以便提供技术支持。

<b>提供反馈……：</b>在Adobe的[支持社区](https://www.adobe.com/go/Substance-3D-feedback-Designer_cn)主页上打开Web浏览器。

<b>Substance 3D资源：</b>浏览订阅者的[收费3D内容](https://substance3d.adobe.com/assets)（以前是Substance Source）。

<b>Substance 3D社区资源：</b>允许您浏览[免费社区资源](https://substance3d.adobe.com/community-assets/)（以前是Substance share）。

<b>管理我的帐户\*：</b>打开Adobe帐户的网页。

<b>登录/注销……\*：</b>允许您登录/注销Adobe帐户。

<b>主屏幕……：</b>显示[主屏幕](../../interface/home-screen/home-screen.md)对话框。

<b>新增功能……：</b>显示一个屏幕，其中突出显示了Designer最新版本中新增的功能

<b>欢迎屏幕……\*：</b>显示一个屏幕，引导新用户了解Designer的用途及其在[Substance 3D生态系统](https://helpx.adobe.com/substance-3d.html)中的位置

<b>合作伙伴：</b>允许您访问Designer中我们的合作伙伴针对第三方集成的免责声明和声明。

<b>关于Substance 3D Designer...：</b>显示有关应用程序及其组件的信息，例如版本号。

\*：这些选项仅在通过[Adobe Creative Cloud桌面版](https://creativecloud.adobe.com/en/apps/download/creative-cloud)安装的Designer版本中可用，该版本需要[Substance 3D订阅](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar)。
