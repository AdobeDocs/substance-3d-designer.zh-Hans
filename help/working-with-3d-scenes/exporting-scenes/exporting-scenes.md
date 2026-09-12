---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: 使用“场景”菜单中的导出场景操作，导出包含在Designer中所做的所有编辑的3D3D 视图。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出场景
user-guide-description: ''
user-guide-title: ''
source-git-commit: fa12f0ba789f700924fa0a6f3cbc0726c5f468e9
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# 导出场景

当需要导出包含在Designer中所做的所有编辑的场景时，请使用[3D 视图](../../interface/3d-view/3d-view.md)的“场景”菜单中的“导出场景...”操作。

对于导出为USD格式，场景的内容将与[场景浏览器](../../interface/3d-view/scene-browser/scene-browser.md)中显示的树相匹配。

对于其他格式，场景的内容及其内部结构将取决于选定文件格式所支持的功能。

>[!NOTE]
>
> Designer添加到场景中的所有项目都将包含在导出的场景中：默认相机、默认环境、所有材料复制任何其他光源。

![场景导出操作](exporting-scenes.resources/exportActions.png "场景导出操作"){zoomable="yes"}

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

“场景...”菜单中的“导出场景...”操作会以破坏性方式导出编辑的3D场景：场景&#x200B;*拼合*，对原始文档的任何引用都将丢失。

这意味着对原始场景的编辑根本不会影响导出的场景。

</td>
<td style="border: 0;" valign="top">

![导出的场景文件 — 拼合](exporting-scenes.resources/exportFlattened.png "导出的场景文件 — 拼合"){zoomable="yes"}

</td>
</tr>
</table>

## 将场景导出为图层

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

“将场景导出为图层……”操作会导出为<b>USD</b>格式(.usd、.usda、.usdc、.usdz)，且是&#x200B;*非破坏性*：主导出文件将形成&#x200B;*引用链*，其中新场景的所有编辑方面均存储到单独的USD文件中。

这意味着对原始场景的编辑会转移到导出的场景。

</td>
<td style="border: 0;" valign="top">

![导出的场景文件 — 分层](exporting-scenes.resources/exportLayered.png "导出的场景文件 — 分层"){zoomable="yes"}

</td>
</tr>
</table>

导出的文件遵循以下结构：

* <b>主文件</b>
  * <b>.layers</b>：引用下面的子图层并声明材料覆盖，该覆盖将几何绑定到Designer创建的材料副本。
    * <b>.assembly</b>：引用.assembly#文件并声明几何覆盖，这将使Designer重新计算的数据包含受覆盖材料影响的几何。
      * <b>.场景#</b>：引用原始场景。
    * <b>.相机</b>：声明由Designer添加到场景的相机。
    * <b>.light</b>：声明Designer添加到场景的光照。
    * <b>.材料</b>：声明Designer添加到场景的材料副本，这些副本使用导出的纹理。

## 纹理

纹理将导出到所导出文件旁边的目录中，并以该文件命名，后缀为“<b>\_纹理</b>”。

它们使用<b>PNG</b>格式，使用<b>EXR</b>格式的HDR纹理（浮点）除外。
