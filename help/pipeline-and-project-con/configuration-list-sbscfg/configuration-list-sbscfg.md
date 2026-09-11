---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中使用SSBSCFG配置列表来管理项目设置和预设。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 配置列表 — SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# 配置列表 — SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

配置文件比[项目配置文件](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)简单得多，因为它仅包含项目列表以及引擎兼容模式。 与单个项目文件相比，它们可用作更高级别的项目/环境配置列表。

您可以针对不同的环境使用多种配置，这些文件可以与SBSPRJ文件一起保持版本控制。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSCFG文件图标](configuration-list-sbscfg.resources/sbscfg.png "SBSCFG文件图标")

</td>
</tr>
</table>

## 修改配置文件

这些文件很简单，但仍然可以用两种不同的方式修改它们，就像SBSPRJ文件一样。

### 在项目设置中

突出显示的部分是与配置文件相关的部分，您只需将更多项目添加到列表，这些项目存储在上面定义的SSBSCFG文件中。

![项目设置](configuration-list-sbscfg.resources/config-ui.png "项目设置")

### 以XML形式进行外部编辑

对于Windows <b>Notepad++</b>是一个很好的免费选项，而macOS <b>Sublime Text</b>是一个替代方案。 但是，任何具有适当缩进、节折叠和某种形式的语法突出显示功能的编辑器都会使您的生活更加轻松。

在编辑器中打开SSBSCFG文件后，您应该会看到一个相当简单的结构化布局，其中包含与UI对应的部分。

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


请注意，未明确列出默认项目和用户项目，并且任何其他项目均是在这些项目之后定义的。

上例还使用了[相对路径](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)。 请注意，相对路径的逻辑在CFG文件和PRJ文件之间略有不同：如上所述，对于CFG文件，**不应在路径前键入“file:/”**。 相反，路径仅被附加到在其中定义路径的CFG文件的位置。

## 删除默认库

目前，无法删除默认库。 反正这样做可能不是个好主意，因为这样会失去很多Designer功能。
