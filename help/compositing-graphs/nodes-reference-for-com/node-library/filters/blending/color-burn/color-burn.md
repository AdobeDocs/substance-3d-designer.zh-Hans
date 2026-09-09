---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: 使用“颜色加深”混合节点通过增加对比度来调暗纹理，以创建阴影和加深效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 颜色加深
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---


# 颜色加深

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-burn.resources/color-burn.png){width="128px"}

<b>英寸：</b>滤镜>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在前景和背景之间执行颜色加深混合。 数学公式为1 - （1 — 背景）/前景。

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
| <b>Alpha 值混合处理</b> <i>False/True</i> | 切换前景颜色和背景Alpha 通道的混合。 如果设置为False，则忽略前景的Alpha 通道。 |
