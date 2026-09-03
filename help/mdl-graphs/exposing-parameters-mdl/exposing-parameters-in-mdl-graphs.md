---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exposing-parameters-in-mdl-graphs.html"
breadcrumb-title: ''
description: 了解如何在MDL图表中公开参数，以使材质可在Substance 3D Designer中自定义和重复使用。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exposing parameters in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在MDL图表中公开参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# 在MDL图表中公开参数

此页面说明了在MDL图形中公开参数的过程，以便这些参数可以连接到图形中&#x200B;*其他节点*&#x200B;或&#x200B;*外部源*&#x200B;提供的值和纹理。

![节点输入的公开状态](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-01.png "节点输入的公开状态")

*节点输入的公开状态*

## 公开节点输入

在大多数情况下，可以公开节点属性的&#x200B;*输入连接器*，以便其&#x200B;*值由图形中的其他节点*&#x200B;设置。 这是MDL图表中任何工作流的&#x200B;*关键*&#x200B;部分，应充分理解。

在<b>图形视图</b>中选择某个节点后，其属性将显示在<b>属性</b>面板中。 大多数属性的标签右侧都列出了一组按钮：

* **![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-02.png)将值复制到新节点并将其链接到此参数**：为此属性创建&#x200B;*输入连接器*&#x200B;并将其连接到输出此属性的当前值的&#x200B;*新节点*
* **![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-03.png)为此参数创建输入插针**：为此属性创建&#x200B;*输入连接器*
* **![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-04.png)将此参数重置为默认值**：当没有值连接到此属性的输入连接器时，将其值重置为默认值

![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-05.gif)

*操作节点输入*

单击前两个按钮的任意一个会导致向节点添加&#x200B;*类型的输入连接器*。 节点的属性对此连接器的&#x200B;*连接状态*&#x200B;做出反应：

* **未连接**：参数在&#x200B;**属性**&#x200B;面板中仍可调整，并且此面板中的值输入为&#x200B;*已应用*
* **已连接**：参数在&#x200B;**属性**&#x200B;面板中不再可调整，此面板中的输入值已被&#x200B;*输入连接器*&#x200B;接收的值&#x200B;*替换*，属性无法重置为其默认值

通过再次单击&#x200B;**创建此参数的输入管脚**&#x200B;按钮，可以&#x200B;*删除*&#x200B;输入连接器。 此时，属性值将返回到&#x200B;**属性**&#x200B;面板中设置的值。

![公开节点参数](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-06.png "公开节点参数")

*公开的节点参数*

## 公开图形输入

在MDL图形中，通过公开输出值的节点来将参数公开到图形级别，即显示为MDL材料输入参数。

可公开的节点的上下文菜单中包含<b>公开</b>选项。 在大多数情况下，这些是生成值或数据（如Float、颜色或纹理坐标）的节点。

节点上下文菜单中的![“公开”选项](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-07.png "&amp;quot；公开&amp;quot；选项")

*节点上下文菜单中的“公开”选项*

公开参数直接在&#x200B;*公开节点*&#x200B;中配置，而不是在图形的属性中配置。 公开参数的属性如下：

* <b>标识符</b>：此输入参数在当前图形中的唯一名称
* <b>默认值</b>：此参数的默认值。 它还可以用作输入参数在Designer中的&#x200B;*预览*。 <b>显示名称</b>、<b>在组中</b>和<b>范围</b>属性用于尽可能准确的预览
* <b>范围</b>：
  * *可变范围*：设置用于显示此参数的构件的默认范围 — 例如，滑块。 此属性仅供接口使用，可以手动输入软范围以外的值
  * *硬范围*：设置此参数的可接受值的范围。 低于此范围的值会被限制为最小值，而高于此范围的值会被限制为最大值。 参数的默认值和可变范围值是&#x200B;*自动调整的*，以适合此范围。
* <b>描述</b>：参数的描述
* <b>在组</b>中：此输入参数所属的参数组。 如果不为空，则该参数将显示在Designer中，作为以该组命名的可折叠部分的一部分
* <b>显示名称</b>：界面中显示的参数名称
* <b>隐藏</b>：设置为True时，参数在图形输入和MDL 材质属性中不可见
* <b>灰度系数类型</b>：对连接到此参数的纹理中的值采样时应使用的灰度系数
* <b>默认情况下可见</b>：在某些参数可能隐藏的情况下，在MDL集成中设置此参数的可见性
* <b>类型修饰符</b>：设置值是统一还是变化。 设置为auto时，参数从其输入继承此属性（例如，对于Float值：连接到Float时一致，连接到纹理时变化）
* <b>Sampler用法</b>：参数用法的标识符，用于在多个输出同时连接到MDL素材时&#x200B;*连接适当的纹理*。 例如，将[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)连接到3D视图中的MDL材料时，纹理会通过匹配其使用标识符连接到正确的输入。

>[!WARNING]
>
> 当在&#x200B;*节点*&#x200B;级别设置图形输入时，将在[图形属性](../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)的&#x200B;**图形输入**&#x200B;部分中的&#x200B;*图形*&#x200B;级别管理其排序。

![将节点公开到图形输入中](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-08.gif "将节点公开到图形输入中")

*将节点公开到图形输入中*
