---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: 使用3D视图场景菜单中的导出场景操作，导出包含在Designer中所做的所有编辑的3D场景。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出场景
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# 导出场景

当需要导出在Designer中所做的所有编辑的场景时，请使用[3D视图](../../interface/3d-view/3d-view.md)的“场景”菜单中的“导出场景……”操作。

对于以USD格式导出，场景的内容将与[场景浏览器](../../interface/3d-view/scene-browser/scene-browser.md)中显示的树相匹配。

对于其他格式，场景的内容及其内部结构将取决于选定文件格式所支持的功能。

>[!NOTE]
>
> 通过Designer添加到场景的所有项目都将包含在导出的场景中：默认相机、默认环境、所有材质都会复制任何附加光源。

![场景导出操作](exporting-scenes.resources/exporting-scenes-01.png "场景导出操作"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 导出场景

</td>
<td style="border: 0;" valign="top">

### 将场景导出为图层

</td>
<td style="border: 0;" valign="top">

### 纹理

</td>
</tr>
</table>

## 导出场景

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

“场景”菜单中的“导出场景……”操作会破坏性导出编辑后的3D场景：场景&#x200B;*拼合*，并且会丢失对原始场景的任何引用。

这意味着对原始场景的编辑完全不影响导出的场景。

</td>
<td style="border: 0;" valign="top">

![导出的场景文件 — 拼合](exporting-scenes.resources/exporting-scenes-02.png "导出的场景文件 — 拼合"){zoomable="yes"}

</td>
</tr>
</table>

## 将场景导出为图层

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

“将场景导出为图层……”操作会导出为<b>USD</b>格式(.usd、.usda、.usdc、.usdz)，且是&#x200B;*非破坏性*：主导出文件控制了一个&#x200B;*引用链*，其中新场景的所有编辑方面均存储到单独的USD文件中。

这意味着对原始场景的编辑会转移到导出的场景中。

</td>
<td style="border: 0;" valign="top">

![导出场景文件 — 分层](exporting-scenes.resources/exporting-scenes-03.png "导出场景文件 — 分层"){zoomable="yes"}

</td>
</tr>
</table>

导出的文件遵循以下结构：

* <b>主文件</b>
  * <b>.layers</b>：引用下面的子图层并声明素材覆盖，该覆盖将几何形状绑定到Designer创建的素材副本。
    * <b>.assembly</b>：引用.scene#文件并声明几何覆盖，这将使Designer重新计算的数据包含受覆盖的材质影响的几何。
      * <b>.scene#</b>：引用原始场景。
    * <b>.camera</b>：声明Designer添加到场景中的摄像机。
    * <b>.light</b>：声明Designer添加到场景的光线。
    * <b>.material</b>：声明Designer添加到场景的材质副本，这些副本使用导出的纹理。

## 纹理

纹理将导出到所导出文件旁边的目录中，并以该文件命名，后缀为“<b>\_textures</b>”。

它们使用<b>PNG</b>格式，但HDR纹理（浮点）除外，其使用<b>EXR</b>格式。
