---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: 解决Substance 3D Designer中的3D视图问题，包括渲染、显示和性能问题。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D查看问题
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1643'
ht-degree: 0%

---


# 3D查看问题

本页列出了与Substance 3D Designer中的[3D视图](../../interface/3d-view/3d-view.md)相关的技术问题，并提供了针对每个问题的故障排除步骤。

## 低性能：未使用独立GPU

**![（错误）](../../assets/error.svg)问题**

Substance 3D Designer不使用系统的&#x200B;*独立* GPU (<b>dGPU</b>)，而使用&#x200B;*集成* GPU (<b>iGPU</b>)。 在渲染图形和/或[3D视图](../../interface/3d-view/3d-view.md)时，这将导致性能降低。

**![（刻度）](../../assets/check.svg)建议的步骤**

具有可切换图形的系统可以&#x200B;*强制使用dGPU*，具体取决于GPU制造商，该GPU应用于专用软件中的&#x200B;*特定应用程序*。

例如，拥有<b>Nvidia dGPU</b>的用户可以执行以下操作：

1. 关闭Substance 3D Designer
2. 打开<b>NVIDIA控制面板</b>
3. 转到<b>3D设置</b>部分中的<b>管理3D设置</b>屏幕
4. 在<b>程序设置</b>选项卡中查找“Substance 3D Designer”条目
5. 在<b>首选GPU</b>组合框中选择<b>高性能NVIDIA处理器</b>
6. 启动Substance 3D Designer

>[!WARNING]
>
> 请注意，集成的GPU (iGPU) *不受支持*。 您可以在[系统要求](../../getting-started/system-requirements/system-requirements.md)页面上了解更多信息。

## 3D对象是扁平的

**![（错误）](../../assets/error.svg)问题**

在一个会话中以详细卷为特征的3D对象在下一个会话中变为平面对象，但是图形没有改变，并且Height映射带有相同的数据。

**![（刻度）](../../assets/check.svg)建议的步骤**

使用一种称为&#x200B;**镶嵌位移**&#x200B;的技术根据Height映射执行3D对象的变形效果。 这项技术包括两个步骤：

1. **镶嵌**：对象几何为&#x200B;*再分割*&#x200B;为顶点，从而产生&#x200B;*更密集的几何形状*&#x200B;以支持更精细的卷细节
2. **位移**：顶点&#x200B;*已移动* — 即已位移 — 沿其&#x200B;*法向矢量*。 法向量沿多边形所面对的方向，并具有模数（即长度）为1的量

位移&#x200B;*方向*&#x200B;是已知的：法向矢量的方向。\
顶点移动所依据的位移&#x200B;*距离*&#x200B;的计算方法如下： `Distance = Height scale * Height map`。 由于Height映射在图形中&#x200B;*未更改*，因此会保留&#x200B;**Height比例**。

默认Height比例值为&#x200B;**1.0**，根据3D视图中所显示的网格以及应用的位移映射，这可能会产生&#x200B;*不明显的* Height效果。

可通过以下方式修改此值：

| 在3D视图中 | 在图形视图中 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 使用左侧工具栏中的&#x200B;**位移弹出窗口**。<br>在[专用页面](../../interface/3d-view/displacement/displacement.md)中了解更多信息。 | 创建[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点并在其属性中设置`heightScale`用法。<br>使用此值为此输出提供一个值，例如，使用[常量浮点节点](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats)，然后&#x200B;*在3D视图中重新应用图形*。 |

>[!TIP]
>
> 使用此方法，您可以设置每个图形&#x200B;*的自定义Height比例值*，这样您就可以调整它以匹配该图形的特定素材。

## 3D视图完全为黑色

**![（错误）](../../assets/error.svg)问题**

在版本15.0.0及更高版本中，3D视图的视区为纯黑色。 我看到一些文本叠加（例如，采样和渲染时间），但3D场景不可见。

**![（刻度）](../../assets/check.svg)建议的步骤**

版本15.1及更高版本

新的3D渲染器已在15.1版中升级，需要最新的GPU驱动程序。 请将系统的GPU驱动程序更新到最新版本。

您可以在此处找到驱动程序： [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [英特尔](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

15.0及更高版本

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md)引入了我们新的内部[3D渲染器](../../interface/3d-view/3d-renderers/3d-renderers.md)，它们使用现代技术，因此不受旧版GPU支持。

根据Designer的[系统要求](../../getting-started/system-requirements/system-requirements.md)，支持的GPU包括NVIDIA RTX 20系列（图例）或更高版本。

通过使用“项目设置”[&#128279;](../../interface/preferences-window/project-settings/project-settings.md)中的new选项，您可以继续默认使用OpenGL渲染器：

1. 转到编辑>首选项>项目
2. 选择列表中的最后一个项目文件
3. 在项目文件列表下，选择3D视图选项卡
4. 将“默认渲染器”选项设置为“OpenGL（已弃用）”
5. 单击“确定”以验证更改

现在，所有新的3D视图在默认情况下都将使用OpenGL渲染器，您可以像以前一样继续工作。

>[!NOTE]
>
> 同样的问题和故障排除步骤适用于大多数AMD和Intel GPU，我们的新3D渲染器当前&#x200B;*不支持*。

>[!IMPORTANT]
>
> OpenGL渲染器&#x200B;*已弃用*，将来可能会从Designer中删除。 我们建议升级系统的GPU，以防止工作流程中断并确保继续获得支持。

## 显示“不支持渲染器”消息

**![（错误）](../../assets/error.svg)问题**

在15.0.0及更高版本中，使用新的3D渲染器（栅格化器、GPU路径跟踪器）时，在视区的右下角会显示“不支持渲染器”消息。 3D场景不可见。

**![（刻度）](../../assets/check.svg)建议的步骤**

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md)引入了我们新的内部[3D渲染器](../../interface/3d-view/3d-renderers/3d-renderers.md)，它们使用现代技术，因此不受旧版GPU支持。

根据Designer的[系统要求](../../getting-started/system-requirements/system-requirements.md)，支持的GPU包括NVIDIA RTX 20系列（图例）或更高版本。

在默认设置下，如果在[项目设置](../../interface/preferences-window/project-settings/project-settings.md)中将“默认渲染器”选项设置为“默认（预定义渲染器）”，则3D视图将自动回退到OpenGL渲染器。

您可以按照以下步骤查找并调整该选项：

1. 转到编辑>首选项>项目
2. 选择列表中的最后一个项目文件
3. 在项目文件列表下，选择3D视图选项卡
4. “默认渲染器”选项列在该选项卡的设置中

>[!NOTE]
>
> 当前只能检测到<b>NVIDIA GTX系列</b>中的GPU不受支持。
> 
> 但是，大多数AMD和Intel GPU也不受支持，将生成黑色渲染且不会显示任何消息。 有关这些GPU的指导，请参阅上面的“3D视图完全是黑色的”项目。

>[!IMPORTANT]
>
> OpenGL渲染器&#x200B;*已弃用*，将来可能会从Designer中删除。 我们建议升级系统的GPU，以防止工作流程中断并确保继续获得支持。

## 3D对象看起来完全平滑

**![（错误）](../../assets/error.svg)问题**

在处理发送到&#x200B;**Height** [输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)的数据后，对象似乎有一些卷，但&#x200B;*看起来完全平滑*，就好像在着色中忽略了Height信息。

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![（刻度）](../../assets/check.svg)建议的步骤**

确保Height数据&#x200B;*转换为法线*，这些法线连接到&#x200B;**法线** [输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)。

使用&#x200B;**镶嵌位移**&#x200B;技术时（请参阅上面的“3D对象是扁平的”），对象可能&#x200B;*变形*&#x200B;以跟随Height数据，但它的表面将&#x200B;*不会对光线做出不同的反应*，直到其&#x200B;*法线*&#x200B;也修改以考虑Height数据。

解决方案非常简单：将流的最后一个指向Height输出的节点连接到[正常](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)节点。 根据您正在处理的材质调整该节点的&#x200B;**强度**&#x200B;参数，并将“正常”节点连接到&#x200B;**正常**&#x200B;输出。

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/3dview-height-without-normals.gif){width="256px"}

</td>
</tr>
</table>

## 渲染模糊/像素化

**![（错误）](../../assets/error.svg)问题**

当系统使用&#x200B;*显示缩放*&#x200B;时，渲染的图像看起来模糊或像素化。

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![（刻度）](../../assets/check.svg)建议的步骤**

默认情况下，Designer使用&#x200B;*缩放*&#x200B;显示分辨率来定义[3D视图](../../interface/3d-view/3d-view.md)的渲染分辨率。 您可以更改此设置，以便使用&#x200B;*本机*&#x200B;显示分辨率来代替清晰的渲染。

打开&#x200B;**编辑**&#x200B;菜单并选择&#x200B;**首选项……**&#x200B;选项。 在[首选项](../../interface/preferences-window/preferences-window.md)窗口中，打开&#x200B;**3D视图**&#x200B;部分并将&#x200B;**视口缩放**&#x200B;参数设置为&#x200B;*无*。

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/demo-viewport-scaling-option.png){width="256px"}

</td>
</tr>
</table>

## 我找不到“镶嵌因子”属性

**![（错误）](../../assets/error.svg)问题**

将Designer升级到版本15.0.0后，我在材质属性中找不到“镶嵌因子”参数（该参数以前处于此位置）。

**![（刻度）](../../assets/check.svg)建议的步骤**

使用新渲染器（栅格化程序和GPU 路径追踪）时，“镶嵌因子”位于这些渲染器的属性中。 在3D视图中，转到<b>渲染器>编辑设置</b>。 该属性将列在“属性”停放区中。

>[!NOTE]
>
> 镶嵌的范围因渲染器而异：
> 
> * 栅格化程序/GPU 路径追踪：将全局应用于整个场景的唯一值。
> * OpenGL：每种材质一个值。
> * 图像：每个网格一个值。

## 3D对象看起来是错误的：它们的着色不适合光照

**![（错误）](../../assets/error.svg)问题**

对象的着色依赖于它们的法向量、切向量和二正规向量。 它们的坐标使用[-1， 1]范围，而正常地图在大多数情况下使用[0， 1]范围。 要使值从一个值到另一个值自适应调整，需要应用<b>偏差和比例</b>：value\*scale+偏差。

例如，比例2和偏差–1会将x值从[0， 1]调整为[-1， 1]：x\*2-1。

Designer不应用正常比例和偏差，除非它们由3D网格指定。 如果缺少该信息，则在[覆盖其任何素材](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)时，控制台中会出现警告：

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![（刻度）](../../assets/check.svg)建议的步骤**

对于不久前导出为美元格式的场景：使用最新版本的USD重新导出场景，这将包括必要的数据。 注意与正常比例和偏差相关的属性（如果有），这些属性将取决于用于导出场景的软件。

当[覆盖素材](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)时，Designer会处理网格并计算与其法线、切线和二项式相关的任何缺失数据。 如果Designer的默认缩放和偏差碰巧与网格所需的缩放和偏差相匹配，则当覆盖时网格看起来将正确无误。

## 启动3D 视图时崩溃

**![（错误）](../../assets/error.svg)问题**

Designer在启动3D 视图、创建项目、加载项目或手动启动3D 视图时崩溃。

**![（刻度）](../../assets/check.svg)建议的步骤**

首先，确保您的系统满足Designer的[系统要求](../../getting-started/system-requirements/system-requirements.md)。

然后，更新图形驱动程序。 您可以通过以下链接找到适用于您的GPU的最新驱动程序： [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [英特尔](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

如果您的系统包含集成的GPU (iGPU)和独立的GPU (dGPU)，请确保&#x200B;*更新两者的驱动程序*！

然后，禁用可能在3D图形流程中注入或叠加数据的任何软件。 示例包括：

* 后处理喷射器，如ReShade
* 叠加，例如自定义十字线或GPU性能度量
* 用于实时录制、流式传输或共享3D图形的屏幕捕捉软件
