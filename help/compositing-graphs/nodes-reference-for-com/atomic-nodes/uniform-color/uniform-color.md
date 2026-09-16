---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ""
description: 使用“统一颜色”节点生成用于创建纯色填充和基层的统一颜色纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 统一颜色
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 7%
---

# 统一颜色

<table>
<tr style="border: 0;">
<td style="border: 0; width: 30%; vertical-align: top">

![原子节点：统一颜色](uniform-color.resources/comp_uniform_1.png "原子节点：统一颜色"){width="20%"}

</td>
<td style="border: 0; vertical-align: top">

生成平面灰度值或颜色值。

它是一个简单的节点，通常用作添加颜色或创建特定值的起点。

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="uniform-color.resources/uniform-color-tooltip.gif" alt="统一颜色工具提示" /></div>


>[!TIP]
>
> 性能优化
> 
> 这两种调整都减少了节点的计算时间和内存占用：
> 
> * 如果需要灰度值，请确保将节点的[颜色模式](#parameters)切换为“灰度”。
> * 由于节点的输出为平面颜色，因此您可以使用尽可能低的分辨率。 设置节点的“[输出大小](../../../../compositing-graphs/output-size/output-size.md)”参数以使用“绝对”[继承方法](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)和16x16像素的分辨率。


## 参数

|  |  |
| --- | --- |
| <b>颜色模式</b> *布尔值* | 在灰度图像和彩色输出图像之间切换。 |
| <b>输出颜色</b> *浮动/浮动4* | 选择要在输出图像中使用的平面颜色。   使用“Alpha”颜色模式时，颜色通道用于不透明度，其中0表示完全透明，1表示完全不透明。 |


## 示例

*即将推出。*
