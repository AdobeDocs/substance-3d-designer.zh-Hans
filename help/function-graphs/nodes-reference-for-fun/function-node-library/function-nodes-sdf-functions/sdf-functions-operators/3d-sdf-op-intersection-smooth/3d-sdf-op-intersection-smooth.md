---
title: 交线平滑
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>运算符>交叉线平滑
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 1%

---


# 交线平滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![交叉平滑图标](./3d-sdf-op-intersection-smooth.png "交叉平滑")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

返回两个SDF形状共有的音量，有效是两个形状重叠时创建的音量，其交集的边缘可进行平滑调整。

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
| <b>SDF 1</b> *浮动* | 第一个SDF形状。 |
| <b>SDF 2</b> *浮动* | 第二个SDF形状。 |
| <b>Smoothness</b> *浮动* | 两个SDF形状交叉处的边缘Smoothness。<br><br><i>注意：</i>硬边缘可能出现在平滑半径相交的地方。<br><br><i>默认值： 0</i> |
