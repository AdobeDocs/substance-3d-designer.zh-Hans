---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: 使用像素处理器节点通过自定义表达式处理单个像素以实现高级纹理操作。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 像素处理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# 像素处理器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：像素处理器](pixel-processor.resources/pixel-processor-01.png "原子节点：像素处理器"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

生成图像，其中每个像素的值是指定的[Substance函数图形](../../../../function-graphs/the-function-graph/the-function-graph.md)的结果。

像素处理器允许您在可选输入上，为每个作为输出返回的像素执行自定义函数。

它是迄今为止最通用的节点，因为它允许运行任何数学运算并在图表中返回结果。

</td>
</tr>
</table>

与[FX-Map](../../../../function-graphs/fxmaps/fxmaps.md)类似，它需要设置内部功能以执行任何操作。 像素处理器与FX-Map的不同之处在于，它不专注于使用多种功能控制图案形状和放置，而是放置图案。 相反，每个像素并行运行单个函数，其中每个像素不知道其相邻像素的计算结果。

该像素处理器类似于[值处理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)，它仅运行于单值，与像素处理器相比可提供很好的优化。

对于习惯于在基于节点的编辑器中创建[着色器](../../../../glossary/glossary.md)函数的任何人，该像素处理器应提供熟悉的环境。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 本文档的[示例Substance图形](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)部分提供了演示简单使用像素处理器节点的带批注的项目文件。
> 
> [值处理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)节点是了解[Substance函数图表](../../../../function-graphs/the-function-graph/the-function-graph.md)的良好起点。
> 
> 此外，还要考虑到使用这种图形并执行数学运算对于从这个节点中取出任何东西都是必需的。
> 
> 我们还建议熟悉[UV](../../../../glossary/glossary.md)、[纹理采样](../../../../glossary/glossary.md)和矢量的概念。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>颜色模式</b> *布尔值* | 在灰度图像和彩色输出图像之间切换。 |
| <b>每像素函数</b> *浮动/浮动4* | 输出图像中每个像素计算的[函数图形](../../../../function-graphs/the-function-graph/the-function-graph.md)Substance。   使用设置为<b>$pos</b>变量的[Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)节点访问当前像素的[规范化](../../../../glossary/glossary.md)位置。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入图像#</b> *灰度/颜色* | 使用[示例颜色](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)或[示例灰度](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)节点访问指定索引输入中的值。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

*即将推出。*
