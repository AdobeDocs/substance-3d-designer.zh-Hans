---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: 了解Substance合成图形和MDL 材质如何在Substance 3D Designer中协同工作以创建材料。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图形和MDL 材质
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---


# 图形和MDL 材质

本页介绍了[图形](../../compositing-graphs/substance-compositing-graphs.md)和MDL 图之间的协同作用，以及如何将Substance图形[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)中的纹理连接到MDL 图输入。

## 概述

图形的输出可以通过两种方式&#x200B;*传递给MDL 材质的公开参数*，如本页所述。

如果当前在3D视图中应用的MDL 材质具有类型为&#x200B;*[变化](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)*&#x200B;的公开参数，则可以使用[公开参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)属性中的<b>类型修饰符</b>选项设置此类型，这些属性可以连接到&#x200B;*纹理*：

* <b>Color</b>参数可以连接到RGBA纹理
* 灰度纹理的<b>Float</b>参数

在这些情况下，原始均匀值被提供改变值的纹理采样器替换。 这些取样器在公开参数中定义了<b>用法</b>属性，使用此用法，Designer可以通过&#x200B;*匹配的用法*&#x200B;将Substance图形输出的纹理连接到MDL 材质中的适当参数。

## 3D 视图中的Substance图形

使用图形的<b>在3D 视图中查看输出</b>选项，或将Substance图形从<b>资源管理器</b>面板拖动到<b>3D视图</b>时，输出将连接到3D视图中当前显示的MDL 材质中&#x200B;*匹配的使用情况*&#x200B;的公开参数。

通过按下图形上的RMB并拖动到3D视图中，可以将来自Substance图形的个别纹理连接到支持纹理采样的任何MDL 材质参数，而不管该标识符如何。 此时会显示可用采样器用法的列表，您可以为所选纹理选择目标用法。

![公开的MDL 图输入](../../assets/mdl-graph-inputs-samplers.png "公开的MDL 图输入")

*图形输出的纹理已连接到3D 视图中的MDL 图公开参数*

## MDL 图中的Substance图形

通过将图形实例从<b>资源管理器</b>面板拖放到MDL 图中，可以直接将MDL 图置入。 MDL 图中可以使用<b>Substance 3D文件</b> (SBS)和<b>Substance 3D资源文件</b> (SBSAR)中的Substance图形。

+++从Substance 3D文件(SBS)Substance图形
![从MDL 图中的SBS文件Substance图形](../../assets/mdl-sbs-instance-hl.png "从MDL 图中的SBS文件Substance图形")



MDL 图&#x200B;*中[Substance 3D文件](../../getting-started/overview/overview.md) (SBS)的*[&#x200B; Substance图形](../../compositing-graphs/substance-compositing-graphs.md)实例

+++

+++从Substance 3D资源(SBSAR)Substance图形
![从MDL 图中的Sbsar 文件Substance图形](../../assets/mdl-sbsar-instance-hl.png "从MDL 图中的Sbsar 文件Substance图形")



MDL 图&#x200B;*中[Substance 3D资源](../../getting-started/overview/overview.md) (SBSAR)的*[&#x200B; Substance图形](../../compositing-graphs/substance-compositing-graphs.md)实例

+++

创建图形实例后，它显示为具有以下功能的&#x200B;*节点*：

* 每个图形输出的&#x200B;*类型化输出*&#x200B;连接器。 输出数据的类型如下：
  * RGBA位图：颜色（变化）
  * 灰度位图：Float（变化）
  * 值：匹配值类型（变量）
* 类型为UV坐标的&#x200B;*输入*，用于指定UV坐标，此坐标应该用于映射Substance图形输出的纹理。 如果未连接，则默认值为UV空间中X和Y的经典的0-1线性渐变
* 节点在图形标签之后被&#x200B;*标记为*，如果未定义标签，则标记为标识符，其第一个位图输出为缩略图

使用node属性可以修改图形的&#x200B;*所有动态属性*：

* 输出大小
* 随机种子
* 输入参数
* …

通过节点属性，还可以设置特定于MDL 材质中纹理&#x200B;*映射*&#x200B;方式的参数：

* 平铺
* 使用物理尺寸
* 法线贴图格式
* 切线空间

图形实例节点的输出可以连接到MDL 图中匹配类型的任何节点输入。

请注意，更改<b>SBS基本参数</b>部分中的任何参数涉及重新计算一个或多个Substance图形输出，该参数使用<b>Substance引擎</b>，并且涉及MDL 图计算上的&#x200B;*性能开销*。 在&#x200B;*修改在3D视图中应用的MDL 图中实例化的Substance图形*&#x200B;时，预计会影响性能。

>[!WARNING]
>
> 在MDL 图中使用Substance图形时，导出MDL 图涉及将Substance图形输出烘焙到位图中，这些位图将导出为与导出的MDL文件绑定的纹理。 这意味着图形的参数性质在导出的MDL文件中&#x200B;*丢失*。
