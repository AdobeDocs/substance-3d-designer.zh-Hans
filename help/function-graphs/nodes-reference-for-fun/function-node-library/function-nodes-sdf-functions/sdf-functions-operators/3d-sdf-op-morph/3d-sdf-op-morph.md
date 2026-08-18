---
title: Morph
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>运算符> Morph
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Morph

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Morph图标](./3d-sdf-op-morph.png "Morph")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据可调整的混合因子，返回基本SDF形状和目标SDF形状之间的线性插值。

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
| <b>基本SDF</b> *浮动* | 基本SDF形状。 |
| <b>目标SDF</b> *浮动* | 目标SDF形状。 |
| <b>混合因子</b> *浮动* | 用于变形输入形状的混合因子，其中0是基本形状，1是目标形状。 |
