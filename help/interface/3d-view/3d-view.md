---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/3d-view.html"
breadcrumb-title: ""
description: 使用Substance 3D Designer中的3D视图预览3D对象上的材料并测试光照条件。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 视图
user-guide-description: ""
user-guide-title: ""
source-git-commit: c3acf6cdb931126827d2a35dec1135800788ed81
workflow-type: tm+mt
source-wordcount: '3549'
ht-degree: 1%
---

# 3D 视图

该3D 视图可帮助您通过自定义网格和渲染的PBR材料来查看和了解材料。<br>与所有Substance 3D Designer Windows一样，它通过右键单击菜单选项和拖放操作与其他窗口协同工作。

3D视图还提供了两种在3D场景中渲染材料的主要方法：
* 使用&#x200B;**光栅器**&#x200B;和&#x200B;**OpenGL**&#x200B;渲染器快速实时可视化
* 具有&#x200B;**GPU 路径追踪**&#x200B;渲染器的高质量光线追踪渲染

在此处了解详情： [3D渲染器](3d-renderers/3d-renderers.md)

+++ 3D视图停放

![3d-view.png](3d-view.resources/3d-view.png)

+++

## 视口交互

下面一节将简要介绍如何执行常见操作，同时附上动画GIF以说明这一过程。

![视口导航](3d-view.resources/3d-navigate.gif "视口导航")

### 导航

相机和环境的处理方式有三种：

* <b>轨道：</b> LMB +拖动
* <b>平移</b>： MMB+拖动/ Ctrl+RMB+拖动
* <b>缩放</b>：使用MouseWheel滚动/人民币并拖动
* <b>旋转环境：</b> ⇧+人民币+拖动
* <b>聚焦所选网格：</b> F（如果没有选择，则聚焦整个场景）
* <b>轨道点光1：</b> Ctrl+⇧+LMB+拖动
* <b>将点光1移近/远离原点：</b> Ctrl+⇧+RMB+拖动
* <b>重置相机轨道位置：</b> R
* <b>重置相机轨道位置和属性：</b> ⇧+R

使用触控板（仅限macOS）

* <b>轨道：</b>双指轻扫
* <b>平移：</b>⇧+双指轻扫
* <b>缩放： </b>双指捏合/⌘+双指轻扫
* <b>旋转环境：</b>⇧+双指轻扫

>[!NOTE]
>
> 缩放方向
> 
> 每种缩放方法都会与另一种方法反转：
> 
> * 鼠标滚轮&#x200B;*拉近*&#x200B;场景的距离
> * 以人民币计价，然后向上拖动&#x200B;*推移*&#x200B;场景
> 
> 可在[首选项](../../interface/preferences-window/preferences-window.md)中反转缩放方向。

### 选择并聚焦

您可以直接在视口中与网格交互：

<b>按住⇧并单击网格上的LMB以选择网格。</b> 所选网格具有蓝色轮廓。

<b>按F键可专注于所选网格</b>。 聚焦网格可以移动相机以帧它并围绕它运行。

<b>在选择网格时单击RMB</b>以在上下文菜单中访问其[材料操作](#material-actions)。

<b>按Esc键取消选择。</b> 光标不需要位于网格上。

![3D 视图 — 聚焦并取消选择](3d-view.resources/sceneBrowser-focus.gif "3D 视图 — 聚焦并取消选择"){zoomable="yes"}

*选择、聚焦、取消选择*

![3D 视图 — 上下文菜单](3d-view.resources/sceneBrowser-contextualMenu.gif "3D 视图 — 上下文菜单"){zoomable="yes"}

*选择，上下文菜单*

>[!NOTE]
>
> 这些操作不适用于已弃用的[OpenGL](../../interface/3d-view/3d-renderers/3d-renderers.md)渲染器。

### 更改环境光照(IBL)

默认情况下，Designer使用基于图像的光照(IBL)。 高动态范围位图用于渲染环境光照。

您可以围绕3D对象旋转此环境，也可以加载预设或自定义HDR光照环境。 请注意，HDR图像应使用等距矩形投影，并且精度为32位浮点。

⇧+人民币+拖动<b>在3D视图中旋转环境</b>。

要设置精确的旋转，请使用顶部3D 视图工具栏中的<b>环境>编辑</b>，并在属性窗口中更改<b>旋转角度</b>滑块。

要使用预设的HDR光照环境，请单击[库](../../interface/the-library/the-library.md)中<b>3D 视图类别</b>的<b> HDRI环境</b>部分，然后将任意图标拖放到3D视图中。

要使用您自己的自定义HDR光照环境，请导入一个HDR图像，方法是：将文件拖放到资源管理器窗口中的一个包中（出现提示时，将该文件<b>链接</b>）。 然后拖放该资源，选择<b>Latitude/Longtitude全景图</b>作为目标。

### 点光

转到<b>光照>编辑属性</b>以切换场景中的点光。

在“光照”模式下按住LMB或RMB并在场景中拖动，可在视口原点周围移动点光1。 <img src="3d-view.resources/image2020-9-17-10-30-37.png" width="24" />

处于相机模式时 <img src="3d-view.resources/image2020-9-17-10-31-32.png" width="24" /> ，也可以通过按住Ctrl+⇧键并结合使用鼠标按钮来临时切换到光照模式。

## 在3D 视图中查看数据

![查看图形输出](3d-view.resources/3d-material.gif "查看Substance图形输出")

### Substance 图形

您可以将整个材料作为完整材料在3D 视图中查看。 这是最常用的工作方式，并且会将[输出节点上的使用属性](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)与3D材料的相关节点槽进行匹配。 这意味着需要正确设置您的输出（使用“模板”可确保这一点），并且您选择的材料/视口着色器支持

要查看图形的所有输出，请单击[图形视图](../../interface/the-graph-view/the-graph-view.md)中的空白区域&#x200B;*人民币*，然后在上下文菜单中选择&#x200B;**在3D 视图中查看输出**&#x200B;选项。

无需打开图形的输出，也可以通过在[资源管理器](../the-explorer-window/the-explorer-window.md)停靠区中的图形资源上单击RMB，然后在上下文菜单中选择&#x200B;**在3D 视图中查看输出**&#x200B;选项来查看输出。

作为图形上下文菜单的替代方法，可以通过将图形从[资源管理器](../the-explorer-window/the-explorer-window.md)停靠区拖动到3D 视图来获得相同结果。

在&#x200B;*加载图形*&#x200B;时，默认情况下，其输出将自动应用于3D 视图。 您可以在[首选项](../../interface/preferences-window/preferences-window.md)中禁用此行为。 转到&#x200B;**编辑>首选项>图形>常用**，并取消选中&#x200B;**打开图形时在3D视图中查看输出**&#x200B;选项。

>[!NOTE]
>
> **多个材料插槽**
> 
> 如果您将自定义网格用于多个单个材料，系统将要求您选择要将材料分配给哪个材料插槽。 使用上述任一方法，单击插槽以确认您的选择。 有关材料及其分配的更多信息，请阅读下面的详细部分。

![查看3D 视图与图形输出](3d-view.resources/3d-channel.gif "查看3D 视图与图形输出")

### 单个节点/图形输出

在[3D 视图](https://substance3d.adobe.com/)中的任何可用材料声道中只能查看单个输出。 此选项卡不太常用，但适用于预览快速测试或无输出的单个节点。

在[节点](../../interface/the-graph-view/the-graph-view.md)中右键单击任何图形视图，然后选择<b>在3D 视图中查看</b>，即可查看任何节点，而不仅仅是输出节点。 您会看到一个列表，其中包含可分配节点的可用通道。 单击“任意”以确认。

您也可以使用&#x200B;*RMB*&#x200B;将任何图形视图从节点拖放到3D 视图中。 您会看到一个列表，其中包含可分配节点的可用通道。 单击“任意”以确认。

您可以通过展开[图形输出](../the-explorer-window/the-explorer-window.md)停靠区中的图形资源并使用&#x200B;*LMB*&#x200B;将该输出拖到3D 视图来查看任何单个资源管理器。 您会看到一个列表，其中包含要分配节点的可用通道。 单击“任意”以确认。

![查看自定义3D网格](3d-view.resources/3d-mesh.gif "查看自定义3D网格")

## 查看（自定义）3D场景

Designer提供十几种预设网格。 这些网格具有统一、可用的UV坐标，并为拼贴纹理提供大多数方案。 也可以导入和查看自己的3D网格。\
通过顶部栏中的<b>网格</b>下拉菜单选取任何默认场景。

对于自定义3D场景，请转至[使用3D场景](../../working-with-3d-scenes/working-with-3d-scenes.md)部分。

![更改材料属性](3d-view.resources/3d-materials.gif "更改材料属性")

## 更改着色器属性

Designer中默认提供了几种不同的[着色器](../../glossary/glossary.md)，并且每个着色器的选项不仅仅是纹理通道。 可以单独配置它们。

请记住，在Designer的[3D渲染器](../../interface/3d-view/3d-renderers/3d-renderers.md)中，着色器是不同的，当切换渲染器时，只有标有“通用”标签的设置才会延续下去。

要更改当前着色器，请转到&#x200B;**材料**&#x200B;菜单，然后打开要编辑的材料的子菜单。

例如，要在“平面（高分辨率）”场景中调整“`Default`”材料的a材料属性，请转到&#x200B;**材料>默认>编辑属性**。 然后在“Properties”（属性）停放中找到“材料”属性

您可以使用子菜单中的“重置材料”或“重置为场景状态”操作来重置着色器。 如果要在3D视图中查看图形输出，则需要重新应用它们。

>[!NOTE]
>
> **关于曲面细分**
> 
> 可以使用[网格弹出窗口](displacement/displacement.md#tessellation)中的&#x200B;**曲面细分因子**&#x200B;参数调整位移的曲面细分。
> 由该参数控制的特定属性随当前3D渲染器而变化：
> 
> * **光栅器/GPU 路径追踪：**&#x200B;名为&#x200B;**细化级别**&#x200B;的每个对象属性。 在[场景浏览器](scene-browser/scene-browser.md)中选择`Mesh`对象以显示其属性并直接编辑。
> * **OpenGL：**&#x200B;每个材料的属性名为&#x200B;**曲面细分因子**。 转到[材料属性](#change-shader-properties)以直接对其进行编辑。

![导出场景](3d-view.resources/3d-view-export-scene.gif "导出场景")

## 导出场景

了解如何在[此页面](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)中导出3D场景。

### 导出镶嵌网格（仅限OpenGL渲染器）

您可以将<b>3D 视图</b>中的网格导出为<b>OBJ</b>、<b>FBX</b>或<b>PLY</b>格式的文件。 如果&#x200B;*曲面细分*&#x200B;位移已启用，则几何的细分烘焙到导出的网格中。

但是，原始网格的顶点法线可能与其新的位移形状不匹配，这意味着位移网格可能无法正确渲染。 您可以通过两种方式管理这种情况：

* 使用将提供正确法向的网格&#x200B;*法线图*
* 使用网格法线图导出时&#x200B;*重新计算网格法线*，这意味着这些法线将烘焙到导出的网格中，不再需要法线图

要导出网格，请转到<b>场景>导出镶嵌网格...</b>，设置有关法线重新计算的选择，然后为导出的网格选择位置、名称和文件格式。

>[!NOTE]
>
> 此功能在&#x200B;**macOS**&#x200B;上&#x200B;*不可用*。

>[!IMPORTANT]
>
> 一些注意事项
> 
> 如果原始网格有多个材料和/或UV 集，则这些将&#x200B;*合并为一个*。
> 
> 导出过程的持续时间及生成的文件大小取决于网格三角形计数和&#x200B;*曲面细分因数*。 较高的曲面细分因数值可能导致不稳定，具体取决于GPU的板载内存池。
> 
> 尽管如此，镶嵌网格的顶点计数应与&#x200B;*Height*&#x200B;映射的像素计数在&#x200B;*相同的范围*&#x200B;内。
> 
> 使用<b>通</b>曲面细分时，网格比高度图密集可以使网格略为平滑，但您应该着眼于先可靠地导出包含所需高度图详细信息的网格，然后根据需要在其他软件中优化导出的网格。

>[!WARNING]
>
> **TDR（仅限Windows）**
> 
> 此功能要求<b>超时检测和恢复(TDR)</b>与我们的文档的[本页](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)中的建议值匹配，如Designer的[技术要求](../../getting-started/system-requirements/system-requirements.md)中所述。

## 菜单栏

菜单栏提供了7个菜单，其中包含与3D 视图相关的选项。 下面是所有可用选项的概述。

+++场景
<b>场景</b>菜单用于处理显示的几何（3D资源）和3D视图状态。 3D资源仅共享网格，场景状态包括光源、相机和相关设置，并且还可将该网格与之一起包含。

![场景的菜单网格](3d-view.resources/3d-view-meshes.png "场景的菜单网格")



<b>编辑： </b>在[属性](../../interface/properties/properties.md)面板中加载场景选项。 用于切换3D 网格的可见性。

<b>标准基元：</b>显示3D 视图中以下任何简单3D网格。

* 立方体

* 圆柱体

* 空心框

* 内框

* 平面

* 平面 (hi-res)

* 球体

<b>扩展基元：</b>显示3D 视图中的以下任何3D网格。

* 布料

* 材质球

* 圆角立方体

* 圆角圆柱体

* 球体 2 平铺

* 圆环体

<b>在2D 视图中显示UV：</b>允许将当前所选网格的UV显示为[2D 视图](../2d-view/2d-view.md)中的叠加。

<b>从当前场景创建3D资源……：</b>在当前场景之外的包中创建新的[3D 场景资源](../../resources/3d-scene-resource/3d-scene-resource.md)。

<b>加载状态文件……： </b>加载外部保存的[场景状态文件](../../working-with-3d-scenes/working-with-3d-scenes.md) (\*.sbsscn)。 不替换3D 网格，仅加载3D渲染器、相机和光源的设置。

<b>加载带有网格的状态文件……：</b>加载外部保存的[场景状态文件](../../working-with-3d-scenes/working-with-3d-scenes.md) (\*.sbsscn)。 载入3D渲染器、相机、光源的设置及其参照3D 场景。 .

<b>保存状态文件……： </b>将3D视图的当前状态保存到[场景状态文件](../../working-with-3d-scenes/working-with-3d-scenes.md) (\*.sbsscn)。

<b>将当前状态保存为默认值： </b>将3D视图的当前状态设置为[场景状态文件](../../working-with-3d-scenes/working-with-3d-scenes.md)，以便在创建新的3D视图时默认使用。 每次重置或初始化3D视图时都会加载此文件，并且可以在[项目设置](../../interface/preferences-window/project-settings/project-settings.md)中进行设置。

<b>导出场景：</b> *（仅限栅格化程序/GPU 路径追踪渲染器）*&#x200B;将当前场景导出为[拼合场景](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)，只写入结果场景，并且丢失对原始场景的任何引用。 导出格式的内容取决于所选导出场景支持的功能。\
可用格式：STL、FBX、GLB、GLTF、PLY、USDC、USD、USDA、USDZ、OBJ。

<b>导出带图层的场景：</b> *（仅栅格化程序/GPU 路径追踪渲染器）*将当前场景导出为[分层场景](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)，其中对原始场景的所有编辑将以非破坏性的工作流程存储到单独的文件中。 这仅适用于USD文件格式。\
可用格式包括：USDC、USD、USDA。

<b>导出镶嵌几何：</b> *（仅限OpenGL渲染器）*&#x200B;将带有曲面细分的当前场景导出为原始几何形状，请参阅导出场景部分。

<b>重置场景： </b>将3D视图重置为默认值。

某些软件更新可能会更改场景状态文件的保存/加载方式。

如果场景&#x200B;*未从文件中正确还原*，建议手动设置场景的所需状态，并&#x200B;*重新导出*&#x200B;场景状态文件。

+++

+++材质
<b>材料</b>菜单会根据加载的3D 网格和使用的渲染器而发生变化。

“材料”菜单包含分配给场景中网格的所有材料的列表。 “材料”菜单中列出的每个材料都有一个材料操作的子菜单：

<b>编辑</b> — 在“材料”窗口中编辑当前属性的设置。

<b>着色器列表</b> — 当前[3D渲染器](../../interface/3d-view/3d-renderers/3d-renderers.md)可用的所有[着色器](../../glossary/glossary.md)。

<b>加载定义……： </b>（仅限OpenGL渲染器）允许您加载自己的自定义[着色器。](../../interface/3d-view/glslfx-shaders/glslfx-shaders.md) 该着色器即被添加到上述列表中。

<b>重置公共参数：</b>重置所有着色器上公共的参数。 例如，在栅格化器/GPU 路径追踪和OpenGL渲染器之间切换时，[Adobe Standard Material](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/general-knowledge/asm/adobe-standard-material)中的几个参数值将传递过去。

<b>重命名：</b>更改此材料的标签。

<b>重置材料：</b>将所有着色器参数重置为默认值。 如果纹理已连接到着色器的任意一个取样器，则这些取样器会断开连接。

<b>将材料重置为场景状态： </b>*（仅限栅格化程序/GPU 路径追踪渲染器）*&#x200B;将[已覆盖材料](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)的所有属性重置为场景中的原始值，包括原始纹理（如果有）。

<b>添加： </b>将新材料添加到列表。 默认情况下，未使用它，并且可能已[&#128279;](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)使用[材料](../../interface/3d-view/scene-browser/scene-browser.md)连接到一个场景浏览器。

+++

+++光源
<b>光照</b>菜单仅处理较旧的旧环境光和点光。 这些光照不符合PBR标准，并且无法提供与基于HDR图像的渲染相同的高品质结果。

<b>编辑：</b>编辑环境光和两点光的个别设置。

<b>重置光源：</b>将光源属性重置为默认状态。

+++

+++相机
使用<b>相机</b>菜单，可以更改相机设置、转到预定义角度并加载存储在自定义相机文件中的3D 网格角度。

<b>编辑属性：</b>在“属性”停靠区中打开默认相机的设置。

<b>焦点： </b>(F)将默认相机聚焦到当前所选网格。 即，网格并将相机透视与其对齐。 如果没有现用选区，则使用场景的全局定界框。

<b>相机：</b>如果场景包含一个或多个相机，则它们在此处列出，它们的设置用作预设，可应用于场景的默认相机。

<b>视点：</b>默认相机的预配置视点。 这些仅影响相机的变换（位置和旋转）。

* 默认：从对象的前左拍摄高角度照片。

* 返回

* 底部

* 前

* 左

* 右

* 顶部

<b>保存渲染……：</b> (Alt+S)将当前渲染的图像以渲染器属性中指定的分辨率或默认相机属性（如果已设置覆盖分辨率）保存到磁盘。

<b>将渲染复制到剪贴板：</b> (Alt+C)将当前渲染的图像复制到剪贴板，以便在外部图像编辑器中粘贴。

<b>重置位置：</b> (R)重置相机的位置。

<b>重置选定项：</b> (Shift+R)重置相机的位置和属性。

+++

+++环境
使用<b>环境</b>菜单可修改用于照明PBR正确材料的HDRI环境相关设置。

<b>编辑属性：</b>允许访问HDR环境设置，用于在PBR中进行光照。 具体来说，您可以使用预览切换可见性、更改曝光度并使用精确滑块设置旋转。

<b>重置环境：</b>将所有环境属性重置为默认值。

+++

+++显示
使用显示菜单，您可以切换所渲染场景的视图模式、助手和信息：

<b>轴：</b>切换视口中3D轴的显示。

<b>网格：</b>切换显示World Frid。

<b>分辨率：</b>切换小分辨率计数器的显示。

<b>场景统计信息：</b>切换场景统计信息的显示，例如多面计数、材料计数、静态网格计数等。

<b>渲染时间：</b>为完整图像计算一个示例的时间。

<b>样本：</b>为累积消除锯齿（栅格化器）或路径跟踪（GPU路径跟踪器）计算的像素样本量。

<b>背面消隐：</b>禁用此选项后，您可以从&#x200B;*两侧*&#x200B;看到网格脸部。 该选项可与线框结合使用

<b>定界框：</b>可切换网格定界框的显示。

<b>线框：</b>切换网格线框的显示。

<b>光源：</b>切换点光源的助手线显示。

<b>正切空间：</b>将所有顶点的正切、次法线和法线矢量显示为彩色小工具

其中一些选项在场景工具栏中的按钮切换中可用。

+++

+++渲染器
使用<b>渲染器</b>菜单，您可以切换3D渲染器，并通过<b>编辑属性</b>操作访问当前3D渲染器的属性。

可用的渲染器及其设置记录在[此专用页面](../../interface/3d-view/3d-renderers/3d-renderers.md)中。

+++

## 场景工具栏

默认情况下，**场景**&#x200B;工具栏位于3D 视图的左边框，提供用于查看文档以及与场景交互的控件。

还允许您访问[位移弹出窗口](displacement/displacement.md)和[场景浏览器](scene-browser/scene-browser.md)程序坞。

>[!NOTE]
>
> 可以使用以三条平行线表示的最左侧&#x200B;*手柄*，围绕&#x200B;**3D 视图**&#x200B;停放区&#x200B;*重新定位*。




### 显示选项

#### 顶部

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-scene-browser.png" width="24" /> <b>场景浏览器</b>

显示3D 场景中所有元素的层次结构。

>[!INFO]
>
>[专用页面](../../interface/3d-view/scene-browser/scene-browser.md)广泛介绍了场景浏览器及其功能。


<img src="3d-view.resources/3d-view-scene-toolbar-select.png" width="24" /> <b>选择</b>

允许直接选择场景中的网格。

<code>LMB</code> 在场景中选择一个网格。

选择场景中的各个网格。 所选网格在视口中有蓝色轮廓，并在[场景浏览器](../../interface/3d-view/scene-browser/scene-browser.md)中突出显示。

上下文菜单可用于选定的网格，可通过单击<code>人民币来显示</code>.

也可以通过按<code>Shift+LMB在“相机”或“浅色”模式中选择网格</code>.

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-camera.png" width="22" /> <b>相机</b>

允许直接控制场景中的相机。

<code>LMB</code> 绕着相机运行目标。<br><code>人民币</code> 将相机移近或移远目标。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-environment.png" width="24" /> <b>显示环境</b>

此按钮可切换场景环境的显示。 在转到3D 视图菜单栏中的<b>“环境”>“编辑”</b>后，可在“属性”停靠区中找到相同的设置。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-light.png" width="24" /> <b>亮度</b>

允许直接控制场景中的点光1。

<code>LMB</code> 围绕场景的原点运行相机。<br><code>RMB</code> 将光源移近或移远场景的原点。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="24" /> <b>渲染器设置</b>

在[属性](../properties/properties.md)停靠区中显示当前渲染器的设置。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-pathtracer.png" width="24" /> <b>启用路径跟踪器</b>

切换[GPU 路径追踪](3d-renderers/3d-renderers.md#gpu-pathtracer)渲染器的选择。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-shadows.png" width="24" /> <b>启用阴影</b>

在[光栅器](3d-renderers/3d-renderers.md#rasterizer)渲染器中切换实时阴影的渲染。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-ground-plane.png" width="24" /> <b>启用地面平面</b>

在[GPU 路径追踪器](3d-renderers/3d-renderers.md#rasterizer)和[光栅器](3d-renderers/3d-renderers.md#gpu-pathtracer)渲染器中切换地面平面的渲染。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-displacement.png" width="24" /> <b>位移</b>

显示[位移弹出窗口](displacement/displacement.md)。

<br>

#### 底部

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-grid.png" width="24" /> <b>网格</b>

切换世界网格的显示。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-stats.png" width="24" /> <b>场景统计信息</b>

切换场景统计信息的显示，如多面计数、材料计数、静态网格计数等。

<br>

<img src="3d-view.resources/3d-view-scene-toolbar-pivot.png" width="24" /> <b>轴</b>

切换视口中3D轴的显示。

<br>

#### 仅限OpenGL渲染器

<br>

![](3d-view.resources/3d-view-display-backface-culling.jpg) <b>背面消隐</b>

禁用此选项后，您可以从&#x200B;*两侧*&#x200B;看到脸部。 该选项可与线框结合使用。

<br>

![](3d-view.resources/3d-view-display-bounding-box.jpg) <b>定界框</b>

切换网格定界框的显示。

<br>

![](3d-view.resources/3d-view-display-vertex-tangent-space.jpg) <b>顶点的正切空间</b>

以彩色小工具显示所有顶点的正切、次法线和法线矢量。

<br>

![](3d-view.resources/3d-view-display-wireframe.jpg) <b>线框</b>

将网格显示切换为线框。

## 显示工具栏

默认情况下，<b>显示</b>工具栏位于<b>3D 视图</b>面板的&#x200B;*底部*，它允许您控制渲染的图像在视口中的显示方式。

>[!NOTE]
>
> 可以使用以三条平行线表示的最左侧&#x200B;*手柄*，围绕&#x200B;**3D 视图**&#x200B;停放区&#x200B;*重新定位*。

### 3D 渲染 AOV

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0; vertical-align: top">
        <td style="border: 0">
            <p>您可以使用<img src="./3d-view.resources/aov/aov-icon.png" alt="3D渲染AOVs图标" style="padding-left: 5px; padding-right: 5px" /> <b>3D渲染AOV</b>按钮显示不同的<a href="../../glossary/glossary.md#aov">AOV</a>。</p>
            <p>使用AOV，可以单独检查网格和材料信息，以便进行重点工作和调试。</p>
            <p>某些AOV包括在视口中固定为1（纯白）或0（纯黑）的<i>HDR 值</i>。<br>要检查整个范围的值，可以将AOV的3D渲染导出为支持HDR 值的图像文件格式，如<code>.exr</code>。<br>使用“<code>Camera > Save render...</code>”菜单选项导出当前AOV。</p>
            <p><i>注意：</i>只有在使用栅格化器和GPU 路径追踪<a href="./3d-renderers/3d-renderers.md">3D渲染器</a>时，AOV才可用。</p>
        </td>
        <td style="width: 33%; border: 0">
            <img src="3d-view.resources/aov/aov-composited.jpg" alt="合成的3D渲染AOV" />
        </td>
    </tr>
</table>

### 颜色通道

您可以使用![](3d-view.resources/2d-view-icon-channels.png) <b>单通道通道</b>按钮显示图像的颜色。 这将打开一个组合框，允许您选择应显示<b>红色</b>、<b>绿色</b>和<b>蓝色</b>通道中的哪一个。 通过选择<b>RGB</b>选项，可以恢复包含所有通道的图像的正常外观。

<b>颜色通道</b>按钮&#x200B;*的*&#x200B;图标&#x200B;*会根据当前显示通道而更改*。

### 色彩空间

为了最准确地呈现颜色，默认情况下，图像以&#x200B;*色彩空间*&#x200B;显示，与&#x200B;*监视器*&#x200B;使用的色彩空间相匹配。

可用控件将取决于[项目设置](../../interface/preferences-window/project-settings/project-settings.md)中设置的色彩管理模式。 在本页的[色彩管理](../../color-management/color-management.md)部分中了解有关这些控件的更多信息。
