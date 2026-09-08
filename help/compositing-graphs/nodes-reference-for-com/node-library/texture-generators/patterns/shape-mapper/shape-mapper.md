---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: 使用“形状映射器”节点可将形状映射到具有可自定义变换和定位的纹理上。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状映射器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 2%

---


# 形状映射器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![形状映射器 — 图标](../../../../../../assets/shape_mapper.png "形状映射器 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

沿圆形或多边形投影输入图像。

投影使图像变形以跟随形状的轮廓，并使它恰好适应指定次数而不出现间隙。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 输入

</td>
<td style="border: 0;" valign="top">

### 输出

</td>
<td style="border: 0;" valign="top">

### 参数

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 输入

|  |  |
| --- | --- |
| <b>输入</b> *灰度* | 应沿形状放置的图案。 |

## 输出

|  |  |
| --- | --- |
| <b>输出</b> *灰度* | 图案沿形状的投影结果，如灰度位图。 |

## 参数

|  |  |
| --- | --- |
| <b>形状</b>整数 | 设置应按其放置图案的形状类型：<ul data-preserve-html="true"> <li data-preserve-html="true">圆圈</li> <li data-preserve-html="true">多边形</li> </ul> |
| <b>图案数量</b>整数 | 沿所选形状放置的图案的数量。 |
| <b>具有图案数量的链接段</b>布尔值&#x200B;*在“形状”设置为“多边形”时可用* | 将<b>模式数量</b>用作<b>段</b>的数量。   这样可防止图案环绕边角，从而确保外观笔直一致。 |
| <b>段</b>整数&#x200B;*在“形状”设置为“多边形”且“链接带有图案数量的段”设置为“假”时可用* | 放置图案的多边形的线段数量。   段的大小是&#x200B;*均匀的*，并且所有顶点的距离中心&#x200B;*相等*，因此，增加段量可使多边形向圆收敛。 |
| <b>Radius</b>Float | 形状半径的乘数，其中1.0是图像最短边长度的一半。 |
| <b>宽度</b>Float | 形状上图案宽度的乘数，其中1.0为图像最短边长度的一半。 |
| <b>旋转</b>Float | 应用于形状的旋转量，以从水平右顺时针旋转多少次为单位。 |
| <b>翻转一对2</b>布尔值 | 垂直翻转一个其他形状。 |
| <b>筛选模式</b>整数 | 应用于沿形状放置的图案的筛选方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>最接近：</i>按原样应用最接近投影像素的值，使外观清晰但呈现锯齿。</li> <li data-preserve-html="true"><i>双线性：</i>应用双线性滤镜将投影的像素与其相邻像素插补，以获得更平滑但更模糊的外观。</li> </ul> |
| <b>非方形扩展</b>布尔值 | 在非方形图像中，保持生成的形状为正方形，并将图像生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
