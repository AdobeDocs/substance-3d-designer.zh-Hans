---
title: 相交曲面
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>运算符>相交曲面
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# 相交曲面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![交集曲面图标](./3d-sdf-op-intersection-surface.png "交集曲面")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

返回Thickness可调的基底SDF形状与其他SDF形状相交部分的表面。

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
| <b>基本SDF</b> *浮动* | 生成的曲面所基于的SDF形状。 |
| <b>交叉SDF</b> *浮动* | 与基本SDF形状相交的SDF形状。 |
| <b>Thickness</b> *浮动* | 生成的表面的Thickness。<br><br><i>默认值： 0.02</i> |
