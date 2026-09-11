---
title: 球体
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>基元>球体
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# 球体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![球面图标](./3d-sdf-sphere.png "球面")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

简单球体的SDF 函数。

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
| <b>半径</b> *浮动* | 球面半径。<br><br><i>默认值： 0.5</i> |
| <b>中心位置</b> *浮点3* | 球面透视的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
