---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: 使用“法线”节点可处理和操纵法线映射纹理，以控制表面细节和光照。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法线
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%
---

# 法线

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：正常](normal.resources/comp_normal_1.png "原子节点：正常"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根据被解释为高度图的灰度图像计算法线图。

该节点将输入灰度映射转换为切空间法线映射输出。 它提供了一些用户选项来设置强度和编码。

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="normal.resources/normal-tooltip.gif" alt="正常工具提示" /></div>

它是一种非常有用的节点，通常用于将Height映射输入转换为实时素材的正常映射。 在[Normal Sobel](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md)和Height到正常世界单位中存在替代项。



## 参数

|  |  |
| --- | --- |
| <b>强度</b> *浮动* | 修改Height映射的强度。   设置将输入Height映射解释为法线的密集程度。 根据输入映射，高于100的值几乎不会产生更多效果。 |
| <b>正常格式</b> *布尔值* | 反转Height映射的Y坐标(OpenGL)。   设置绿色(Y)通道的编码方式。 基本上是“Flip Green/Y”（翻转绿色/y）开关。 |
| <b>频道内容Alpha</b> *布尔值* | 用输入纹理填充法线映射的Alpha通道。   将输入/强制Alpha填充Alpha为1：这样可以将Alpha声道设置为纯色，而不是使用输入作为附加Alpha。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度*&#x200B;主要 | 输入解释为Height图的图像。 |


## 示例

*即将推出。*
