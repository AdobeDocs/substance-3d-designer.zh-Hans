---
title: 胶囊
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>基元>胶囊
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# 胶囊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![胶囊图标](./3d-sdf-capsule.png "胶囊")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种用于长度及半径可调的胶囊的SDF 函数。<br>胶囊是两个球体连接的结果。

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
| <b>开始</b> *浮点3* | 起始球体的位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>结束</b> *浮点3* | 结束球体的位置。<br><br><i>默认值： (0， 0， 1)</i> |
| <b>半径</b> *浮动* | 起始球面和结束球面的半径。<br><br><i>默认值： 0.25</i> |
| <b>开始/结束于tip</b> *布尔值* | 控制<b>开始</b>和<b>结束</b>位置是否应位于球面的最末端。<br>即，控制胶囊的Height是否应包括球面半径。<br><br><i>默认值： False</i> |
| <b>中心位置</b> *浮点3* | 胶囊的圆心的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
