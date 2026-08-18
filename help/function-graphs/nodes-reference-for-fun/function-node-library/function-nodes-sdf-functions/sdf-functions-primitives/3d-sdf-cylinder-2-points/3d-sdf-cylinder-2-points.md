---
title: 圆柱体2点
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>基元>圆柱体2点
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 圆柱体2点

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![圆柱体2点图标](./3d-sdf-cylinder-2-points.png "圆柱体2点")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种用于圆柱体的SDF 函数，该圆柱体的半径可调节，该圆柱体由其起始盘和结束盘的位置限定。

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
| <b>开始</b> *浮点3* | 圆柱体起始磁盘的位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>结束</b> *浮点3* | 圆柱体末端磁盘的位置。<br><br><i>默认值： (0， 0， 1)</i> |
| <b>半径</b> *浮动* | 圆柱半径。<br><br><i>默认值： 0.25</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
