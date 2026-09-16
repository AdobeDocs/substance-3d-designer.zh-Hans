---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ""
description: 使用FX-Map节点将函数图形应用于用于创建程序化图案和效果的纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%
---

# FX-Map

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子节点：FX-Map](fx-map.resources/fxmap.png "原子节点：FX-Map"){width="100%"}

<b>进入：</b>个原子节点

</td>
<td style="border: 0;" valign="top">

FX-Map可以反复复制和细分输入的图像或图案，并借助参数和逻辑功能控制每个图案的分布。

它是功能最强大的原子节点之一，也是应用程序中最复杂的节点。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="fx-map.resources/fxmap-tooltip.gif" alt="fx-map工具提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

与[像素处理器](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)类似，由您来定义和创建确定此节点的行为和输出的函数。


>[!TIP]
>
> 阅读[专用指南](../../../../function-graphs/fxmaps/fxmaps.md)，了解并了解有关FX-Map过程的更多信息。

>[!IMPORTANT]
>
> 建议在尝试使用FX-Map节点之前，熟悉软件的各个方面，并且不必为参数创建[数学函数](../../../../function-graphs/function-graphs.md)。


请记住，与其他节点不同，FX-Map的大多数行为并非由参数决定，而是通过编辑其内部的FX-Map函数[&#128279;](../../../../function-graphs/fxmaps/fxmaps.md)来。

|  |  |
| --- | --- |
| <b>颜色模式</b> *布尔值* | 在灰度图像和彩色输出图像之间切换。 颜色将比灰度慢得多。 |
| <b>背景</b> *Float/Float4* | 设置要合成结果的背景起始颜色。 |
| <b>渲染区域</b> *Float4* | 用于设置FX-Map每侧的起始像素范围，从而产生拉伸效果。 |
| <b>拼贴区域</b> *Float4* | 可让您偏移FX-Map的拼贴距离。 |
| <b>在外部剔除</b> *布尔值* | 通过[剔除](../../../../glossary/glossary.md)超出正常范围的图案来执行优化。 |
| <b>粗糙度</b> *浮动* | 用作深度和不透明度乘数。 它对FX-map混合过程应用偏置。 |
| <b>全局不透明度</b> *浮动* | 设置FX映射输出的全局不透明度。 |

## FX-Map指南

*即将推出。*

## 输入连接器

|  |  |
| --- | --- |
| <b>背景</b> *灰度/颜色*&#x200B;主要 | 输出图像的背景色。 |
| <b>输入图像#</b> *灰度/颜色* |  |


## 示例

![](fx-map.resources/image2015-9-10-17-28-32.png)
