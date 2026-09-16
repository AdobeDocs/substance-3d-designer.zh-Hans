---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/inheritance-in-substance-compositing-graphs.html"
breadcrumb-title: ""
description: 了解继承在Substance合成图形中的工作原理，以创建可重用的图形层次结构和变化。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Inheritance in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 图形中的继承
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 0%
---

# Substance 图形中的继承

此页面描述继承如何在[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)内的[Substance图表](../../compositing-graphs/substance-compositing-graphs.md)中应用以及它对图表输出的影响。

![继承方法](inheritance-in-substance-compositing-graphs.resources/inheritance-overview-1.jpg "继承方法"){width="1400px"}

## 概述

Substance图中的所有节点都可以&#x200B;*继承*&#x200B;源中某些参数的值。 继承意味着更改源中的值将&#x200B;*在从该源继承的所有节点中执行该更改*。 这是Substance 3D Designer生成参数化资源的能力所依据的基本概念之一。

>[!NOTE]
>
> 在本文档的[示例Substance图形](../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)部分中提供了说明继承的注释项目文件。

### 继承方法

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![“绝对”继承方法的图标](inheritance-in-substance-compositing-graphs.resources/ds-inheritance-absolute.png "“绝对”继承方法的图标"){width="128px"}

<b>绝对</b>

没有继承，为参数任意且本地地定义值&#x200B;**

</td>
<td style="border: 0;" valign="top">

![“相对于输入”继承方法的图标](inheritance-in-substance-compositing-graphs.resources/ds-inheritance-relative-to-input.png "“相对于输入”继承方法的图标"){width="128px"}

<b>相对于输入</b>

该值继承自连接到节点&#x200B;*主输入*&#x200B;的数据

</td>
<td style="border: 0;" valign="top">

![“相对于父代”继承方法的图标](inheritance-in-substance-compositing-graphs.resources/ds-inheritance-relative-to-parent.png "“相对于父代”继承方法的图标"){width="128px"}

<b>相对于主页</b>

该值继承自节点或图形的&#x200B;*父*

</td>
</tr>
</table>

![继承方法演示](inheritance-in-substance-compositing-graphs.resources/inheritance-overview.gif "继承方法演示")

对节点的[基参数](../../compositing-graphs/graph-parameters/graph-parameters.md)应用继承方法，该参数是所有节点都具有的&#x200B;*基本方面*&#x200B;行为的公共参数集。 这些参数包括：

* **输出大小**
* **输出格式**（即位深度）
* **像素大小**
* **像素比率**
* **拼贴模式**
* **随机植入**

这应该让您了解&#x200B;*一个*&#x200B;节点中的更改如何影响它的&#x200B;*所有下游节点*&#x200B;的分辨率、精度和拼贴行为。

>[!WARNING]
>
> 要理解此页中讨论的概念，请注意以下重要提示： *实例节点*&#x200B;是表示另一个图形中的图形的[节点](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)，它具有其&#x200B;*自己的离散参数值*，因此术语是&#x200B;*实例*。\
> 例如，同一图形中的两个[Perlin噪声](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/perlin-noise/perlin-noise.md)节点都是&#x200B;*相同*&#x200B;源图形（`noise_perlin_noise.sbs`中的`perlin_noise`）的表示形式，具有它们自己的&#x200B;*参数值集*。

>[!NOTE]
>
> **输出大小：**&#x200B;使用![](inheritance-in-substance-compositing-graphs.resources/props-output-size-lock.jpg)锁定按钮使Height值&#x200B;*匹配*&#x200B;宽度值\
> **随机植入：**&#x200B;使用![](inheritance-in-substance-compositing-graphs.resources/prop-randomise.jpg)按钮向随机植入分配新的随机值。

## 进行更改

### 更改继承方法

在“属性”面板中，节点属性的[基本参数](../../compositing-graphs/graph-parameters/graph-parameters.md)部分中列出的所有参数都有一个与其标签相对的（图标） <b>设置继承方法</b>下拉按钮。\
此按钮允许您选择用于参数的继承方法。

![更改继承方法](inheritance-in-substance-compositing-graphs.resources/inheritance-change.gif "更改继承方法"){width="512px"}

在大多数情况下，*节点*&#x200B;的基参数设置为&#x200B;*相对于输入*，以利用将节点链接在一起的过程行为，而&#x200B;*图形*&#x200B;的基参数设置为&#x200B;*相对于父项*，因此全局参数可以适应使用图形的上下文。

### 调整继承的值

某些基本参数（如[输出大小](../../compositing-graphs/output-size/output-size.md)、像素大小或随机种子）可以&#x200B;*相对于继承值*&#x200B;进行更改。

例如，当“输出大小”参数使用&#x200B;*“相对于……*”继承方法时，值或`(1, -1)`表示&#x200B;*高于*&#x200B;两个分辨率的整数倍X的继承值，以及&#x200B;*低于*&#x200B;两个分辨率的整数倍Y的继承值，例如：

* 继承的值： `(9, 9)`，即`2^9, 2^9 = 512, 512`
* 相对值： `(1, -1)`，即`2^(9+1), 2^(9-1) = 256, 1024`

>[!NOTE]
>
> [输出大小](../../compositing-graphs/output-size/output-size.md)页深入挖掘此关键Base参数，建议阅读以了解如何计算节点的最终分辨率。

如果将函数应用于Base参数，则还将使用该参数的继承方法解释该函数的结果。\
请牢记输出大小示例，一个旨在在X和Y中将继承的分辨率增加两倍的函数应输出`(2, 2)` Integer2值。

## 节点和图形的父子关系

使用“相对于父继承”方法时，您应确切了解该父代在特定上下文中处于什么状态。

节点的父级是它所在的&#x200B;*图形*。

图表的父级是它存在于&#x200B;*上下文*&#x200B;中：

* 如果该图形是作为&#x200B;*实例化*&#x200B;实例化到另一个主机图形中的子图形，则子图形的父级是&#x200B;*实例化*。 该实例化的父级是&#x200B;*主机图形*。
* 如果该图形是根图形，则父应用程序是&#x200B;*应用程序本身*&#x200B;以及该应用程序为给定参数设置的任何值。 例如，图形将继承自[图形视图工具栏](../../interface/the-graph-view/the-graph-view.md)中设置的<b>父项大小</b>参数。

>[!WARNING]
>
> 在将包发布到Substance 3D资源文件(SBSAR)时，父子关系是&#x200B;*按原样应用*。 这意味着将任何参数设置为&#x200B;*Absolute*&#x200B;继承方法将&#x200B;*将该参数锁定*，使其在发布资源中保持当前值。\
> 尽管这对于[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点或[优化目的](../../best-practices/performance-optimization/performance-optimization-guidelines.md)是必需的，例如，我们&#x200B;*强烈*&#x200B;建议在图形中工作时，使用&#x200B;*“相对于……”*&#x200B;继承方法，除非这样做有&#x200B;*清晰、深思熟虑的目的*。

### IN-CONTEXT EDIT

在图形上使用[In-context editing](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)时，节点的父级是&#x200B;*实例化*。 在这种情况下，[图形视图工具栏](../../interface/the-graph-view/the-graph-view.md)中的<b>父级大小</b>设置是&#x200B;*禁用的*，因为图形是继承自实例化的基本参数。

此特性是上下文编辑的&#x200B;*点*，在设置继承方法和评估任何节点的基参数的当前值时，应在&#x200B;*中考虑*&#x200B;因素。

## 使用多个输入的继承

当图形有多个输入时，根据其继承方法，每个输入可能继承自其离散输入数据或继承自图形：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![“相对于输入”继承方法的图标](inheritance-in-substance-compositing-graphs.resources/ds-inheritance-relative-to-input.png "“相对于输入”继承方法的图标"){width="128px"}

<b>相对于输入</b>

无论图形的“基本”参数如何，输入都将继承自其离散的输入数据。 这对于控制每次输入的数据非常有用。

</td>
<td style="border: 0;" valign="top">

![“相对于父代”继承方法的图标](inheritance-in-substance-compositing-graphs.resources/ds-inheritance-relative-to-parent.png "“相对于父代”继承方法的图标"){width="128px"}

<b>相对于主页</b>

输入从图形继承，并且其接收的数据相应地被适配。

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

### 主要输入

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![主输入颜色/灰度](inheritance-in-substance-compositing-graphs.resources/inheritance-primary-input-both.png){width="48px"}

</td>
<td style="border: 0;" valign="top">

![主输入颜色](inheritance-in-substance-compositing-graphs.resources/inheritance-primary-input-color.png){width="48px"}

</td>
<td style="border: 0;" valign="top">

![主输入灰度](inheritance-in-substance-compositing-graphs.resources/inheritance-primary-input-grayscale.png){width="48px"}

</td>
</tr>
</table>

通过在该[输入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md)图形上单击&#x200B;**人民币**，然后在上下文菜单中选择&#x200B;**设置为主要输入**&#x200B;选项，可以将其中一个输入设置为&#x200B;**主要输入**。

</td>
<td style="border: 0;" valign="top">

![输入连接器类型](inheritance-in-substance-compositing-graphs.resources/inheritance-primary-input.jpg "输入连接器类型")

</td>
</tr>
</table>

当图形作为实例节点实例化到另一个图形中时，所有设置为&#x200B;*相对于输入*&#x200B;的实例节点的Base参数将继承连接到&#x200B;*该输入*&#x200B;的数据。 实例节点的“主要”输入可以通过其连接器中的小黑点来标识。

设置为&#x200B;*相对于父项*&#x200B;的其他输入将继承相同的基本参数的值，因为它们继承自&#x200B;*图形*，该图形继承自&#x200B;*实例节点\**，该节点继承自“主要”输入。

\*：如果图形使用*&#x200B;相对于父级*继承方法，则此项为true。

## 示例

下面是一些示例，这些示例涵盖了不同的继承情况以及下列操作器中设置的继承方法的相互作用（从上到下）：

1. Application
1. 主机图形
1. 主机图形中的实例节点
1. 子图 — 即实例节点引用的图
1. 子图中的节点

为操作员设置的&#x200B;*继承方法*&#x200B;正上方以橙色显示。 *继承流*&#x200B;的源，以橙色线条显示。

字母表示基本参数的&#x200B;*个单独集*，应有助于跟踪哪个操作者继承了哪些数据。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

**示例A**

![继承图A](inheritance-in-substance-compositing-graphs.resources/inheritance-schematic-a.png "继承图A"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

**示例B**

![继承图B](inheritance-in-substance-compositing-graphs.resources/inheritance-schematic-b.png "继承图B"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

**示例C**

![继承图C](inheritance-in-substance-compositing-graphs.resources/inheritance-schematic-c.png "继承图C"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

**示例D**

![继承图D](inheritance-in-substance-compositing-graphs.resources/inheritance-schematic-d.png "继承图D"){zoomable="yes"}

</td>
</tr>
</table>

## 解决继承问题

在构建图表并增加其复杂性时，您可能会遇到因继承而导致的意外结果。 如果节点输出具有错误的分辨率或精度（即，位深度），则您应&#x200B;*沿继承链*&#x200B;向上移动，以查明这些值的来源。

检查节点下方显示的数据是一个很好的起点：这些是节点&#x200B;*第一输出*&#x200B;所输出的图像的分辨率、颜色格式和精度。 虽然理解解决方案很简单，但第二部分数据值得详细阐述：

* *字母前缀*&#x200B;引用图像的颜色格式：
  * <b>L</b>：明亮度（即灰度）
  * <b>C</b>：颜色
* *数字*&#x200B;引用图像的位深度（从最低到最高精度）：
  * <b>8</b>： 8位整数（0-1中的256步）
  * <b>16</b>： 16位整数（0-1中的65 536步）
  * <b>16F</b>： 16位浮点（精度低于0-1的值，包括负数）
  * <b>32F</b>：32位浮点（精度高于0-1的高值，包括负数）

如果节点有多个输出，可以通过两种简单的方法检查其分辨率和精度：

* 双击&#x200B;*输出连接器*&#x200B;上的<b>LMB</b>以在[2D视图](../../interface/2d-view/2d-view.md)中显示图像，并检查2D视图视口的&#x200B;*左下角*&#x200B;上显示的图像信息
* 创建[级别](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)或[转换2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)节点，并将其输入连接到要检查的输出。 默认情况下，节点将&#x200B;*从输出*&#x200B;继承，然后您可以检查节点下面的值。

现在，您可以在图形中的节点链上查找&#x200B;*第一个节点*，其中显示意外值。 检查其Base参数的继承方法。

如果没有任何错误且节点是实例节点，则需要更深入并打开该实例节点引用的图形。 从图形的“输出”节点开始重复以上游的过程。

### 常见示例

特别是，*主要输入*&#x200B;概念易于&#x200B;*忽略*，并可能导致继承问题。

[混合](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)节点非常容易受此影响，因为它经常使用。 其<b>Background</b>输入是其主要输入。

![输出大小继承](inheritance-in-substance-compositing-graphs.resources/inheritance-blend.jpg "输出大小继承"){width="512px"}

您需要注意混合两个输入的顺序：您希望保留在图表中的分辨率和精度的输入应连接到“背景”输入（如果您需要的混合模式使其成为可能）。 如果不是，则可能需要调整“混合”节点的“基本”参数及其继承方法以进行补偿。
