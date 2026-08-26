---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中创建和使用材质定义语言图表以用于高级材质工作流。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL图表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# MDL图表

此页面在Substance 3D Designer中显示MDL图表，通过这些图表，您可以创作MDL材质并实时预览其行为。

![孔雀石MDL材料](../assets/mdl-malachite-example.jpg "孔雀石MDL材料")

*带有Chrysocolla的Malachite，由[Mark Foreman](https://www.artstation.com/oggyart)**提供的MDL材料，可在我们的[旧版Substance share](https://share-legacy.substance3d.com/libraries/4043)**&#x200B;平台*&#x200B;上使用

>[!WARNING]
> 
> 16.0.0版中已从Designer中删除MDL图表和所有相关功能。
> 
> 在此处了解详情： [MDL图表和Iray生命周期结束](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++目录

* [主要MDL图形概念](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [创建MDL图形](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [MDL库](/help/mdl-graphs/mdl-library/mdl-library.md)
* [在MDL图表中公开参数](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [Substance图形和MDL材料](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [导出MDL内容](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [MDL图表中的警告](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [MDL学习资源](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## 概述

MDL表示[材质定义语言](http://www.nvidia.com/object/material-definition-language.html)：“由[NVIDIA](https://www.nvidia.com/)开发的技术，用于定义基于物理的材质以用于基于物理的渲染解决方案。” （来源： [NVIDIA MDL文档](https://raytracing-docs.nvidia.com/mdl/index.html)）

使用此语言，完整的素材定义是可移植的，因此可在应用程序和渲染器间使用以实现一致的输出。 Substance 3D Designer当前是&#x200B;*仅*&#x200B;个应用程序，通过将MDL函数和值类型公开为MDL图表中的节点来提供MDL素材的基于图表的节点创作。

在创作素材时，您可以使用NVIDIA自己的[Iray](../interface/3d-view/iray/iray.md)渲染器（嵌入在Designer中，可在[3D视图](../interface/3d-view/3d-view.md)面板中找到）以交互方式预览素材&#x200B;*的行为*。

MDL图形与[Substance图形](../compositing-graphs/substance-compositing-graphs.md)互补，后者输出&#x200B;*纹理*，其可被MDL素材&#x200B;*采样*&#x200B;以影响其行为和外观。

我们建议按照&#x200B;*的顺序*&#x200B;浏览此文档的各个部分，以获得引导式学习路径，首先从下面的MDL图形资源的属性开始。\
想跳进去吗？ 开始使用MDL学习资源部分中的MDL图表！

>[!NOTE]
>
> 您可以在[NVIDIA MDL文档](https://raytracing-docs.nvidia.com/mdl/index.html)中详细了解材质定义语言的技术实现，该文档包括指向MDL规范和[MDL手册](http://mdlhandbook.com/)的链接，均由NVIDIA编写和维护。

![MDL图形属性](../assets/mdl-main.png "MDL图形属性")

*“属性”面板中的MDL图形属性*

## MDL图形属性

### 属性

本节包括有关MDL材料的信息，用于标识、分类和建立署名。

* <b>标识符</b>：此资源的名称，它在包中其父级下应是唯一的
* <b>显示名称</b>：界面中显示的MDL材质名称
* <b>图标</b>：Designer库中用作此图形缩略图的图像
* <b>隐藏\*</b>：设置为* True*时，MDL素材在MDL库中不可见，但仍存在于内部且可引用
* <b>在库中显示</b>：设置为&#x200B;*True*&#x200B;时，MDL图表显示在Designer的库中
* <b>描述</b>：MDL材料的描述，该描述可以显示在引用此图表的实例节点的工具提示中
* <b>类别\*</b>： MDL图表所属的类别 — 这目前不影响图表在Designer [库](../interface/the-library/the-library.md)中的排序方式
* <b>在组中\*</b>：MDL素材所属的库组
* <b>作者\*</b>：MDL素材的作者
* <b>参与者\*</b>：除作者之外的MDL素材参与者
* <b>关键字\*</b>：可用于查找库搜索中的MDL素材的关键字
* <b>版权声明\*</b>：与MDL材料的创作和使用相关的版权声明

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
