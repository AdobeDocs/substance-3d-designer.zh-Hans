---
title: 壳
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>运算符> Shell
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---


# 壳

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![外壳图标](./3d-sdf-op-shell.png "外壳")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使SDF形状中空，所得包络的Thickness可调整。

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
| <b>SDF</b> *Float* | 输入SDF形状。 |
| <b>Thickness</b> *浮动* | 壳的Thickness向内和向外应用。<br>壳在Thickness增加时是圆角的。<br><br><i>默认值： 0.02</i> |
