---
title: '平滑减法 '
description: 'Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>运算符>减法平滑 '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# 平滑减法

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![减法平滑图标](./3d-sdf-op-subtraction-smooth.png "减法平滑")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从SDF 2形状中减去SDF 1形状的体积，并在两者相交处应用可调整的平滑。

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
| <b>SDF 1</b> *浮动* | 从中减去的SDF形状。 |
| <b>SDF 2</b> *浮动* | 正在从SDF 1形状中减去SDF形状。 |
| <b>Smoothness</b> *浮动* | 平滑应用于两个形状的交叉点。<br><br><i>注意：</i>硬边缘可能会出现在平滑半径相交的地方。 |
