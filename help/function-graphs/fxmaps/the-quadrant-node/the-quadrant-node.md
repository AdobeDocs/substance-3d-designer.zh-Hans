---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: 使用FXMaps中的象限节点将纹理分为四个部分，以创建拼贴图案和变化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 象限节点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# 象限节点

许多FX-Maps完全由象限节点链组成。 象限节点是FX-Map组中功能最强大、最灵活的节点，因此了解该节点的工作原理非常有价值。

关于象限节点，最重要的是它们是唯一能够增加图形深度或&#x200B;*八度音阶*&#x200B;的节点。 每个象限节点都添加到基础四叉树图形中；其他节点都不这样做。

象限节点具有多个参数：

## 颜色/亮度

当节点将图像添加到FX-Map时，这些设置定义通道与链中其他图像的混合方式。 *颜色/亮度*&#x200B;参数适用于此特定节点渲染的任何图像。

### 分支偏移

移动节点的图像。 该偏移被应用于图形中的后续节点所渲染的所有其他图像。 “分支偏移”会将转换应用到当前象限节点以及图形同一分支中位于该象限节点下的所有节点。

此参数可使用动态函数控制。

### 图案

定义要由此节点添加到FX-Map的图像（如果有）。

象限节点支持一长串模式，本主题稍后将对此进行介绍。

>[!WARNING]
>
> 此参数不能由sbsar 文件中的动态函数控制。

### 样式偏移

按指定的偏移量偏移节点的映像，但不会影响后续节点。 此参数可使用动态函数控制。

### 图案尺寸

定义要添加到FX-Map的图像的大小（如果适用）。 此参数可使用动态函数控制。

### 图案旋转

定义要添加到FX-Map的图像的旋转（如果适用）。 此参数可使用动态函数控制。

### 样式变化

有些模式具有变体。 此设置允许您选择要使用的变体。 此参数可使用动态函数控制。

### 混合模式

指定将此节点的图像（如果适用）混合到FX-Map图像时要使用的混合过程。 此参数可使用动态函数控制。

### 随机种子

随机数生成器的种子。

生成器将此种子用作起始点，创建一系列看似随机数的内容。 这种方法的优势在于，与现实世界不同，您可以确保每次生成完全相同的随机数序列，从而生成可预测、可重复但具有随机外观的结果。

此参数可使用动态函数控制。

### 继承随机

如果设置为“是”，则随机数生成器种子继承自图形中的上一节点（即四叉树中该节点上方的节点）。 如果这是第一个节点，则它从包含的[图形](../../../compositing-graphs/substance-compositing-graphs.md)中获取其随机植入。

## 图案

每个象限节点都可以选择将图像添加到最终FX-Map。

默认情况下，未选择“无图案”，因此不渲染任何图像。 象限节点仅对FX-Map图像进行细分，将其拆分为四组，用于链中的下一个节点。

下一个选项&#x200B;*输入图像*&#x200B;是使用提供给FX-Map节点的图像。 FX-Map节点接受颜色或灰度图像以用作背景或替换其中一个内置图案。 请注意，“象限”节点只能渲染灰度Fx-Map中的输入图像，相反，它只能渲染彩色FX-Map中的输入图像。 如果要混合颜色类型，则需要在图形中转换输入。

最后，您可以从以下内置图案中进行选择：方形、磁盘、抛物面、钟形、高斯、荆棘、金字塔、砖块、层次、波形、半圆、脊状的圆、新月和胶囊体。

其他注意：您可以在此参数中创建动态函数，但只能在Substance 3D Designer中使用。 要通过动态函数访问图像输入，您必须使用从256（图像输入1）到更高值（图像输入2等257）的值。

### 图案类型。

图案都是灰度的。 可以使用&#x200B;*图案变化*&#x200B;参数稍微修改一些图案。

许多内置图案都有某种形式的径向渐变填充或类似内容。 这使它们对于许多类型的噪声和图案非常有用。 其他图案（例如砖块、磁盘和方形）是简单的平坦形状。

“阵列变化”参数调整阵列的定义特征。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/fxmap-quadrants.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/quadrant-parameters.jpg)

</td>
</tr>
</table>
