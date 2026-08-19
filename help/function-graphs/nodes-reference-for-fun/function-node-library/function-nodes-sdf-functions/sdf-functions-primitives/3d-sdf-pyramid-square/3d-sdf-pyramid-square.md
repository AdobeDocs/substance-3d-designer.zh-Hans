---
title: 金字塔方形
description: Designer >Substance合成图表>用于Substance合成图表的SDF 函数参考>节点库>节点>基元>金字塔方形
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# 金字塔方形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![棱锥方形图标](./3d-sdf-pyramid-square.png "棱锥方形")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种用于具有方形基部的棱锥的SDF 函数，其Height和基部位置可调节。

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
| <b>Height</b> *浮动* | 金字塔顶点从其底部开始的Z-upHeight。<br><br><i>默认值： 1</i> |
| <b>基本大小</b> *浮动* | 金字塔底部边缘的长度。<br>所有边缘的长度都相等。<br><br><i>默认值： 1</i> |
| <b>基本位置</b> *浮点3* | 金字塔基底的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
