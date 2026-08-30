---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters/exposing-a-parameter.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer合成图中公开参数，以使素材可自定义并可重用。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 公开参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '2267'
ht-degree: 4%

---


# 公开参数

公开参数是功能最强大的工具之一，对于向其他应用程序（如Substance 3D Painter、Substance 3D Sampler以及适用于Maya和3DS Max的Substance集成）打开图表至关重要。

此页面介绍了开始公开的所有必需概念。 建议[先了解图形实例是什么](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)，然后再继续此页面。 另外，您还应该了解[Publish与导出的区别，以及所涉及的文件类型。](../../../getting-started/overview/overview.md)

![简化了公开参数](exposing-a-parameter.resources/parameters-5.png "简化了公开参数")

*\*上方的虚线、透明线条是连接的抽象表示形式\
从公开的参数到图形参数。*

## 了解参数和显示

+++什么是参数？
*参数是具有UI元素的简单值，用于控制图表的行为。* 您可在所有Substance软件中持续使用它们：更改颜色、设置混合模式、选择不透明度值等……如果没有参数，Substance软件将不允许进行任何自定义。

参数可以有多种不同的形式：滑块、拨号、输入框、下拉菜单等。它们表示的值可以有很多种类型：十进制值、整数（整数）值、布尔值(true/false)，甚至文本片段。

+++

+++什么是“曝光”？
***公开是指使参数可在当前图形视图之外使用的过程。***  构建图表时，通常选择节点来更改其属性中的参数；如果公开，则您&#x200B;*启用从外部控制面板访问此参数*。 根据上下文，“外部控制面板”可能具有不同的含义：在Designer中用作图表实例时，它仅充当另一个节点。 在Substance 3D Painter、Substance 3D Sampler或集成中使用时，这些公开的参数将是&#x200B;*您对图表拥有的唯一控件*。

+++

+++为什么说曝光很有用？
***公开参数是使Substance 3D Designer超越简单纹理编辑器的工具，允许您创建可自定义的动态纹理生成工具*** **。** 如果不进行曝光，Substance材质将不会与静态纹理有很大差异：您将无法修改其输出。

+++

+++为什么不随时自动公开每个参数？
<b> [Substance图](../../../compositing-graphs/substance-compositing-graphs.md)可能会变得很复杂，一次可包含数百个参数。 始终向用户显示所有参数是没有意义的，特别是当您要用简单的目标生成不需要很多参数的图表时。</b> 在公开参数时，您作为UI或UX设计者工作：您会考虑哪些控件是合理的，需要哪些值，以及如何使其易于为自己、在线其他用户或您的同事使用。

+++

+++我是否需要了解数学才能进行曝光？ 我是否应该了解Substance函数图表？
***不需要数学知识来很好地使用公开参数，也不需要使用函数。***  作为初始用户，您几乎可以完全避免在[函数图表](../../../function-graphs/function-graphs.md)中进行数学运算。 唯一强烈建议的是[对不同数据类型（如整数、浮点和布尔值）的适当基础知识。](../../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)

+++

## 如何公开

目前，公开参数的主要方法有两种。 一种方法更适合于快速曝光单个参数，第二种方法更适合于在一次扫描中曝光多个参数。

![单公开方法演练](exposing-a-parameter.resources/single-expose2.gif "单公开方法演练"){width="512px"}

### 单曝光法

1. 在“[属性](../../../interface/properties/properties.md)”面板的“特定参数”选项卡下找到要公开的参数
1. 单击![](exposing-a-parameter.resources/image2020-9-17-15-35-59.png)下拉选项按钮
1. 从下拉列表第一个选项中选择![](exposing-a-parameter.resources/image2020-9-17-15-37-7.png) <b>公开为新图形输入</b>。
1. 出现<b>公开参数</b>对话框，根据需要设置任何参数属性。

   建议至少更改<b>标识符</b>和<b>标签</b>
1. 按<b>确定</b>以确认
1. 参数名称变为&#x200B;*蓝色*，变为![](exposing-a-parameter.resources/image2020-9-17-15-35-46.png)\
   在下拉选项旁显示<b>编辑参数函数</b>按钮，以确认参数已公开

>[!NOTE]
>
> 大多数数字字段支持&#x200B;*基本数学公式*&#x200B;作为输入 — 例如，`17+3.5`、`7/3`、`(4+2)*3`。 按&#x200B;*Enter*&#x200B;验证公式，结果将输入到字段中。 如果公式无效，则字段将恢复为以前的值。\
> 应用程序其他部分（如[属性](../../../interface/properties/properties.md)程序坞）中的某些数字字段也支持此功能。

![批量公开方法演练](exposing-a-parameter.resources/batch-expose-2.gif "批量公开方法演练"){width="512px"}

### 批量公开方法

公开一个参数时，此方法将比上一个方法慢一些。 公开多个参数时，速度要快得多。

1. 查找<b>特定参数</b>选项卡右上角的![](exposing-a-parameter.resources/image2020-9-17-15-39-7.png) <b>多公开</b>按钮，而不是查找单个参数
1. 从下拉菜单中选择<b>批量公开参数……</b>
1. 此时会显示<b>批量公开</b>对话框，允许您自定义节点的所有特定参数<b>的公开</b>
1. 使用<b>全部</b>、<b>无</b>或特定的复选框来决定公开哪些参数
1. 单击列表中<b>图形输入标识符</b>列下的参数名称以更改其名称。
1. 单击列表中<b>图形输入组</b>列下的<b>组名称</b>以添加一个特定参数的（子）组
1. 使用底部的<b>图形输入标识符</b>和<b>图形输入组</b>键入框，将前缀、后缀和输入组一次性添加到所有公开参数。 所有这些值都会在每参数设置的基础上应用。
1. 单击<b>确定</b>以确认并公开所有选定的参数。 参数名称现在显示&#x200B;*蓝色*&#x200B;以确认参数已公开，同时显示![](exposing-a-parameter.resources/image2020-9-17-15-35-46.png) <b>编辑函数</b>按钮。

## 限制

一些与公开参数有关的限制，如下表所示。

| 参数类型 | 原因 |
| --- | --- |
| [渐变曲线](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)，[曲线编辑器](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)，[字体](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)，[色阶直方图](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) | 需要小部件，这些小部件不可用于用户创建的参数。 |

另一个重要限制与[静态参数](../../../glossary/glossary.md)有关。 这些无法在[发布的Substance 3D资源(SBSAR)](../../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中更改。

静态参数 — 与动态参数相对 — *在图形*&#x200B;完成&#x200B;*后无法动态编辑* — 即，为了快速高效地运行其算法而处理静态参数。 每次图形&#x200B;*已编辑*&#x200B;或&#x200B;*已发布*&#x200B;时，Designer中都会发生烹饪。

因此，静态参数在Designer中可见且可编辑，但在发布的Substance 3D资源中&#x200B;*隐藏*。 在发布到Substance 3D资源之前，可使用“预览”模式查看这些有效的限制：请参阅下面的“预览参数”。

作为解决方法，您可以使用[Switch](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)或[Multi Switch](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)节点和多个逻辑集在这些参数的不同值/状态之间切换。

| 节点 | 参数 |
| --- | --- |
| 所有节点 | 拼贴模式像素比率 |
| [统一颜色](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | 颜色模式 |
| [像素处理器](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | 颜色模式 |
| [混合](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | 混合模式Alpha混合裁切区域 |
| [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | 混合模式 |
| [象限](../../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | 图案输入图像Alpha输入图像滤镜 |

## 修改公开参数

一旦暴露出来，就不能再像以前一样访问参数。 更改其值、重命名、在用户界面中排列甚至删除参数都发生在图形属性级别。 本节详细介绍如何执行该操作。

要更改公开参数的选项，请执行以下任一操作：

1. 单击已公开参数旁边的下拉选项按钮![](exposing-a-parameter.resources/image2020-9-17-15-35-59.png)
1. 选择“![](exposing-a-parameter.resources/image2020-9-17-15-37-7.png)<b>”“编辑公开的图形输入”</b>。 该操作会将您直接带到图表属性中的相关条目
1. 双击图形的空白区域以转到图形属性，然后在<b>输入参数</b>列表中查找该参数
1. 单击<b>资源管理器</b>中的图形，然后在<b>输入参数</b>列表中查找该参数

![输入参数](exposing-a-parameter.resources/input-parameters-2.png "输入参数"){width="512px"}

### 输入参数

所有公开的参数均列在“输入参数”选项卡下。 以下属性可用于大多数常见情况，例如具有默认编辑器类型的“浮点”和“整数”。

1. <b>标识符</b>：此参数的唯一标识符。 不能包含空格或特殊字符。
1. <b>标签</b>：仅限UI标签。 如果未定义标签，则在UI中显示标识符。 可以包含空格和特殊字符
1. <b>组</b>：将参数分组到可折叠部分，以使长长的参数列表保持干净并可管理。 如果参数共享&#x200B;*完全相同的*&#x200B;组名称，则这些参数将被组合在一起。 使用`/`字符创建&#x200B;*子组* — 例如`My Group/My Sub-group`
1. <b>描述</b>：描述的Textfield，用作工具提示。
1. <b>类型/编辑器</b>：设置数据类型和UI编辑器类型。 某些编辑器仅适用于某些数据类型（如下拉列表仅适用于Integer）。 *更改编辑器在很多情况下会擦除默认值，请小心。*
1. <b>默认值</b>：参数的起始默认值。 这也是在预览节点时在图形中输入的值。 尝试在此处使用简单、可用的值，避免极端情况。
1. <b>最小值</b>：用户界面的最小值
1. <b>最大值</b>：用户界面的最大值
1. <b>固定</b>：设置“最小值”和“最大值”是软限制还是硬限制（允许用户超过限制）。
1. <b>步骤</b>:Set值的精度或粒度。
1. <b>用户数据</b>：自定义用户数据，可用于任何用途。
1. <b>在以下情况下可见</b>：特殊表达式，供系统用于根据外部条件显示或隐藏参数。 请参阅[显示条件：控制输入、输出和参数的可见性](../../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md)

![整数参数的下拉列表编辑器](exposing-a-parameter.resources/dropdown.gif "整数参数的下拉列表编辑器"){width="512px"}

#### 下拉列表

一个特殊的情况是整数类型的<b>下拉列表</b>。 没有“默认”、“最小”或“最大”，只有一个“值”设置允许您定义项目列表。

* 每个项目对应于下拉列表中的项目。
* 物料的第一个值是图形使用的实际内部整数。 例如，确保为[Multi Switch](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)正确设置了这些参数（从1开始，而不是0）。
* 第二个值是向用户显示的UI标签。
* 第三个复选框允许您将一个项目标记为默认选定项目。
* X删除项目，+添加项目

![对输入参数重新排序](exposing-a-parameter.resources/reorder-2.gif "对输入参数重新排序"){width="512px"}

#### 重新排序

通过拖放列表中输入参数名称左侧的深色条带化手柄，可以轻松对参数重新排序。 请记住，分组参数会影响顺序。

![预览输入参数](exposing-a-parameter.resources/parameter-preview-2.gif "预览输入参数"){width="512px"}

### 预览参数

由于设置参数可能很难看到最终结果，因此可以启用<b>预览模式</b>，以检查参数UI的外观和行为方式。 单击“输入参数”转出过程顶部中间的“<b>预览</b>”选项卡。

通常，在<b>预览模式</b>中所做的任何更改都&#x200B;*已丢弃*。 但是，您可以使用眼睛图标旁边的<b>应用按钮</b>将<b>预览模式</b>的当前值设置为&#x200B;*新的默认值*。

[“预览模式”还允许您创建嵌入预设。](../../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

>[!IMPORTANT]
>
> 使用[上下文编辑](../../../interface/preferences-window/preferences-window.md)时禁用预览模式。

>[!WARNING]
>
> 预览模式旨在尽可能准确地呈现[已发布的Substance 3D资源(SBSAR)](../../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)的体验。 因此，本页中列出的限制将在此模式下应用，如&#x200B;*静态参数不在列表中*。

![复制和粘贴输入参数](exposing-a-parameter.resources/copy-paste-params-2.gif "复制和粘贴输入参数"){width="512px"}

### 复制粘贴参数

可以在图形之间复制粘贴参数。

可以使用复制按钮![](exposing-a-parameter.resources/image2019-9-19-11-3-49.png)复制单个参数。 可以通过参数菜单![](exposing-a-parameter.resources/image2020-9-17-15-39-7.png)复制多个参数。 选择“复制输入”以复制所有输入。

在“参数”菜单![](exposing-a-parameter.resources/image2020-9-17-15-39-7.png)中选择“粘贴输入”![](exposing-a-parameter.resources/image2020-9-17-16-43-15.png)以粘贴一个或多个参数。

如果要传输值，而不是实际公开的参数本身，请[阅读参数预设。](../../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

## 删除和清除暴露的参数

由于参数的性质（您可以让输入参数控制多个节点，或者输入参数可以在不控制节点的情况下存在），因此缺少参数或未使用的参数可能会出现问题。 下面介绍了常见问题及其解决方案。

![节点参数出错](exposing-a-parameter.resources/parameter-error.gif "节点参数出错"){width="512px"}

### 跟踪节点上的损坏参数

您可以通过“节点查找器工具”![](exposing-a-parameter.resources/image2019-9-19-14-15-53.png)（位于“图形视图”顶栏中）跟踪哪个节点使用了哪个参数。 单击它可让您使用特定参数查找节点。

如果节点遇到实际问题，则会在节点的左上角显示警告标记![](exposing-a-parameter.resources/image2019-9-19-14-23-54.png)。 将鼠标悬停在徽章上会显示工具提示，其中包含更多信息。

要重置并移除问题，对于要修复或重置的参数，单击“编辑函数”按钮旁边的下拉按钮![](exposing-a-parameter.resources/image2020-9-17-15-35-59.png)并选择![](exposing-a-parameter.resources/image2020-9-17-16-56-18.png) <b>重置。 </b>这将使参数返回到其以前的非公开状态，蓝色名称将再次变为灰色以反映此情况。

![清除未使用的输入参数](exposing-a-parameter.resources/clean-inputs-2.gif "清除未使用的输入参数"){width="512px"}

### 清除未使用的输入参数

如果您丢失了输入参数的跟踪信息并且不再知道使用了哪些参数，可以使用小工具清理它们。 单击“输入参数”菜单按钮![](exposing-a-parameter.resources/image2020-9-17-15-39-7.png)，然后选择<b>清理输入。</b>

此时会出现一个新对话框，其中列出了所有未使用的参数。 选中或取消选中要删除或保留的任何参数，然后单击“确定”。 如果未出现对话框，则当前没有要清理的未使用参数。

![正在删除参数](exposing-a-parameter.resources/delete-param-2.gif "正在删除参数"){width="512px"}

### 删除参数

要实际移除正在使用的参数，需要两个不同的步骤。

1. 在具有已公开参数的节点上，单击“函数公开”按钮右侧的绿色下拉箭头：![](exposing-a-parameter.resources/image2019-9-19-14-55-55.png)。 然后选择“重置为默认值”。 这样将删除在该节点上对该参数的使用。 对使用相同参数的任何其他节点重复此步骤。 “重置为默认值”也会将参数小部件的范围重置为其&#x200B;*软范围*。
1. 在图形的“输入参数”列表中，单击参数条目右侧的X。 这会彻底删除参数。 如果有任何节点尝试使用此参数，则会出现警告徽章（请参阅上文）。
