---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/working-with-3d-scenes.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中导入、编辑和使用3D场景以预览和测试您的素材。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用3D场景
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---


# 使用3D场景

![处理3D场景](../assets/workingWith3DScenes.png "处理3D场景"){zoomable="yes"}

通过Designer，可加载[3D场景](../glossary/glossary.md)以处理上下文中的材质。 您可以在此处找到支持3D场景的文件格式列表，包括每种格式支持的功能列表。 <b>&lt;需要链接></b>

在上下文中工作涉及[覆盖](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)场景的[材质](../glossary/glossary.md)之一，以将其替换为Designer中创作的材质。\
您可以从头开始使用Designer中提供的任何Substance图形模板，或从3D场景的素材中[提取值和纹理](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)作为起点。

完成3D场景处理后，您可以[将其导出](../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)到新文件中，以便在其他应用程序中收录。

导出为USD格式时，此工作流程可以完全<b>非破坏性</b>，这意味着仅导出编辑和添加。

首先，您需要加载3D场景才能处理，并且能够在会话间在Designer中保留其状态。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 3D场景的内容

</td>
<td style="border: 0;" valign="top">

### 加载场景

</td>
<td style="border: 0;" valign="top">

### 场景状态文件

</td>
</tr>
</table>

## 3D场景的内容

加载3D场景时，Designer会创建自己的场景来承载它。

您可以与场景的以下内容进行交互：

* <b>素材：</b>场景中使用的所有素材都可以[覆盖](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)，并使用Designer创建的副本。 您可以使用Substance图表中的原始值或纹理来编辑该副本的[素材属性](../interface/3d-view/material-properties/material-properties.md)。
* <b>网格：</b>可以直接在视口中或从[场景浏览器](../interface/3d-view/scene-browser/scene-browser.md)选取几何以访问其材质操作（[覆盖](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)、[重置](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)、[提取到Substance图形](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)）
* <b>光源：</b>场景中的所有光源都可以在[场景浏览器](../interface/3d-view/scene-browser/scene-browser.md)中禁用。
* <b>摄像机：</b>场景中检测到的所有摄像机都会作为预设添加到Designer添加的摄像机中。

![3D场景的内容](../assets/loaded3DScene.png "3D场景的内容"){zoomable="yes"}

Designer对其3D 场景使用USD描述。 其布局可以在场景浏览器中导航，其中每个[USD素材](https://openusd.org/release/glossary.html#usdglossary-prim)类型都有自己的图标（几何、材料、着色器、相机、变换...）。

[场景浏览器](../interface/3d-view/scene-browser/scene-browser.md)可用于选择、启用和禁用场景的内容。 因此，我们建议您在使用自定义3D场景时保持该屏幕显示。

## 加载场景

在3D 视图中加载3D 场景有几种途径：

1. 双击或将[3D 场景资源](../resources/3d-scene-resource/3d-scene-resource.md)从[包](../glossary/glossary.md)拖动到3D 视图中
1. 将3D 场景项从[库](../interface/the-library/the-library.md)拖到3D 视图中（前提是您已[将自己的内容添加到库](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)）
1. 将3D 场景文件从系统的文件浏览器拖动到3D 视图中
1. 载入3D 场景状态文件(SBSSCN)及其引用的网格

请注意，只有方法1和4可以让您完全按照上次处理场景时的状态再次加载模板，因为场景的状态会写入3D 场景资源和场景状态文件中并保存在包中。 方法2和3将场景加载为任意其他格式。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![加载3D 场景 — 从3D 场景资源](../assets/load3DScene-3DSceneResource.gif "加载3D 场景 — 从3D 场景资源"){zoomable="yes"}

加载3D 场景资源

</td>
<td style="border: 0;" valign="top">

![加载3D 场景 — 从库](../assets/load3DScene-Library.gif "加载3D 场景 — 从库"){zoomable="yes"}

从库中加载3D 场景

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![加载3D 场景 — 从3D 场景文件](../assets/load3DScene-3DSceneFile.gif "加载3D 场景 — 从3D 场景文件"){zoomable="yes"}

加载3D 场景文件

</td>
<td style="border: 0;" valign="top">

![加载3D 场景 — 从场景状态文件](../assets/load3DScene-sceneStateFile.gif "加载3D 场景 — 从场景状态文件"){zoomable="yes"}

正在加载场景状态文件

</td>
</tr>
</table>

>[!NOTE]
>
> [3D 视图文档](../interface/3d-view/3d-view.md)涵盖了在3D 视图中导航和可视化场景。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

除了场景中可能存在的环境之外，Designer始终创建自己的环境（在USD中为DomeLight）和相机。

Designer创建的任何项目均在场景浏览器中用<b>粗体标签</b>列出。

>[!NOTE]
>
> 当加载的场景至少有一个环境(DomeLight)时，默认情况下，Designer创建的环境&#x200B;*处于禁用状态*，因此它不会干扰场景的环境光照。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![场景浏览器 — 由Designer创建的元素](../assets/sceneBrowser-createdByDesigner.png "场景浏览器 — 由Designer创建的元素"){zoomable="yes"}

</td>
</tr>
</table>

## 场景状态文件

在3D 视图中设置材料、相机、灯光等后，可将该状态保存到场景状态文件(.sbsscn)中，稍后可加载该文件以恢复该状态。 例如，您可能需要设置一些场景来预览不同类型的环境或特定照明材料。

![加载场景状态文件](../assets/loadSceneStateFile.gif "加载场景状态文件"){zoomable="yes"}

保存的场景状态还可以用作3D 视图的默认状态，这样，每当创建新3D 视图时，都将使用该状态。 如果想在拼贴值为2且特定环境图的“球体2拼贴”网格上默认预览材料的材料，此功能非常有用。

与场景状态文件相关的操作位于3D 视图的“场景”菜单中，在[此处](../interface/3d-view/3d-view.md)介绍了相关操作。

场景状态文件使用XML格式，并使用[别名](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)（如果在您的[项目设置](../interface/preferences-window/project-settings/project-settings.md)中定义了别名）。

>[!NOTE]
>
> 渲染器未保存到场景状态文件。
