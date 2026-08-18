---
title: 平滑合并
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>运算符>联合平滑
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# 平滑合并

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![联合平滑图标](./3d-sdf-op-union-smooth.png "联合平滑")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

返回两个SDF形状的添加体积块，其交叉边的边缘可调整平滑。

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
| <b>Smoothness</b> *浮动* | 平滑半径，从交叉点的边缘开始。<br><br><i>默认值： 0</i><br><br><i>注意：</i>硬边缘可能出现在平滑半径相交的地方。 |
