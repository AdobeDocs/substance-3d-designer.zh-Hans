---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: 了解路径和样条节点使用的路径格式规范和数据结构。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径格式规范
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# 路径格式规范

本页介绍“路径”格式，并提供使用“路径”工具中包含的函数处理该格式数据的指导。

## 格式规范

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

本节介绍<b>路径文档</b>（或图像）如何编码：

路径文档是路径列表，每个路径都描述以<b>32位浮点颜色纹理</b>编码的段列表。

纹理被拆分为“顶部”(*$pos.y &lt; 0.5*)和“底部”(*$pos.y > 0.5*)部分。

“顶部”部分像素中的任何数据在语义上与“底部”部分中的匹配像素紧密相关，反之亦然。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![路径多边形编码数据](../../../../../../assets/PathsPolygon_Data.jpg "路径多边形编码数据")

</td>
</tr>
</table>

>[!NOTE]
>
> 路径数据需要32位的精度，使用较低的位深度会产生错误的结果。
> 
> 因此，请确保将生成路径数据的节点的“输出格式”参数设置为“HDR高精度(32F)”。

让`*uv\_pos*`成为“顶部”部分的像素的2D地址（如&#x200B;*$pos*）。

本文档其余部分：

* <b>top[uv\_pos].XYZW</b>将引用顶部像素中存储的4个浮点。\
  top[uv\_pos] == sample\_color(paths， uv\_pos)
* <b>bottom[uv\_pos].XYZW</b>将引用存储在底部匹配像素中的4个浮点。\
  bottom[uv\_pos] == sample\_color(paths， uv\_pos + Float2(0， 0.5))

top[uv\_pos]和bottom[uv\_pos]共同构成文档的语义单元U[uv\_pos]，由8个浮点组成。

### 文档标题

每个“路径”文档都以一个文档页眉开头。 它是第一个语义单位U[(0,0)]：

+++顶部
<b>X</b>

路径数（应为[0； 16777216]中的正整数）。

如果某些路径是空的，它们仍然会计算在此处。 所以你可以把它想成是“要解码的路径标头的数量”。

<b>YZ</b>

此文档的像素大小（即，刚好`Float2(1,1) / $size`）。

在从[像素处理器](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)或[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)（例如，其输出大小不同）读取路径时，此功能非常有用。

<b>宽</b>

1/16 = 0.0625（标题标志）

+++

+++底部
<b>XY</b>

本文档中定义的最后一个顶点的地址。 这有助于附加新数据。

因此，它实际上可以是比最后一个顶点的地址大（按扫描线顺序）的任何地址。 它必须位于&rbrack;0， 1[×]0，.5&lbrack;范围内

<b>ZW</b>

未使用，应为Float2(0， 1)

+++

### 路径标题

文档标头后面紧跟number-of-paths = top[(0,0)].X path-headers（按语义单位排列）。\
E.g. 如果文档中有3条路径，则它们将存储在U[(0,1)\*pixel\_size]、U[(0,2)\*pixel\_size]和U[(0,3)\*pixel\_size] (pixel\_size = top[(0,0)].YZ)中。

如果路径多于像素的一行可以包含的路径，则其余路径标题将按扫描行顺序写入下一行。\
允许具有null路径标头(`top[...].XYZW = Float4(0,0,0,0)`)；此类路径仍然可以作为一个空路径。

将在地址`path\_addr`处定义第N个路径的路径标头定义为：

+++顶部
<b>X</b>

此路径中的顶点数。 必须位于[0， 16777216]范围内。

如果闭合路径的开始和结束顶点位于同一位置，则它们仍然计为2个顶点。\
但具有0顶点的路径仍然是有效的。

<b>年</b>

*Is\_closed*&#x200B;标志：如果路径闭合（如圆形），则为1；否则为0（如直线）。

<b>Z</b>

路径索引&#x200B;*N.*&#x200B;必须完全匹配*path\_addr*（请参见下面的注释）。

<b>宽</b>

标头标志： 1/16 = 0.0625。

+++

+++底部
<b>XY</b>

起始（或第一个）顶点地址。

<b>ZW</b>

结束（或最后一个）顶点的地址。

+++

>[!NOTE]
>
> 您可以使用paths\_tools.sbs中的函数`Utils/pixel\_index\_to\_position`从N计算`path\_addr`： `path\_addr = pixel\_index\_to\_position(N+1)`

### 顶点信息

可以在图像标题（文档或路径标题）后的任意位置找到顶点。 顶点可以是各种“类型”（“开始”、“中间”或“结束”），并且它们使用2个地址指针（“链接”）显式链接在一起。

<b>开始</b>和<b>结束</b>顶点在这方面是特殊的：为了允许表示闭合路径或链接在一起的任意路径网络，实际使用链接之一来形成表示相同顶点的其他所有开始或结束顶点的循环向前链接列表。 这种相互匹配的顶点称为“兄弟姐妹”。 [插图受到欢迎]

形式上，地址`*vert\_addr*`的每个顶点的定义如下：

+++顶部
<b>XY</b>

顶点位置。 坐标可以是任何不是NaN或±inf的浮点值。 在这个层次没有拼贴的概念（它可以通过每个过滤器的实现来处理，也可以不处理），所以路径应该是在欧几里德平面上定义的。

<b>Z</b>

顶点路径索引。 一个顶点只能属于一个Path。 （如前所述，“开始”和“结束”顶点可以具有同级节点。） 路径索引可用于检索路径标题（请参阅上面的“部分路径标题”），因此请确保使其保持同步。

<b>宽</b>

顶点类型。 它在值的符号与其绝对值之间拆分：

在符号部分中，值为0表示实际上此处没有顶点（所有其他元件也都应为0）。 负值表示将顶点标记为“边角”；正值表示顶点“平滑”。 角点与平滑顶点是一个纯粹的隔离属性，对于其余路径编码没有影响或意义。

在绝对值部分，对像素的类型（开始、中间或结束）和另一个标志(trivial\_link)进行编码：

* *0.125*：结束顶点（形状的最后一个顶点；始终是非普通链接，请参阅下文）

* *0.25*：起始顶点（形状的第一个顶点；始终是非平庸链接，请参阅下文）

* *0.5*：带有非平凡链接的中间顶点

* *1*：带有简单链接的中间顶点

“普通链接”是指上一个和下一个顶点（在当前路径的顶点列表中）分别存储在左侧(vert\_addr-(0，pixel\_size))和右侧(vert\_addr+(0，pixel\_size))的像素中，而“非普通链接”意味着其中至少一个顶点存储在其他位置。

+++

+++底部
无论链接是“平凡的”，其可信值都存储在底部：

<b>XY</b>

此路径的上一个顶点的地址。 对于起始顶点，将指向下一个同级顶点。\
如果 |top[vert\_addr].W| = 1，然后bottom[vert\_addr].XY = vert\_addr - (0，pixel\_size)

<b>ZW</b>

此路径的下一个顶点的地址。 对于“结束”顶点，将指向下一个同级顶点。\
如果 |top[vert\_addr].W| = 1，然后bottom[vert\_addr].ZW = vert\_addr + (0，pixel\_size)

+++

## 读取和写入路径信息

如果您想创建自己的路径处理节点，您有多种工具。

[路径顶点处理器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)和[路径顶点处理器简单](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)节点提供了基础知识，它们基本上可以用与[像素处理器](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)相同的方法。

如果您需要路径顶点处理器节点提供的功能之外的功能（更多输入纹理，或更多上一或下一顶点），复制此图表的实现可能是很好的起点(假设您使用自定义处理替换<b>Get(“%perVertex”)</b>节点)。

但是，如果您想做一些比应用单顶点函数更陌生的事，这里提供了对您可以使用的工具的详细说明。 这些通常是可在与其他Paths节点(*paths\_tools.sbs)*&#x200B;相同的包中找到的小帮助器函数。 （这些函数未在[<b>库</b>](../../../../../../interface/the-library/the-library.md)和<b>节点菜单</b>中公开。）

### “读取”函数

在`Read`文件夹下，您可以找到以下几项有助于收集有关路径的信息：

有些可以提供有关给定像素的信息。 它们都将\*top\*部分中的取样Float4值作为输入。 如果你看看它们的实现，它们非常简单。 他们的目的是传达更多含义，而不仅仅是原子节点：

+++is_header
检查当前采样值是路径页眉还是文档页眉。

+++

+++path_is_closed
检查路径标头中的Is\_Closed标志(.Y)。 它\*假定您已检查它是否为`is\_header`的路径\*，并且`current\_pixel\_is\_document\_header`返回了false。

+++

+++is_vertex
检查当前采样值是否为顶点，即不是标题，也不是空像素。

+++

+++is_start_vertex
检查\*顶部零件取样\*值是否为起始顶点（无需先检查`is\_vertex`）。

+++

+++is_mid_vertex
检查\*顶部零件采样\*值是否为非起始或结束顶点的顶点（无需先检查`is\_vertex`）。

+++

+++is_end_vertex
检查\*顶部零件取样\*值是否为“结束”顶点（无需先检查`is\_vertex`）。

+++

+++is_segment_start
`is\_start\_vertex || is\_mid\_vertex`的短手。 对于基于[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)的处理（最多处理一次每个段）更有用。

+++

+++is_corner
检查顶点的边角标志（无需先检查`is\_vertex`：如果答案为true，则您肯定位于顶点上）。 请注意，官方节点尚不支持此标志。

+++

+++has_trivial_links
如果是顶点，将指示是否可以在不对底部进行采样的情况下轻松推导上一顶点和下一顶点的位置。 （注意：非顶点将始终返回false。）

您可能不想直接使用此项，而是使用`sample\_next\*`或`sample\_prev\*`函数之一，由它们为您处理。

+++

+++sample_next， sample_prev
在给定顶部采样值`*sampled*`及其位置`*sampled\_position*`的情况下，返回下一个（分别为上一个）顶点顶部采样值，并将浮点数2变量`*next\_sampled\_pos*`设置为此邻居的位置(即&lt;returned value> = SampleColor(next\_sampled\_pos， image0))。 `*input0PixSize*`必须等于路径的像素大小(top[(0,0)].YZ)。

如果当前像素(`*sampled*`)是<b>开始</b>顶点，*sample\_prev*&#x200B;将返回此顶点的下一个同级成员；同样，如果它是<b>结束</b>顶点，*sample\_next*&#x200B;将返回此顶点的下一个同级成员（即，可能不是您想要的）。 请参阅下面的`*sample\_next\_advanced*`和`*sample\_prev\_advanced*`来解决此问题。

请注意，为简单起见，<b>路径信息假定存储在input0！</b>中 此外，与函数的doc状态不同，您不需要预声明`*next\_sampled\_pos*`。 `*[out]next\_sampled\_pos*`是一个虚拟参数，用于提醒您存在第二个“返回值”。

可以在第三迭代节点的Iterations参数中检查`*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)，以说明如何使用它。

![sample_next的最小用例](../../../../../../assets/paths-spec_fxmap-sample-next_02.png "sample_next的最小用例")



![预览路径中sample_next的用例(path_trace)](../../../../../../assets/paths-spec_fxmap-sample-next_01.png "预览路径中sample_next的用例(path_trace)")



+++

+++sample_next_advanced， sample_prev_advanced
这是为了处理闭合路径。 对于开放路径，“起始”或“结束”顶点没有同级，在这种情况下，两个函数都返回相同且唯一的邻居。 对于具有多个同级的“开始”或“结束”顶点（将路径连接为网络），这将返回链接列表中下一个同级的相邻顶点。

+++

### “写入”函数

在`Write`文件夹下，您会发现一些小帮助程序，这些帮助程序生成准备由[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b>写入<b>的Float4。

实际上，[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)在绘制之前会将RGB与Alpha相乘，因此会取消预乘实际值以对其进行补偿。 如果您想在[像素处理器](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)中使用这些函数，我们建议您自己再次应用预乘，或者编写自定义版本（更优化且更易于使用）。

+++document_header
生成文档标题的顶部，声明您提供的路径数。

+++

+++document_last_vertex_spec
生成文档标题的\*bottom\*部分，该部分指定最后一个顶点地址（请参见A.1.）。

+++

+++path_header
根据路径`*nbVertices*`中的顶点数、`*isClosed*`标志和`*pathIndex*`生成路径标头的顶部。

+++

+++start_vertex、mid_vertex、end_vertex
生成顶点的顶部，并相应地设置位置、类型和其他选项。

约&#x200B;*mid\_vertex*&#x200B;和&#x200B;*hasTrivialLinks*&#x200B;参数：理想情况下，您应设置适当的值，但如果由于任何原因您最终无法判断链接是否微不足道，则可安全地将其设置为false（代价是较慢地处理所生成的路径）。

+++

没有用于路径标头或顶点的底部生成器：两者都编码到顶部的两个链接，因此此函数本质上将是来自两个Float2的Vector Float4构造函数。 如果使用[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)进行写操作，请不要忘记将XYZ除以W （W是地址的Y，它不应为Null）。

您将在托管[路径多边形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)节点的&#x200B;<b>*paths\_polygon.sbs* </b>包中找到相关示例，说明如何使用这些函数。

### 处理路径的方法

您可能会使用像素处理器或Fx-Map来实现您的自定义处理，每种处理都有其优势和弱点：

+++FX-Map
当执行需要全局了解整个路径（或路径）或累积路径（例如，在抽取或镶嵌后重新打包顶点）的高层操作时，通常首选基于[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)的解决方案。 这种方法也是最简单的方法，因此，如果您是第一次进行自定义处理，您可能需要使用Fx-Map，尽管它&#x200B;*可能*&#x200B;会比较慢。

您需要先熟悉Fx-Map。 如果不是，请查看[特定文档](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)。

我们建议您查看&#x200B;<b>*路径\_trace.sbs*</b>&#x200B;中的[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)和&#x200B;<b>*路径\_多边形.sbs*</b>&#x200B;中的[路径多边形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)的实现，以了解如何使用Fx-Map（分别）读写路径。

+++

+++像素处理器
如果您只需要“本地”信息，[像素处理器](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)解决方案将适合。 这里我们指的是“局部”不是空间上的（元素之间的距离），而是拓扑上的（链接在一起的顶点）。 这就是顶点处理器的实现方式。 对于此类操作，像素处理器通常比Fx-Map快，因为每个像素的功能都是并行计算的，而访问的数据量有限。 但实现工作可能更为重要，因为您只能修改当前像素。

我们不会透露详细信息，因为根据您的具体用例，我们将透露很多信息，但第一件事是检查您的位置：

您是位于顶部($pos.y &lt; 0.5)还是底部($pos.y > 0.5)？ 我们建议记住，在专用变量（例如`*isTop*`）中，创建`*vert.addr*` Float2时，顶部的值为`*$pos*`，底部为`$pos - (0,0.5)`。

*vert.addr*&#x200B;处是什么？ 对其取样并检查是否存在任何内容(W != 0)，如果存在，则确切地检查是否存在任何内容。 标题(W = 0.0625) （用`*Read/is\_header*`检查）或顶点（用`Read/is\_vertex`检查）？ 如果是页眉，那么它是文档页眉还是路径页眉？ （可使用`*Read/current\_pixel\_is\_document\_header*`检查这一点。） 使用一个或多个帮助函数来匹配您感兴趣的内容。

+++
