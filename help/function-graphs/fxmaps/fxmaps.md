---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中使用FXMaps将函数图表应用于纹理，以生成程序化图案。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---


# FXMap

**FX-Map节点允许创建程序化图像**。 它是Substance技术最强大的功能之一。

FX-Map代表一种特殊类型的图形，称为马尔可夫链。 马尔可夫链代表了一个简单的核心过程：一次又一次地重复复制和细分图像。 在每个步骤中，可以随意旋转、平移和混合图像。 结果可以是简单图案或复杂噪声。 FX-Maps是随Substance 3D Designer一起安装的许多示例Substance的基础。

## 创建FX-Map图表

如果要查看FX-Map图形，只需将[FX-Map节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)添加到[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)，然后右键单击该节点并按CMD + E (OS X)或CTRL + E (Windows)打开其图形。 此FX-Map图表将显示在“图表”面板上的新选项卡中；您可以通过单击选项卡在此图表和Substance图表之间切换。

## FX-Maps有何用途？

FX-Maps最常见的用途是创建重复图案（如条纹和砖块）和噪声（如柏林噪声、布朗噪声和高斯噪声）。 噪声对于创建有机、自然外观的纹理（如Dirt、Dust、混凝土、石面、液体飞溅等）特别有用。

FX-Map图的工作方式与Substance图不同：在Substance图中，每个节点都是独立的，不了解其在整体图中的位置，也不关心其图像数据来自何处或去往何处。

在下一章中，我们将更详细地了解三个FX-Map图形节点中的每一个节点，但简单地说，每个FX-Map节点都提供了以下三种操作之一：

### 象限

这会将图中此步骤中的图像拆分为四个象限。 这是最常见的节点类型。 一连串象限节点可以创建外观非常复杂的图像以及复杂的图案。

事实上，象限节点在四叉树图表中表示级别，即&#x200B;**八度音阶**。 FX-Map图形通过用单个象限表示树中的每个级别来隐藏此树结构：每次将一个象限节点连接到另一个象限节点时，实际上是在创建完整的树级别。

之所以使用这种“作弊”技术，是因为无需在树的每一层分别表示每个节点：在仅使用四层深度后，您需要使用4 x 4 x 4 x 4节点，即256个单个节点！ 相反，每个象限节点都“知道”自己在树中的哪个级别，并相应生成图像。

这对许多读者来说可能没什么意义，但我们稍后会更详细地介绍。

### 迭代

将传递到右侧连接器的图像重复设置迭代次数，然后将传递到左侧连接器的图像重叠。

此节点通常用于一个或多个动态函数图形，以便在每次迭代中以某种方式移动或旋转输入图像。

### 切换

这需要两个输入，并且按照其选择器设置中的定义，仅在一个或另一个之间进行切换。 与“迭代”节点一样，“选择器”设置通常由“动态函数”选择。

## FX-Maps系统变量

FX-Maps支持系统变量。 这些变量始终以美元符号(“$”)开头，如下所示：

| 名称 | 特殊性 | 数据类型 | 目的 |
| --- | --- | --- | --- |
| $time | - | float1 | 此变量返回自Substance渲染引擎启动以来的时间（秒）。它非常适合需要按时间进行动画制作的Substance。 (E.g. 时钟的指针。)在某些应用中（包括Substance Player），使用$time的Substance会导致时间轴出现在用户界面中。 |
| $深度 | - | float1 | 返回FX-Map节点的八度音阶（级别）编号。 这允许节点根据它所代表的四叉树中的级别来修改其行为。 |
| $depthpow2 | - | float1 | 如上所述，但返回2，其值为八度音阶（级别）数字的次方。 这是帮助值，对于某些常见计算很有用。 |
| $number | 仅迭代节点 | float1 | 返回绘制的模式的编号。 这可以通过控制迭代节点的动态函数图表来访问，以便修改其在每个迭代步骤中的行为。（请注意，$number从0开始计数，而不是1。） |
| $size | - | float2 | 返回当前节点的大小（像素）。 |
| $sizelog2 | - | float2 | 如上所述，但以2的幂值返回大小（例如：对于2048\*2048图像，$sizelog2返回11）。 |
| $pos | 仅象限节点 | float2 | 返回模式的出生位置。 结果始终是一个介于0和1之间的值。 |
