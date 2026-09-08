---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: 使用Vector Morph节点使用矢量场在两个输入之间变形纹理，以实现平滑过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 矢量图Morph
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# 矢量图Morph

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

通过矢量图扭曲输入图像。 该效果类似于使用正常映射进行UV扭曲，或在视频游戏着色器中使用“流图”。 输入像素由在矢量图的红色和绿色值中定义的矢量移动。

此节点本身并不是最难使用的，但创建正确的矢量图非常小心。 我们建议您使用最高位深度以确保变形时的精度。

Vector Morph与[矢量变形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)非常相似：主要区别在于此Morph节点在被推到画布边界外部时不会“循环”或“平铺”结果。 相反，它会夹紧并重复边缘。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>彩色/灰度输入</i> | 应作为变形目标的源输入。 |
| <b>矢量字段</b> <i>颜色输入</i> | 用于驱动变形的矢量图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>金额</b> <i>0.0 - 1.0</i> | 设置变形效果的强度，作为矢量图的乘数。 |
