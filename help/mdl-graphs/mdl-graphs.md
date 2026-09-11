---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中创建和使用材料定义语言图形执行高级材料工作流程。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL 图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# MDL 图

此页显示Substance 3D Designer中的MDL 图，可让您创作MDL 材质并实时预览其行为。

![孔雀石MDL 材质](../assets/mdl-malachite-example.jpg "孔雀石MDL 材质")

*带有Chrysocolla的Malachite，由[Mark Foreman](https://www.artstation.com/oggyart)MDL 材质**在我们的[旧版Substance share](https://share-legacy.substance3d.com/libraries/4043)**平台*&#x200B;上提供

>[!WARNING]
> 
> Designer 16.0.0版中删除了MDL 图和所有相关功能。
> 
> 在此处了解详情： [MDL 图和Iray生命周期结束](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++目录

* [主要MDL 图概念](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [创建MDL 图](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [MDL库](/help/mdl-graphs/mdl-library/mdl-library.md)
* [在MDL 图中公开参数](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [图形和MDL 材质](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [导出MDL内容](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [MDL 图中的警告](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [MDL学习资源](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## 概述

MDL表示[材料定义语言](http://www.nvidia.com/object/material-definition-language.html)：“[NVIDIA](https://www.nvidia.com/)开发的用于定义基于物理的渲染解决方案的材料的技术。” （来源： [NVIDIA MDL文档](https://raytracing-docs.nvidia.com/mdl/index.html)）

使用此语言，完整的材料定义是可移植的，因此可在应用程序和渲染器间使用以获得一致的输出。 Substance 3D Designer当前是&#x200B;*仅*&#x200B;个应用程序，通过将MDL函数和值类型作为图形公开，为MDL 图提供基于MDL 材质的节点创作。

在创作材料时，您可以使用NVIDIA自己的[Iray](../interface/3d-view/iray/iray.md)渲染器（嵌入在Designer中，可在[3D视图](../interface/3d-view/3d-view.md)面板中使用）以交互方式预览材料&#x200B;*的行为*。

MDL 图与[Substance图形](../compositing-graphs/substance-compositing-graphs.md)互补，因为后者输出&#x200B;*纹理*，MDL 材质可以对它进行&#x200B;*采样*&#x200B;以影响它的行为和外观。

我们建议按&#x200B;*顺序浏览本文档*&#x200B;的各个部分，以便了解指导式学习路径，从MDL 图资源的属性开始，具体内容如下。\
想跳进去吗？ 在“MDL学习资源”部分中开始使用MDL 图！

>[!NOTE]
>
> 您可以在[NVIDIA MDL文档](https://raytracing-docs.nvidia.com/mdl/index.html)中详细了解材料定义语言的技术实现，其中包含MDL规范和[MDL手册](http://mdlhandbook.com/)的链接，所有这些文档均由NVIDIA创作和维护。

![MDL 图属性](../assets/mdl-main.png "MDL 图属性")

*“属性”面板中的属性MDL 图*

## MDL 图属性

### 属性

本节包括有关MDL 材质的信息，以便识别、分类和确定署名。

* <b>标识符</b>：此资源的名称，它在包中其父级下应是唯一的
* <b>显示名称</b>：界面中显示的MDL 材质名称
* <b>图标</b>：在Designer图库中用作此图形缩略图的图像
* <b>隐藏\*</b>：设置为* True*时，该MDL 材质在MDL库中不可见，但仍在内部存在并且可以引用
* <b>在库中显示</b>：设置为&#x200B;*True*&#x200B;时，MDL 图显示在Designer的库中
* <b>说明</b>：MDL 材质的说明，该说明可以显示在引用此图形的实例化的工具提示中
* <b>类别\*</b>：MDL 图所属的类别 — 这目前对图形在Designer的[库](../interface/the-library/the-library.md)中的排序方式没有影响
* <b>在组中\*</b>：MDL 材质所属的库组
* <b>作者\*</b>：MDL 材质的作者
* <b>投稿人\*</b>：MDL 材质的投稿人（作者除外）
* <b>关键字\*</b>：可用于查找图库搜索中MDL 材质的关键字
* <b>版权声明\*</b>：与MDL 材质的创作和使用相关的版权声明

注意：标有星号(\*)的属性是MDL库集成使用的MDL批注，在Designer中*&#x200B;无影响*。

### 图形输入

此部分列出连接到MDL图形的公开参数的交互式参数，并定义其&#x200B;*默认值*。 它们可能随时&#x200B;*被调整*&#x200B;和&#x200B;*重新排序*。

这些输入的接口和行为由它们所连接的公开参数的&#x200B;*值类型*&#x200B;和&#x200B;*范围*&#x200B;定义。 例如：

* 设置为软范围[0.0,4.0]的<b>Float</b>类型的公开值将显示为范围从0.0到4.0的&#x200B;*单个滑块*
* <b>颜色</b>类型的公开值将显示为&#x200B;*颜色构件*，其中包括选取渐变和颜色缩略图

要对图形输入重新排序，请将光标放在参数左侧的&#x200B;*深色手柄*&#x200B;上，单击并&#x200B;*按住* <b>LMB</b>并向上或向下拖动光标。 此自定义顺序用于在以下上下文中显示MDL材料的属性：

* 引用此材料的MDL图表的实例节点
* [3D视图](../interface/3d-view/3d-view.md)中的材质属性
* 第三方MDL集成
