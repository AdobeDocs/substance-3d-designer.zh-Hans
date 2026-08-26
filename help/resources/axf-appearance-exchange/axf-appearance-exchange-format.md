---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/resources/axf-appearance-exchange-format.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中导入和使用AxF外观交换格式资源进行材质导入。
helpx_creative_field: ""
helpx_description: Designer > Resources > AxF (Appearance eXchange Format)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AxF（外观交换格式）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '2140'
ht-degree: 0%

---


# AxF（外观交换格式）

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

[![AxF文件图标](../../assets/axf-file-icon.png)](https://www.xrite.com/axf)

</td>
<td width="100.00%" style="border: 0;" valign="top">

Substance 3D Designer支持[X-Rite的外观交换格式。](https://www.xrite.com/axf) 该格式的创建者按如下方式描述它：

“AxF文件在整个数字设计工作流程中用于捕获、存储、编辑和传达复杂的材料特性。 AxF提供了一种标准方式来存储和共享所有相关外观数据 — 颜色、纹理、光泽、折射、半透明、特效（火花）和反射属性 — 跨产品生命周期管理(PLM)、计算机辅助设计(CAD)和一流的渲染应用程序。

</td>
</tr>
</table>

简而言之， AxF文件包含许多由X-Rite的TAC7扫描仪硬件提取的纹理，再加上描述材料附加属性的元数据。 这意味着AxF不仅仅是纹理数据，它还具有着色属性。

AxF文件&#x200B;*未*&#x200B;作为包[资源](../../resources/resources.md)导入。 相反，[导入过程](#import)涉及从AxF文件中提取纹理和元数据，然后使用这些纹理和元数据准备从[专用模板](#graph-templates)创建的图形。

可用的模板针对两个AxF工作流：

* <b>将AxF文件中的SVBRDF素材转换为PBR素材</b>；
* <b>正在就地编辑</b>SVBRDF素材，并[将其](#export)导出为现有AxF文件作为新图层。

>[!NOTE]
>
> 支持的材质模型
> 
> 只有使用<b>SVBRDF</b>（空间变化BRDF）模型的素材才能&#x200B;*完全*&#x200B;加载并在Designer中编辑。
> 
> 可以加载使用<b>EP-SVBRDF</b>（节能SVBRDF）模型的材料，但只能编辑和可视化SVBRDF模型中存在的功能。 不支持EP-SVBRDF独有的功能。
> 
> 不支持其他模型。

## 导入AxF文件

AxF文件导入工作流程可以从以下两种方法之一启动：

+++主屏幕

单击[主屏幕](../../interface/home-screen/home-screen.md)左侧部分中的<b>导入AxF...</b>按钮。

![AxF：从主屏幕开始导入](../../assets/axf_home-screen.png "AxF：从主屏幕开始导入"){width="600px"}

+++

+++资源管理器

在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中单击包上的RMB，然后转到包上下文菜单中的<b>导入> AxF</b>。

![AxF：从资源管理器开始导入](../../assets/axf_explorer.png "AxF：从资源管理器开始导入"){width="600px"}

+++

### “导入”对话框

通过<b>AxF导入</b>对话框，可以查看从所选AxF文件加载的数据，并设置执行预期编辑或转换所需的图形模板。

它包含四个部分：

<b>标题</b>显示在AxF文件中检测到的材料的名称及其表示形式（当前始终为SVBRDF）。 还会显示嵌入到文件中的预览缩览图。

通过<b>模板</b>部分，您可以设置[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)模板，以开始处理素材。 请参阅下面的[图形模板](#graph-templates)部分以了解有关这些模板以及设置它们的更多信息。

<b>纹理</b>列出了从检测到的材料中涉及的AxF文件提取的所有纹理。 对于每个纹理，都会显示其名称、本机分辨率、数据格式和物理尺寸。

<b>元数据</b>和<b>属性</b>列出从AxF文件中的素材提取的数据。 这些对于配置某些Substance图形模板属性的方式有影响（请参阅下面的[图形模板](#graph-templates)部分）。

![AxF：导入对话框](../../assets/axf_import.png "AxF：导入对话框")

### 结果

单击<b>确定</b>按钮后，将在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中创建包。 该包包含以下资源：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

对于从AxF文件导入的每个材料，<b>资源</b>文件夹都承载一个&#x200B;*子文件夹*。

每个子文件夹都包含另一个子文件夹，该子文件夹包含从AxF文件中为该素材提取的&#x200B;*纹理*。 最后一个子文件夹以纹理使用的材质&#x200B;*表示法*&#x200B;命名（当前仅<b>SVBRDF</b>）。

在导入对话框的<b>模板</b>部分中设置的每个模板的图形。\
对于[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)，这些模板已使用从AxF文件中提取的纹理和数据以及您选择的模板设置进行了预配置（请参阅下面的“图形模板”部分）。

</td>
<td style="border: 0;" valign="top">

![AxF：导入过程的包结果](../../assets/axf_package.png "AxF：导入过程的包结果")

</td>
</tr>
</table>

## 图表模板

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

有专用于处理[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)的AxF工作流的图形模板。

单击<b>添加模板</b>按钮，然后在下拉菜单中选择所需的图形类型。

</td>
<td style="border: 0;" valign="top">

![AxF：在导入对话框中添加模板](../../assets/axf_add-template.png "AxF：在导入对话框中添加模板")

</td>
</tr>
</table>

### Substance图形模板

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

有两种类型的Substance图模板可用：

<b>AxF到金属粗糙度</b>和<b>AxF到Specular光泽度</b>是&#x200B;*转换*&#x200B;模板，可用于将AxF材质映射到标准PBR模型。\
然后，可以将它们与默认3D视图着色器一起使用，并与在Designer、[Sampler](https://www.adobe.com/cn/products/substance3d-sampler.html)中制作或从我们的[3D资源](https://substance3d.adobe.com/assets/)库中获取的其他PBR素材组合使用。

<b>AxF到AxF</b>是一个&#x200B;*直通*&#x200B;模板，可让您就地编辑AxF材料，并将这些更改导出为现有AxF文件中的新图层。 要了解更多信息，请参见下面的导出AxF文件。

</td>
<td style="border: 0;" valign="top">

![AxF：Substance图形模板](../../assets/axf-templates.png "AxF：Substance图形模板")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

对于<b>模板</b>列表中添加的所有Substance图形模板，将执行以下附加操作：

对于任何[<b>输入</b>](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)节点，如果&#x200B;*用法*&#x200B;与从AxF文件中提取的纹理的&#x200B;*标识符*&#x200B;匹配，则输入节点将被替换为引用该纹理的[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点；

图形的<b>分辨率</b>属性（即，输出大小）将自动设置为两个的幂，等于或高于&#x200B;*最大*&#x200B;提取纹理的分辨率；

[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点的<b>分辨率</b>属性（即，输出大小）在应用上一个操作后自动设置为与图形匹配；

图形的<b>物理尺寸</b>属性设置为&#x200B;*第一个*&#x200B;提取纹理的物理尺寸；

图形参数的&#x200B;*默认值*&#x200B;设置为与AxF文件中的数据匹配。

从AxF文件中的素材提取的&#x200B;*元数据*&#x200B;将复制到图形的<b>描述</b>属性中。

>[!IMPORTANT]
>
> 图形参数的默认值不应在此初始配置之后进行修改。
> 
> 它们指定了正确解释着色中的值所必需的“纹理”属性。
> 
> 因此，在[3D视图](../../interface/3d-view/3d-view.md)中可视化素材时，更改这些设置将导致渲染不正确。

</td>
<td style="border: 0;" valign="top">

![AxF：图形参数Substance](../../assets/axf_graph-props.png "AxF：图形参数Substance")

</td>
</tr>
</table>

## 导出AxF文件

可从Designer就地编辑现有AxF文件，其资源可使用[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)进行更新。

由于能够将图形输出导出到AxF文件，Designer中的典型AxF工作流程可能如下所示：

1. 导入AxF文件
1. 使用“AxF到AxF”Substance图形模板
1. 使用Substance图中可用的特性和节点编辑提取的纹理
1. 将图形输出导出到同一AxF文件

图形的<b>物理尺寸</b>属性用于设置已编辑AxF文件中更新纹理的<b>物理尺寸</b>属性。

>[!NOTE]
>
> 对文件中资源的更改将添加为&#x200B;*新图层*。 这意味着每次从Designer导出到同一AxF文件都会增加该文件的大小。

![导出AxF](../../assets/exportaxf.gif)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

### “导出”对话框

<b>AxF</b>导出对话框在<b>导出输出</b>对话框中可用作专用选项卡。

在[图形视图](../../interface/the-graph-view/the-graph-view.md)工具栏中，打开![](../../assets/tools.jpg) <b>工具</b>菜单，选择<b>导出输出……</b>选项以显示对话框，然后选择<b>AxF</b>选项卡。

</td>
<td width="100.00%" style="border: 0;" valign="top">

![AxF：“图形视图”工具栏中的“导出”选项](../../assets/axf_graph-export.png "AxF：“图形视图”工具栏中的“导出”选项")

</td>
</tr>
</table>

该对话框包含三个主要部分：

使用<b>文件</b>输入字段可以选择应编辑的目标AxF文件。 加载并检查该文件，如果文件数据有效，则使用它填充下面的“AxF资源”列。

<b>映射输出</b>在输出列中列出图形输出，并将其&#x200B;*用法*&#x200B;与共享相同&#x200B;*标识符*&#x200B;的目标文件中的AxF资源匹配。 如果检测到任何问题，则它们在“备注”栏中显示为警告（黄色）或错误(ref)。

<b>未映射的输出</b>在无法映射的目标文件中列出图形输出和AxF资源。 这些输出被忽略，这些AxF资源保持不变。

>[!NOTE]
>
> 图形输出需要将其的<b>组</b>属性设置为“AxF”，才能在此对话框中列出。

![AxF：导出对话框](../../assets/axf_export.png "AxF：导出对话框")

单击“<b>开始导出</b>”以使用包含映射输出中的更改的新图层编辑目标AxF文件。

结果将以消息形式显示在对话框状态栏中的进度栏旁边。

>[!TIP]
>
> 每次执行导出时，都会在目标文件中创建一个新图层。 因此，请注意进行深思熟虑、有针对性的导出，以管理文件的大小和复杂性。

### 将输出映射到AxF资源

导出到现有AxF文件时，将使用图形输出更新其资源。 Designer将该资源标识符与[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点匹配，这些节点的标识符与<b>Usage</b>相同。

此外，输出的<b>组</b>属性&#x200B;*必须*&#x200B;设置为“AxF”，才能将其列在AxF导出对话框中（请参阅上文）。

![AxF：Substance图表的输出用法](../../assets/axf_output_usage.png "AxF：Substance图表的输出用法")

资源可以是具有特定通道数量的纹理（即位图）或制服（即值）。 图形输出必须与该数目的声道完全匹配。 否则，将在导出期间针对该资源引发错误，并且该资源将保持不变。

根据提供给Output节点的数据类型，通道数会以不同的方式指定：

* <b>位图（纹理）：</b> [组件](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)属性用于指定通道数，其中R是一个通道，RG是两个通道，依此类推。 该属性用于让Designer知道应将彩色位图的RGBA通道的哪个通道编码到资源中。
* <b>值（一致）：</b>矢量值的组件数用于指定通道数，其中[Float](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)是一个通道，[Float2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)是两个通道，依此类推。

>[!IMPORTANT]
>
> 在<b>AxF到AxF</b>Substance图形模板中，<b>Specular瓣</b>贡献的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点默认配置为&#x200B;*单通道*（即，其Components属性设置为“R”）。\
> 如果导入的AxF文件在其SpecularLobe资源中使用了多个通道，请相应地设置输出的<b>组件</b>属性。
> 
> 例如，对于使用两个声道的SpecularLobe资源（“红色”表示Specular粗糙度，“绿色”表示Specular各向异性），将“组件”属性设置为“RG”。

## 在3D视图中查看AxF文件

在[3D视图](../../interface/3d-view/3d-view.md)中渲染AxF SVBRDF材质的方法取决于[导入设置](#import)。

+++转换为PBR

如果要将AxF文件中的SVBRDF材质转换为标准PBR材质，则导入设置可能需要[Substance图形转换模板](#graph-templates)。

在这种情况下，应在3D视图中使用&#x200B;**OpenGL渲染器**，然后选择<code>AxF SVBRF</code> 着色器。\
然后，可以拖放在“导入”对话框中设置的Substance图形，以便将其输出连接到着色器。

![AxF：查看以进行转换](../../assets/axf-view-for-convert.gif "AxF：查看以进行转换")

+++

+++在当前位置编辑

如果您的目标是对现有AxF文件执行&#x200B;*编辑*，请按照以下说明根据选定的渲染器显示其SVBRDF素材：

专用的GLSLFX着色器可用于使用AxF文件中的SVBRDF表示法可视化材质： <b>AxF SVBRDF</b>。

着色器在<b>材质</b>菜单中可用：打开场景材质的子菜单（默认情况下为“默认”），然后选择<b>AxF SVBRDF</b>条目下的任何技术。

使用同一子菜单中的<b>编辑</b>选项在[属性](../../interface/properties/properties.md)停靠区中显示着色器的属性。\
特别是，<b>拼贴</b>属性允许您调整模型上的纹理拼贴，以便您可以按适当的比例可视化素材。

选择着色器后，在图形的空白处单击RMB，然后选择<b>在3D视图中查看输出</b>选项以在[3D视图](../../interface/3d-view/3d-view.md)中可视化其输出。

![AxF： SVBRDF GLSLFX着色器](../../assets/axf_glslfx-svbrdf.png "AxF： SVBRDF GLSLFX着色器"){width="600px"}

此着色器当前是&#x200B;*在创作品*，某些功能仍不受支持。 因此，虽然它可以提供材料特性的一个概览，但不能用于精细调整。

使用同一子菜单中的<b>编辑</b>选项在[属性](../../interface/properties/properties.md)停靠区中显示着色器的属性。\
特别是，<b>拼贴</b>属性允许您调整模型上的纹理拼贴，以便您可以按适当的比例可视化素材。

选择着色器后，在图形的空白处单击RMB，然后选择<b>在3D视图中查看输出</b>选项以在[3D视图](../../interface/3d-view/3d-view.md)中可视化其输出。

![AxF：查看版本](../../assets/axf-view-for-edit.gif "AxF：查看版本")
<i>注意：</i>忽略视频部分从切换到Iray渲染器直到结束，因为16.0.0版中的Iray渲染器和MDL支持已从Designer <i>移除</i>。

+++

### 支持的模型变体

3D视图中使用的着色器支持Specular、菲涅耳和透明皮毛传输模型的以下变体：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">
<b>Specular变体</b>

* 沃德/盖斯勒 — 莫罗德，2010年
* GGX / Walter2007
* GGX / Ross 2005

</td>
<td style="border: 0;" valign="top">
<b>菲涅耳变体</b>

* Schlick 1994
* Schlick 1994 Colored
* 简单菲涅耳

</td>
<td style="border: 0;" valign="top">
<b>透明皮革变速器变体</b>

* 折射Dirac *（仅限OpenGL）*
* 折射Dirac/无实角压缩&#x200B;*（仅限OpenGL）*
* 非折射性迪拉克
* 非折射Dirac / DSPBR 2020x
* GGX

</td>
</tr>
</table>
