---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer函数图表中可用的内置系统变量，了解高级工作流程。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 内置变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# 内置变量

您可以在[Substance函数图表](../../../function-graphs/function-graphs.md)中使用内置变量来访问特定值。 它们始终以`$`（美元）符号开头。

某些变量仅在特定上下文中可用。

<b>所有节点</b>

系统变量

| 名称 | 类型 | 目的 |
| --- | --- | --- |
| $size | 浮点 2 | 返回当前节点的大小（像素）。   如果在[输出大小](../../../compositing-graphs/output-size/output-size.md)参数中使用设置为&#x200B;*相对于……* [继承方法](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，则返回&#x200B;*继承值*。 |
| $sizelog2 | 浮点 2 | 如上所述，但以2的幂值形式返回大小（例如：对于2048\*2048图像，`$sizelog2`返回11）。   如果在[输出大小](../../../compositing-graphs/output-size/output-size.md)参数中使用设置为&#x200B;*相对于……* [继承方法](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，则返回&#x200B;*继承值*。 |
| $pixelration | 整数 | 返回与当前节点像素比率（继承或绝对）对应的整数值：0：拉伸1：方形 |
| $tiling | 整数 | 返回与当前节点拼贴模式（继承或绝对）对应的整数值：0：无拼贴1：水平拼贴2：垂直拼贴3：H和V拼贴 |
| $physicalsize | 浮点 3 | 返回[图形的](../../../compositing-graphs/graph-parameters/graph-parameters.md) <b>物理尺寸</b>属性值。 |
| $uvtile | 整数 2 | 使用UDIM工作流时，此变量返回U和V中当前udim的索引。   例如，对于拼贴1003为(2,0)，对于拼贴1118为(7,11)，... |

<b>FX-Map</b>

系统变量

| 名称 | 类型 | 目的 |
| --- | --- | --- |
| $pos | 浮点 2 | 返回模式的出生位置。 原点(0， 0)位于图像的左上角。 |
| $深度 | 浮点 | 返回[FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)节点的八度音阶（级别）编号。 这允许节点根据它所代表的四叉树中的级别来修改其行为。 |
| $depthpow2 | 浮点 | 如上所示，但返回2的乘反值，其值为八度音阶（音阶）数字的次方 — 即1/（2^八度音阶）。 这是帮助值，对于某些常见计算很有用。 |
| $number | 浮点 | 返回绘制的模式的编号。 这可以通过控制[迭代](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md)节点的动态函数图来访问，以便在每个迭代步骤修改其行为。   请注意，`$number`从0开始计数，而不是1。   使用迭代节点链时，`$number`变量将返回使用函数参数之前连接的最后一个迭代节点的迭代编号。 如果要从多个“迭代”节点检索迭代编号，应通过[设置](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md)节点使用“自定义变量”。 |

<b>像素处理器</b>

系统变量

| 名称 | 类型 | 目的 |
| --- | --- | --- |
| $pos | 浮点 2 | 返回正在计算的像素的位置。 |

<b>全局</b>

系统变量

| 名称 | 类型 | 目的 |
| --- | --- | --- |
| $time | 浮点 | 此变量返回自Substance 引擎启动以来的时间（秒）。 它可用于结果会根据经过时间而变化的图形中。  **注意：**&#x200B;虽然目前无法在Designer中更改此值，但集成该Substance 引擎的应用程序可以利用该值，例如[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)用于动画，或[Substance 3D Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home)用于[动态笔触](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes)。 |
| $normalformat | 整数 | 当前环境中使用的普通格式（即，DirectX或OpenGL）。  **注意：**&#x200B;此变量在Designer中无效，可能被集成该Substance 引擎的其他应用程序使用。 |
