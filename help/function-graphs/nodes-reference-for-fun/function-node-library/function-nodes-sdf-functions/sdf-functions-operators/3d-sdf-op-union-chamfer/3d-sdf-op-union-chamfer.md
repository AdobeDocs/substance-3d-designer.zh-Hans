---
title: 联合倒角
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>运算符>联合倒角
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# 联合倒角

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![联合倒角图标](./3d-sdf-op-union-chamfer.png "联合倒角")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

返回两个SDF形状的附加体积，沿其交叉的边缘具有可调整半径的附加体积。

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
| <b>半径</b> *浮动* | 沿形状交叉点的边缘添加的体积的半径。<br><br><i>默认值： 0</i> |
