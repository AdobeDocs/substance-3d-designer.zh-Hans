---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: 了解如何从Substance 3D Designer导出MDL内容，以便在外部渲染器和应用程序中使用。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出MDL内容
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---


# 导出MDL内容

本页介绍与Substance 3D Designer中的[MDL 图](../../mdl-graphs/mdl-graphs.md)和材料相关的导出过程。

## 概述

在Designer中创作MDL 材质后，需要将其导出为可以&#x200B;*包含材料定义*&#x200B;且可由支持MDL的渲染器读取的格式。 MDL使用专有格式来包含材料定义，这些定义称为MDL 模块，它们以不同格式编写和打包，并且都可以从Designer中导出。

>[!NOTE]
>
> 所有这些格式都可以使用&#x200B;*文本编辑器*&#x200B;直接打开（有时在用归档管理器解包之后），以检查它们所包含的材料定义。

## MDL 模块(\*.mdl)

这是材料定义的基本交换文件格式。 MDL 模块定义以下内容：

* 材料的特性和行为
* 其公开参数和默认值
* 其批注（即元数据）：作者、标签、类别……

导出MDL 模块是在&#x200B;*包*&#x200B;级别执行的。 若要导出给定包的MDL 模块，请单击[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中的![](exporting-mdl-content.resources/mdl-export-module-icon.png) <b>导出MDL 模块</b>按钮，或在&#x200B;*包的上下文菜单*&#x200B;中选择该相同选项。 为导出的MDL 模块选择目标位置和名称，将显示<b>导出报告</b>对话框，其中显示了在导出过程中记录的消息列表。

导出的模块将包含包中[MDL 图](../../mdl-graphs/mdl-graphs.md)定义的&#x200B;*所有* MDL 材质的定义。

>[!NOTE]
>
> 在NVIDIA的[MDL规范](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9)的第4节和第15节中了解有关MDL 模块的更多信息。

>[!NOTE]
>
> 此模板之后的警告： `x appears to be invalid whereas it was expected to be an mdl::call`是由在MDL 图中处理MDL 材质的方式造成的，并且&#x200B;*可以安全忽略*。

![MDL导出途径](exporting-mdl-content.resources/mdl-export-module.png "MDL导出途径")

*资源管理器中的“导出MDL模块”路径以及生成的“导出报告”对话框*

### MDL预设(\*.mdl)

MDL模块预设与其所基于的模块大致相同，唯一区别在于它带有一组不同的默认值 — 在[此处](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details)了解更多信息。

可以从以下位置导出分配给场景材质`my_material`的MDL材质的预设：

* 在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中，单击MDL图形资源上的<b>人民币</b>，然后在上下文菜单中选择<b>导出预设……</b>选项
* [3D视图](../../interface/3d-view/3d-view.md)面板，使用<b>材质> my\_material >导出预设……</b>菜单选项

菜单选项将打开<b>导出MDL材质预设</b>对话框，该对话框提供以下选项：

* <b>目录</b>：导出MDL模块的目标位置
* <b>MDL文件名</b>： MDL模块的名称
* <b>嵌入导入的MDL模块</b>：如果MDL模块依赖于导入的模块，即具有任何模块依赖项，则选中此选项会将模块依赖项&#x200B;*嵌入*&#x200B;导出的MDL模块，从而使其有效&#x200B;*自给自足*，但代价是文件大小和动态继承

导出的预设将在3D视图中使用素材的参数&#x200B;*当前值*&#x200B;作为&#x200B;*新默认值*&#x200B;值。 可以使用<b>材料> my\_材料>编辑</b>选项修改这些值，该选项将在“属性”面板中显示材料的公开参数。

>[!WARNING]
>
> 从[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中导出MDL模块时，会导致某个MDL模块包含&#x200B;*所有*&#x200B;由包中的MDL图表定义的MDL材质，从[3D视图](../../interface/3d-view/3d-view.md)中导出MDL预设会导致某个MDL模块仅包含&#x200B;*7&rbrace;应用于*&#x200B;所选材质&#x200B;*的MDL材质定义，在本示例中为`my_material`。*

![MDL预设导出路径](exporting-mdl-content.resources/mdl-export-preset.png "MDL预设导出路径")

*3D视图中的“导出预设”路径以及生成的“导出MDL素材预设”对话框*

## MDL模块存档(\*.mdr)

MDL模块存档将MDL模块（见上文）与&#x200B;*纹理*&#x200B;和自述文件等资源合并为一个&#x200B;*单个可传输文件*。

导出MDL模块存档是在&#x200B;*包*&#x200B;级别执行的。 若要导出给定包的MDL模块存档，请单击[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中的![](exporting-mdl-content.resources/mdl-export-module-icon.png) <b>导出MDL模块存档</b>按钮，或在&#x200B;*包的上下文菜单*&#x200B;中选择相同的选项。 为导出的MDL模块存档选择目标位置和名称，此时会显示<b>导出报告</b>对话框，其中包含导出过程中记录的消息列表。

导出的模块存档将包含MDL模块，其中包含包中[MDL图形](../../mdl-graphs/mdl-graphs.md)定义的&#x200B;*所有* MDL材料的定义。 如果[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)已[实例化到MDL图形](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)中并连接到指向[根](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)节点的流，则它输出的纹理&#x200B;*将保存到存档中*。

除了这些项之外，存档还包含一个<b>MANIFEST</b>文件，该文件描述了MDL模块存档的以下元数据：

* `mdl`：用于导出模块存档的MDL版本 — 例如“1.5”
* `version`：模块存档的版本 — 例如“1.0.0”
* `module`：模块存档的名称 — 例如“：：pbr\_metallic\_roughness\_basic”
* `exports.material`：材料存档中定义的模块的名称 — 例如“：：pbr\_metallic\_roughness\_basic：：MDL\_图形”

>[!NOTE]
>
> 在NVIDIA的[MDL规范](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9)的附录C中了解有关MDL存档文件格式的更多信息。

![MDR导出途径](exporting-mdl-content.resources/mdl-export-archive.png "MDR导出途径")

*资源管理器中的“导出MDL 模块归档”路径以及生成的导出报告对话框*

## MDL封装模块(\*.mdle)

带有公开参数的MDL 图可以导出为封装MDL 材质。 封装&#x200B;*将数据包装*&#x200B;到专用类中，以便不能直接访问数据&#x200B;**。

例如，虽然您仍然可以修改公开参数的值以控制材料的行为，但在封装的MDL 模块中，这些参数的&#x200B;*定义*&#x200B;是&#x200B;*不可用*。

通过选择MDL 图上下文菜单中的<b>导出为.mdle</b>选项，可以在MDL 图级别的[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中导出封装MDL 模块。 为导出的MDL封装模块选择目标位置和名称，将显示<b>导出报告</b>对话框，其中显示了在导出过程中记录的消息列表。

*仅*&#x200B;在导出的封装材料中将包含&#x200B;*选定MDL 图*&#x200B;的MDL 模块定义。

>[!NOTE]
>
> 了解更多有关NVIDIA的[MDL规范](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9)和[MDL SDK API](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html)的第13.5节中封装的材料定义。

![MDLE出口途径](exporting-mdl-content.resources/mdl-export-encapsulated.png "MDLE出口途径")

*资源管理器中的“导出为中间文件”路径以及生成的导出报告对话框*
