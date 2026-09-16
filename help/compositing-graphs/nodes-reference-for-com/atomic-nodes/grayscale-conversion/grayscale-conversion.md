---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ""
description: 使用“灰度转换”节点，通过各种转换方法将彩色纹理转换为灰度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 灰度转换
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 7%
---

# 灰度转换

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![原子节点：灰度转换](grayscale-conversion.resources/comp_grayscaleconversion_1.png "原子节点：灰度转换"){width="100%"}

<b>在：</b>个原子节点中

</td>
<td style="border: 0;" valign="top">

通过加权每个颜色通道的明亮度，将彩色图像转换为灰度图像。

此节点可以用作从彩色图像提取灰度通道的最优化方法，其方法是将除所需通道（应当设置为1）之外的所有“通道权重”值设置为0。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="grayscale-conversion.resources/grayscale-conversion-tooltip.gif" alt="灰度转换工具提示" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

大多数节点都可以设置为以灰度或彩色输出，其中前者更受青睐，这是出于简单和性能原因。

实际上，建议从一开始就使用灰度图像，并在以后的工作流程中使用[渐变映射](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)节点为图像着色。

这意味着，灰度转换节点通常仅保留用于专门要将彩色图像转换为灰度图像的情况。 在这些情况下，还要看一下[高级灰度转换](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md)和[颜色到蒙版](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md)。



## 参数

|  |  |
| --- | --- |
| <b>通道粗细</b> *浮点4* | 设置灰度转换中每个RGBA通道的权重。   默认情况下，会跨RGB声道执行偶数拆分。 |
| <b>拼合Alpha</b> *布尔值* | 设置Alpha对最终灰度结果的行为，因为灰度值不能包含Alpha信息。   在&#x200B;*True*&#x200B;时，灰度转换将乘以输入图像的Alpha通道 |
| <b>背景值</b> *浮动* | 设置输入具有Alpha蒙版时的基本背景值。 即，确定将哪些像素视为透明。   *当“拼合Alpha”设置为“True”时可用。* |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *颜色*&#x200B;主要 | 要处理的彩色图像。 |


## 示例

*即将推出。*
