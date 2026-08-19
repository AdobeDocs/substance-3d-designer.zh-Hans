---
title: 舍入
description: Designer >Substance合成图表>用于Substance合成图表的“节点”参考>“节点库”>“SDF 函数”>“运算符”>“舍入”
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# 舍入

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![舍入图标](./3d-sdf-op-rounding.png "舍入")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

展开SDF形状，使其膨胀和平滑其硬边缘。

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
| <b>SDF</b> *浮动* | 输入SDF形状。 |
| <b>半径</b> *浮动* | 应用于形状边缘的圆角弧的半径。<br><br><i>注意：</i>硬边缘可能出现在圆角半径相交的地方。<br><br><i>默认值： 0.05</i> |
