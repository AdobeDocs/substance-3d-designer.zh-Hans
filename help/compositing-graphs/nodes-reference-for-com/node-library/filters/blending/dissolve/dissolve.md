---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/dissolve.html"
breadcrumb-title: ''
description: 使用“溶解”节点可以使用溶解模式混合纹理，以便在纹理之间创建过渡和渐隐效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Dissolve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 溶解
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 7%

---


# 溶解

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/dissolve-2.png){width="128px"}

<b>英寸：</b>滤镜>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将两个输入与白噪声混合作为过渡的蒙版。

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
