---
title: 封闭圆锥2点
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>基元>封闭的圆锥2点
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# 封闭圆锥2点

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![封顶圆锥2点图标](./3d-sdf-capped-cone-2-points.png "封顶圆锥2点")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

由圆锥的底部和顶部的位置定义的圆锥的SDF 函数。<br>底部和顶部具有可调整的半径。

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> 要了解有关涉及SDF 函数的概念和工作流的更多信息，请转到专用页面： [使用SDF 函数](../../working-with-sdf-functions.md)

## 输入

|  |  |
| :--- | :--- |
| <b>定位基数</b> *Float3* | 封顶圆锥基底的位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>位置靠上</b> *Float3* | 封闭圆锥顶部的位置。<br><br><i>默认值： (0， 0， 1)</i> |
| <b>Radius基</b> *Float* | 封闭圆锥的基底的半径。<br><br><i>默认值： 0.5</i> |
| <b>半径顶部</b> *Float* | 封闭圆锥顶部的半径。<br><br><i>默认值： 0.2</i> |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
