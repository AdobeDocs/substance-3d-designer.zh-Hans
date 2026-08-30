---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-blend-node.html"
breadcrumb-title: ''
description: 使用“Color blend”（颜色混合）节点通过颜色模式混合纹理，可以在更改色相和饱和度时保留明亮度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color（混合节点）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Color（混合节点）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-blend-node.resources/difference.png){width="128px"}

<b>英寸：</b>滤镜>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

执行“颜色”混合模式，该模式可在采用前景色相和色度的同时保留背景的明亮度。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>前景</b> <i>颜色输入</i> |  |
| <b>背景</b> <i>颜色输入</i> |  |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 在前景和背景之间混合不透明度。 |
| <b>Alpha 值混合处理</b> <i>False/True</i> | 切换前景和背景Alpha通道的混合。 如果设置为False，则会忽略前景的Alpha通道。 |
