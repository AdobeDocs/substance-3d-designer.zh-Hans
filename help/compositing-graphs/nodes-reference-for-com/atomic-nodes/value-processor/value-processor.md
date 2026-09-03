---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ''
description: 使用“值处理器”节点，使用数学运算处理并处理自定义调整的纹理值。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 值处理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 4%

---


# 值处理器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：值处理器](value-processor.resources/value-processor-01.png "原子节点：值处理器"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

计算[Substance函数图形](../../../../function-graphs/the-function-graph/the-function-graph.md)并输出其结果。

它与[像素处理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)类似，不同之处在于它不是为每个像素计算函数，而是计算单个值，使它[在Substance图](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)中可用。

</td>
</tr>
</table>

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
> 此节点是了解[Substance函数图表](../../../../function-graphs/the-function-graph/the-function-graph.md)的良好起点。
> 
> 还要考虑到使用这种类型的图表和执行数学运算对于从这个节点中取出任何东西都是强制性的。

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
| <b>值处理器函数</b> *任何可用的值类型* | 计算[Substance函数图形](../../../../function-graphs/the-function-graph/the-function-graph.md)以计算输出值。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入图像#</b> *灰度/颜色* | 使用[示例颜色](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)或[示例灰度](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)节点访问指定索引输入中的值。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *任何可用的值类型* |  |

## 示例

*即将推出。*
