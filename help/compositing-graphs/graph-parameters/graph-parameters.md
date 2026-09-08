---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/graph-parameters.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中创建和管理图形参数以控制材料属性和行为。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Graph parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图形参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 1%

---


# 图形参数

此页描述<b>图形</b>的标准参数。

一个图形有多个可以修改的参数。 您可以通过单击图形中的&#x200B;*空白区域*&#x200B;或在<b>图形</b>面板中选择&#x200B;*资源管理器项*&#x200B;来查找它们。 然后，参数将显示在“参数”视图中。

<a name="base-parameters"></a>

## 基本参数

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

此部分包含对&#x200B;*它包含的所有节点*&#x200B;有影响的参数。

实际上，此图形中基参数设置为“相对于父代”的[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)的每个节点都将从&#x200B;*图形*&#x200B;基参数中获取其值。

反过来，图形的基本参数值将取决于在其中使用图形的上下文。

</td>
<td style="border: 0;" valign="top">

![基本参数](../../assets/doc-graph-props-base-params.png "基本参数"){width="512px" zoomable="yes"}

</td>
</tr>
</table>

例如，当该图形在另一个图形中用作实例化时，其基本参数默认使用“相对于输入”继承方法。 这意味着他们将从与其主输入连接的节点获取其值。 （除非它们[被覆盖](#input-parameters)）

在大多数情况下，继承在定义这些值以及这些值在整个图形中的变化方式方面起着重要作用。 因此，强烈建议在使用这些参数之前充分了解图形](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)中的[继承。

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>输出大小</b> | 此参数允许您在图形中选择图像的&#x200B;*基分辨率*。  使用 <div><img data-preserve-html="true" height="22" src="../../assets/props-output-size-lock.jpg"/></div> 锁定按钮，使高度值和宽度值匹配，并在调整大小时保持图像正方形。<br><br>*默认： (0,0) -相对于父代* [了解详情](../../compositing-graphs/output-size/output-size.md) |
| <b>输出格式</b> | 允许从以下选项中选择图形中的&#x200B;*基本位深度*：<ul data-preserve-html="true"><li data-preserve-html="true">8位</li><li data-preserve-html="true">16位</li><li data-preserve-html="true">HDR Low Precision 16F（16位浮点）</li><li data-preserve-html="true">HDR High Precision 32F（32位浮点）</li></ul>*默认值：每通道8位 — 相对于主页* |
| <b>像素大小</b> | 定义像素大小。 我们建议将&#x200B;**宽度**&#x200B;和&#x200B;**Height**&#x200B;值都设置为&#x200B;**1**。*默认值： (1,1) — 相对于主页* |
| <b>拼贴模式</b> | 通过以下选项在图形中定义基&#x200B;*拼贴模式*：<ul data-preserve-html="true"> <li data-preserve-html="true">无平铺</li> <li data-preserve-html="true">水平平铺</li> <li data-preserve-html="true">垂直平铺</li> <li data-preserve-html="true">H+V拼贴（即水平和垂直）</li> </ul>*默认： H和V拼贴 — 相对于主页* |
| <b>随机植入</b> | 为图形定义基&#x200B;*随机植入*。  使用 <div><img data-preserve-html="true" height="22" src="../../assets/prop-randomise.jpg"/></div> 按钮以向随机种子分配新的随机值。<br><br>*默认值： 0 — 相对于主页* |

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<a name="attributes"></a>

## 属性

<b>属性</b>部分包含图形的&#x200B;*元数据*，该部分提供了有关&#x200B;*标识*、*分类*&#x200B;和&#x200B;*应用*&#x200B;图形的信息，如作者所设计。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![图形属性](../../assets/doc-graph-props-attributes.png "图形属性"){zoomable="yes"}

</td>
</tr>
</table>

+++属性列表

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **标识符** | 这是图形的名称，必须为&#x200B;*唯一* — 不能在同一包中有两个或多个图形具有相同的<b>标识符</b>。 它在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)面板中用作图形的&#x200B;*名称*。<br><br>*注意：*&#x200B;标识符&#x200B;*不能为空字符串*。 空字符串会自动替换为`_`或`Substance_graph`。 对于此值，您只能&#x200B;*使用*&#x200B;以下字符： *`A-Z, 1-9, @$%[{]}_-`.* 未授权的字符会自动替换为`_`。<br><br>*默认： New\_Graph，或在创建图形时由用户设置* |
| **标签** | 使用<b>标签</b>而非<b>标识符</b>来显示图形的&#x200B;*名称*，以便在&#x200B;*面向用户*&#x200B;的情况下提高可读性 — 例如，[库](../../interface/the-library/the-library.md)项或[实例节点](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)标签。  标签可以是&#x200B;*不唯一*，并且可以包含特殊字符。<br><br>*提示：*&#x200B;如果您重命名图形 — 例如，在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中 — 您可能还希望更改其标签！<br><br>*默认：空* |
| **类型** | <b>类型</b>用于定义[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)的预期用途。 它主要用于[“发送”互操作性功能](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)。 |
| **材质模型** | 设置图形的材质模型可确保3D视图中使用适当的着色器（如果着色器&#x200B;*与模型*&#x200B;匹配）。<br>例如， 在3D视图中查看具有`OpenPBR v1.1`素材模式的图表将为目标素材选择中的`OpenPBR Surface`着色器。<br><br>如果未找到匹配的着色器，或者图表的模型设置为`Undefined`，则在3D视图中用于目标素材的着色器为&#x200B;*未更改*。 |
| **物理尺寸** | 此值指定&#x200B;*物理世界*&#x200B;中纹理的尺寸，采用X（长度）、Y（宽度）和Z(Height)。 因此，它与图形中生成的材料有内在联系。 例如，可以使用物理尺寸在<b>2D视图</b>和<b>3D视图</b>中以正确的比例显示纹理。<br><br>*提示：*&#x200B;可以使用$physicalsize [内置变量](../../function-graphs/variables/system-variables/system-variables.md)，将Substance图形的物理尺寸检索为应用于该图形中任何Substance的纹理函数图形中的Float3值。<br><br>*注意：*&#x200B;在&#x200B;**3D视图中，** Z **值当前为&#x200B;*未考虑在内*视图**。 因此，应使用&#x200B;**输出** Height设置为&#x200B;**高阶**&#x200B;用法，或直接在&#x200B;**材质属性**&#x200B;中设置材质的&#x200B;**节点比例**&#x200B;值。<br><br>*默认值： (0,0，0)* |
| **图标** | 此区域允许您定义&#x200B;*图标*，<b>库</b>将使用此图标将此图表的条目显示为<b>SBS</b>和<b>SBSAR</b>。 此图标还用于其他情况，如[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)的<b>托架</b>。 该区域提供以下选项：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>浏览</b>：允许您浏览系统文件以查找<i>应用作图标的现有映像</i></li> <li data-preserve-html="true"><b>生成</b>：这将使用<b>PBR 渲染</b>节点的<i>内置预设</i>生成图标</li> <li data-preserve-html="true"><b>粘贴</b>：允许您将当前位于<i>剪贴板</i>中的图像数据粘贴为图标</li> <li data-preserve-html="true"><b>移除</b>：此选项<i>移除</i>现有图标，并将图标槽<i>留空</i></li> </ul>*注意：* **生成**&#x200B;选项使用&#x200B;**物理尺寸**&#x200B;来确定&#x200B;**PBR 渲染**&#x200B;的&#x200B;**Height比例**&#x200B;的位移效果。 如果图形中存在设置为&#x200B;**物理大小**&#x200B;用法的&#x200B;**输出**&#x200B;节点，则使用此输出。 如果不存在此类输出，则使用图形的&#x200B;**属性**&#x200B;中的值&#x200B;*代替*。 如果属性的值为(0,0，0)，则使用0.1的&#x200B;*预设值*。<br><br>*注意：*&#x200B;未定义&#x200B;*图标*&#x200B;时，将改用图形的&#x200B;*第一个图像输出*。<br><br>*默认：空* |
| **包** | 此图形所属的&#x200B;**包**&#x200B;的&#x200B;*绝对*&#x200B;文件名。使用&#x200B;**文件夹**&#x200B;按钮，可以在此位置打开新系统&#x200B;*文件浏览器窗口*。*默认：包文件名/如果从未保存包，则为空* |
| **在SBSAR中公开** | 这控制是否可以在从图形的&#x200B;**包**&#x200B;发布的&#x200B;**SBSAR**&#x200B;文件中&#x200B;*查看图形及其输出*。如果包中的某些图形仅用作包的主图形的&#x200B;*子图*，并且&#x200B;*不应显示在&#x200B;**SBSAR**中*，则此功能非常有用。*默认：是* |
| **在库中显示** | 控制当包存储在&#x200B;**库**&#x200B;的&#x200B;*监视*&#x200B;位置时，在&#x200B;**库**&#x200B;中图形是否应为&#x200B;*可见*。*默认值：在项目设置的“库”选项卡中设置* |
| **描述** | 这是图形的&#x200B;*描述文本*。在&#x200B;**库**&#x200B;中的图形条目&#x200B;*工具提示*、此图形的任何&#x200B;**实例**&#x200B;节点以及现有&#x200B;**Substance集成**&#x200B;的软件中可以看到此实例。*默认：空* |
| **类别** | 您可以在此字段中为&#x200B;**库**&#x200B;中的此图形项设置&#x200B;*类别*。*默认值：空* |
| **作者** | 您可以使用此字段来放置作者的&#x200B;*姓名*。*默认值：空* |
| **作者URL** | 此字段允许您输入&#x200B;*URL* — 例如，作者的网站。*默认值：空* |
| **标签** | 您可以使用此字段添加您自己的&#x200B;*标记*，以提高图形的&#x200B;*可搜索性*&#x200B;和&#x200B;*可发现性*。*默认：空* |
| **组** | 启用“节点”菜单中的物料分组。 共享公共“组”值的资源（如图形或位图）将分组到以组命名的部分中。 *默认值：空* |
| **用户数据** | 您可以使用此字段添加自己的其他数据。 这对于第三方软件中的自定义集成非常有用。 Substance 3D Painter和Sampler使用此userdata设置某些特定行为。*默认：空* |
| **模板数据** | 将Substance图形用作模板时，此属性设置[模板的类别和副标题](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)。 它们由此分隔： &lt;category>；&lt;subtitle> <br><br>*默认值：空* |

+++
<a name="input-parameters"></a>

## 输入参数

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

特定于图形的所有参数（包括[公开的参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)）均[受管理](../../compositing-graphs/manage-parameters/manage-parameters.md)，可在此处编辑和预览。

也可以为部分或所有参数创建[参数预设](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)。

</td>
<td style="border: 0;" valign="top">

![输入参数](../../assets/doc-graph-props-input-parameters.png "输入参数"){zoomable="yes"}

</td>
</tr>
</table>

+++覆盖基本参数
将另一个图形中的某个图形用作[实例节点](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)时，可以控制该新实例节点上任何基本参数的默认值。

打开“输入参数”部分顶部的汉堡包菜单，然后转到“覆盖基本参数”子菜单以选择要为其设置任意默认值的基本参数。

选定参数的编辑器将显示在图表输入参数列表的顶部。 然后，您可以根据需要调整它们的值和[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。

+++

>[!IMPORTANT]
>
> 使用[上下文编辑](../../interface/preferences-window/preferences-window.md)时，<b>预览</b>和<b>预设</b>选项卡处于禁用状态。

<a name="inputs"></a>

## 输入

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

在此部分中，将列出图形的所有[输入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)节点。

可通过在每个项目最左侧的手柄上使用拖放操作来重新排列顺序。

</td>
<td style="border: 0;" valign="top">

![输入](../../assets/doc-graph-props-inputs.png "输入"){zoomable="yes"}

</td>
</tr>
</table>

<a name="outputs"></a>

## 输出

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

在此部分中，图形的所有[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。

可通过在每个项目最左侧的手柄上使用拖放操作来重新排列顺序。

</td>
<td style="border: 0;" valign="top">

![输出](../../assets/doc-graph-props-outputs.png "输出"){zoomable="yes"}

</td>
</tr>
</table>
