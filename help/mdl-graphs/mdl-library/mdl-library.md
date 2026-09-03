---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: 访问Substance 3D Designer中的材质定义语言库以创建自定义材质。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL库
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# MDL库

此页面显示与Substance 3D Designer中包含的[MDL图表](../../mdl-graphs/mdl-graphs.md)和材质相关的内容库。 还介绍了如何在[库](../../interface/the-library/the-library.md)中安装和管理自定义内容。

## 库中的MDL内容

在[库](../../interface/the-library/the-library.md)的<b>mdl</b>部分中提供了MDL图形中可用的节点。 根据节点所定义的MDL模块将节点排列成过滤器。\
如果模块存储到子文件夹中，此层次结构将在库中作为&#x200B;*类别*&#x200B;进行&#x200B;*镜像*。

本节包含来自以下来源的内容：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 内置内容

Designer包含一些MDL模块，这些模块包含用于创作MDL图表的基本构建块，以及准备好使用的完整材质定义。

此内容存储在安装目录`./resources/view3d/iray/`下的此位置

### 自定义内容

除了内置内容之外，您还可以将&#x200B;*您自己的* MDL模块添加到库中。

事实上，在[项目设置](../../interface/preferences-window/project-settings/project-settings.md)的<b>MDL</b>部分中列出的目录下找到的任何MDL模块都会跨项目文件&#x200B;*累计*&#x200B;添加到此部分。

### NVIDIA素材版

如果安装了NVIDIA的[vMaterials](https://developer.nvidia.com/vmaterials)库，则会将其&#x200B;*自动添加*&#x200B;到其&#x200B;*自己的类别*&#x200B;下的库中。

</td>
<td style="border: 0;" valign="top">

![库中的MDL资源](mdl-library.resources/mdl-library-01.png "库中的MDL资源")

将设置库、vMaterials库和自定义内容中的&#x200B;*“mdl”部分的框架*

</td>
</tr>
</table>

## 3D视图中的MDL内容

使用Iray渲染器时，库中可用的所有MDL模块都可以在[3D视图](../../interface/3d-view/3d-view.md)中使用。

打开<b>材质</b>菜单，然后打开&#x200B;*场景材质的子菜单*&#x200B;以浏览可用的MDL模块。 这些列表包括：

* 内置内容
* 自定义内容
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* 已加载[个MDL图形](../../mdl-graphs/mdl-graphs.md)

![3D视图中的MDL材质](mdl-library.resources/mdl-library-02.png "3D视图中的MDL材质")

*3D视图中的MDL材质*
