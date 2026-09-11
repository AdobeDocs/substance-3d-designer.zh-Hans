---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中使用SBSPRJ项目配置文件来管理项目设置。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 项目配置文件 — SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# 概述

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>项目配置文件</b>是用于配置Substance 3D Designer的最复杂且最扩展的文件。

它们具有特殊性，因为您可以使用多个项目配置文件，其中每个下一个“子”项目将扩展或覆盖上一个“父”。 除非明确需要，否则不应修改设置或将设置添加到项目文件，以便Designer可以回退到其父级配置，甚至是默认设置。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSPRJ文件图标](../../assets/sbsprj.png "SBSPRJ文件图标")

</td>
</tr>
</table>

默认情况下，Designer具有两个活动项目配置：

<b>默认项目： </b>包含所有默认设置，并且Designer随附库用于全新安装。*只读，无法修改或删除。*

<b>用户项目： </b>由于默认值是只读的，默认情况下，*用户所做的任何更改*&#x200B;都会进入此项目。 *无法删除。*

这种基本设置可确保默认库和其他设置不会被损坏或修改，但仍允许单个业余用户添加自己的修改，而无需费心使用复杂的设置。

## 展开或覆盖

连续项目中的大多数设置将<b>覆盖</b>上一个项目中的设置。 例如，自定义项目文件中的其他Tangent Space插件将覆盖在Default或User项目中定义的任何TS插件。 这意味着，除非明确需要，否则建议不要覆盖或更改子项目中的设置。

但是，有些设置是根据父设置<b>扩展</b>的，而不是覆盖它们。 最值得注意的是，这些设置是库路径和过滤器，因此您始终可以向库添加更多内容，而不是覆盖库。 此外，还会扩展别名（相对文件路径的路径关键字），如果定义了副本，则会覆盖这些别名。 这样可以更好地控制内容文件路径和引用。

## 项目文件内容

项目文件可以包含以下设置：

<b>3D 视图： </b>默认着色器、HDR和场景状态定义。

<b>别名： </b>相对路径的关键字别名。

<b>烘焙： </b>烘焙命名约定的设置。

<b>常规： </b>图形模板、切线空间增效工具、普通和图像格式默认值。

<b>库： </b>监视要在库中显示的路径。

<b>脚本： </b>回调脚本和解释器。

<b>版本控制： </b>将版本控制集成到Designer中的设置。

## 修改项目文件

与所有其他类型一样，项目配置也另存为结构化XML文件（使用<b>.sbsprj</b>扩展名），可通过Designer UI或外部文本编辑器进行修改。

## Substance 3D Designer内部

请参阅[项目设置](../../interface/preferences-window/project-settings/project-settings.md)页面，了解有关管理项目文件和更改项目设置的更多信息。

项目文件还包括[库](../../interface/the-library/the-library.md)的自定义<b>类别</b>和<b>筛选器</b>，您可以在[管理自定义内容和筛选器](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)页面中详细了解这些内容。

## 在外部编辑XML

对于Windows，[记事本++](https://notepad-plus-plus.org)是一个很好的免费选项。 在macOS上，[Sublime Text](https://www.sublimetext.com/)是替代方法。 尽管如此，任何具有适当缩进、部分折叠和某种形式的语法突出显示功能的编辑都将使您的生活更加轻松。

在编辑器中打开SBSPRJ文件后，您应该会看到一个相当简单的结构化版面，其中的各部分与UI中的选项卡相对应。 并非所有设置都会记录在这里，因为它相当容易解释。

![XML编辑](../../assets/project-xml.png "XML编辑")

## 相对路径和别名

与别名结合的相对路径是比较复杂但最重要的项目配置部分之一，本节将对其进行说明。 在[项目设置](../../interface/preferences-window/project-settings/project-settings.md)中为特定项目文件添加自定义别名。

在多台用户的PC上，文件引用系统中其他文件的主要问题之一是绝对文件路径不起作用。 用户可以在完全不同的位置(例如， C：/John/Gamedev/SubstanceLibrary或D：/Dev/SubstanceLibrary)。 别名和相对路径共同解决这个问题。 否则，您可能会打开其他人的文件，而该文件将尝试查找用户本地拥有该文件的特定位置所使用的自定义节点，您可能没有以完全相同的方式定义该节点。

<b>别名</b>是替换（部分）路径的关键字。 它类似于Windows环境变量（如%TEMP%），其中单个单词替换了经常使用的路径，然后该路径被集中定义。 优点是简化了所有位置的路径，并且当您决定重定位此路径时，可以一次性修改所有引用。

>[!NOTE]
>
> **别名示例**
> 
> | 别名 | 实际路径值 |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>自定义</b> | *D:\Dev\CustomProject\Substance* |
> 
> 默认库默认位于&#x200B;*C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*，所有使用默认内容的图形都引用此目录。 定义了“<b>SBS</b>”（不带引号）的别名，而不是引用完整路径。 对于默认库，将SBS路径的确切值在安装时设置为用户为Designer选择的任何目录。
> 
> 当引用包含带别名的路径时，在内部按以下方式修改引用：
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>blur\_hq.sbs**

<b>相对路径</b>始终相对于在其中定义它们的文件。 这意味着配置文件的当前位置决定了大部分路径，而别名路径将基于它，主要通过添加子文件夹来实现。 <b>这意味着强烈建议将sbsprj文件放在要监视的文件夹旁边！</b>

例如，在&#x200B;*C：/Versioncontrol/tools/*&#x200B;处获取一个包含&#x200B;*CustomProject.sbsprj*&#x200B;的存储库，然后获取两个文件夹，*/Base*&#x200B;和&#x200B;*/Tools，*，这两个文件夹包含节点。

在SBSPRJ文件中，为“基础”和“工具”定义两个相对别名将按照如下方式执行：

### C：/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


此配置文件的结果如下：

**BaseAlias://**&#x200B;将为&#x200B;*C：/Versioncontrol/Substance/Base/*，**ToolsAlias://**&#x200B;将为&#x200B;*C：/Versioncontrol/Substance/Tools/.*

如果只想定义&#x200B;*C：/Versioncontrol/path/*，Substance将列为&#x200B;**&quot;file：.&quot;**，点表示文件本身的位置。
