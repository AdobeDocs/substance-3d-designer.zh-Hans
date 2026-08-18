---
title: 封闭圆环
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>基元>带顶圆环
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# 封闭圆环

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![带顶圆环图标](./3d-sdf-capped-torus.png "带顶圆环")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

带顶圆环面的SDF 函数，其中沿主圆扫掠小圆可以一定角度封顶。<br>两个圆的半径均可调整。

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
| <b>大半径</b> *浮动* | 小圆沿其扫掠以形成环面的主圆半径。<br><br><i>默认值：0.5</i> |
| <b>小半径</b> *浮动* | 沿主圆扫掠的小圆的半径形成环面。<br><br><i>默认值： 0.2</i> |
| <b>角度</b> *浮动* | 中心角依次定义主圆的修剪圆弧，小圆不会沿着该圆弧扫过。<br><br><i>默认值：0.75</i> |
| <b>角度偏移</b> *浮动* | 沿修剪圆弧的主半径的偏移，小圆不会沿着此偏移进行扫描。<br><br><i>默认值： 0</i> |
| <b>对称</b> *布尔值* | 控制是否应该在一个或两个方向绘制修剪弧。<br><br><i>默认值： True</i> |
| <b>中心位置</b> *浮点3* | 封闭环面支点的世界空间位置。<br><br><i>默认值： (0， 0， 0.5)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
