---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/scene-browser.html"
breadcrumb-title: ''
description: 使用场景浏览器导航和管理视区中的3D场景元素、素材和对象。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Scene browser
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 场景浏览器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 1%

---


# 场景浏览器

3D视图的场景浏览器会列出场景中的所有元素及其层次结构。

它提供了用于选择对象、切换对象的可见性以及选择哪些素材应[覆盖场景素材](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)的控件。

由于Designer使用[USD](https://openusd.org/release/index.html)来描述和管理其场景，因此可以在场景树中找到它的术语和概念。

通过单击[3D视图场景工具栏](../../../interface/3d-view/3d-view.md)中的专用切换按钮![](../../../assets/sceneBrowser-toggleButton.png)，可显示它。

![场景浏览器 — 加载的3D场景](../../../assets/loaded3DScene.png "场景浏览器 — 加载的3D场景"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 场景树

</td>
<td style="border: 0;" valign="top">

### 切换场景中的对象

</td>
<td style="border: 0;" valign="top">

### 连接的材质

</td>
</tr>
</table>

## 场景树

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

场景浏览器显示以分层树排列的对象列表。

对象被置于其他对象的父子关系中，直至场景的根。 父对象有一个箭头按钮，用于展开或折叠其子对象的列表。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![场景浏览器 — 场景树](../../../assets/sceneBrowser-sceneTree.png "场景浏览器 — 场景树"){zoomable="yes"}

</td>
</tr>
</table>

将光标置于树中的任意项目上几秒钟，以显示工具提示，其中包含下列信息：

* <b>路径：</b>场景中对象的完整路径。
* <b>类型名称：</b>对象的USD类型。
* <b>文档：</b>有关作为USD场景元素的对象的详细信息。

网格具有附加信息：顶点计数、面部计数和UV计数。

### 由Designer添加的对象

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designer可将一些对象添加到任何加载的场景。 由Designer添加的对象以<b>粗体</b>标记。

在光线、相机和环境菜单中使用“编辑……”操作时，无论场景中是否存在其他光线、相机或环境，这些对象都是正在编辑的对象。

[导出](../../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)时，场景中包含这些对象。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![场景浏览器 — Designer添加的对象以粗体列出](../../../assets/sceneBrowser-addedByDesigner.png "场景浏览器 — Designer添加的对象以粗体列出"){zoomable="yes"}

</td>
</tr>
</table>

* <b>摄像机：</b>场景的默认摄像机。 这是您唯一可以在Designer中与之交互的相机。 加载的场景中包含的所有摄像机都会添加为默认摄像机的预设。
* <b>环境：</b>场景的默认环境。 应用于场景环境的任何纹理将仅应用于该环境。 同样，环境旋转也只会影响该环境。\
  当加载的场景包含一个或多个环境光时([DomeLight](https://openusd.org/release/user_guides/schemas/usdLux/DomeLight.html)（美元）)，将自动禁用默认环境以不干扰场景的环境光照。
* <b>点光#：</b>如果在“光源”>“编辑属性”中启用了任何Designer点光，则每个点光都会添加到场景中。

## 切换场景中的对象

### 所有类型

可以在场景中启用和禁用任何对象。 禁用后，对象将对场景不再起作用：它不再投影、发光或反射光线。

父对象的状态会传递到其子对象，因此禁用父对象也会禁用其子对象。

通过单击对象的眼睛按钮![](../../../assets/sceneBrowser-eyeButton.png)或单击对象的上下文菜单，可以切换对象的可见性。 该菜单提供了更多用于管理场景对象可见性的操作：

* <b>隐藏：</b>禁用所选对象。
* <b>显示：</b>启用所选对象。

某些操作会特别影响网格的可见性：

* <b>仅显示：</b>禁用除选定网格及其子网格之外的所有网格。
* <b>显示全部：</b>启用所有网格。

父对象具有以下附加操作：

* <b>隐藏子项：</b>递归禁用选定对象的所有子项。
* <b>显示子级：</b>递归启用选定对象的所有子级。
* <b>展开所有子项：</b>递归展开所选对象下的所有子项列表。
* <b>折叠所有子项：</b>递归折叠所选对象下的所有子项列表。

![场景浏览器 — 切换对象可见性](../../../assets/sceneBrowser-toggleVisibility.gif "场景浏览器 — 切换对象可见性"){zoomable="yes"}

### 环境

任何环境光(DomeLight)的可见性都可以像其他对象一样被启用和禁用。

禁用环境光时，也会禁用环境光对场景的光照贡献。

如果启用了多个环境光，则它们的光照贡献是&#x200B;*累加*。

![场景浏览器 — 切换环境可见性](../../../assets/sceneBrowser-toggleEnvLights.gif "场景浏览器 — 切换环境可见性"){zoomable="yes"}

### 光源

场景中的任何光线都是一样的：可以单独切换每个光线。

![场景浏览器 — 切换光照可见性](../../../assets/sceneBrowser-toggleLights.gif "场景浏览器 — 切换光照可见性"){zoomable="yes"}

## 连接的材质

场景浏览器还允许您将任何被覆盖材质连接到Designer在3D视图的[材质菜单](../../../interface/3d-view/3d-view.md)中列出的其他材质。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Designer列出的素材是场景树中的素材对象，至少在一个网格上使用。

当[覆盖](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)这些素材中的任意素材时，Designer会创建一个带有数字后缀的副本。

被覆盖素材在其上下文菜单中提供了一个附加项：“[已连接素材](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)”子菜单列出可用于覆盖此素材的所有其他可用素材。

</td>
<td style="border: 0;" valign="top">

![场景浏览器 — 连接的素材](../../../assets/sceneBrowser-connectedMaterial.png "场景浏览器 — 连接的素材"){zoomable="yes"}

</td>
</tr>
</table>
