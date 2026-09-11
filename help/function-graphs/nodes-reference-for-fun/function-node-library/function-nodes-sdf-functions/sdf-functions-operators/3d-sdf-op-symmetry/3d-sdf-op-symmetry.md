---
title: 对称
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>运算符>对称
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# 对称

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![对称图标](./3d-sdf-op-symmetry.png "对称")

<b>In：</b>SDF 函数>运算符

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

跨镜像平面翻转和复制SDF形状，然后返回基本SDF形状与其副本的并集。<br>对称可以同时在任何轴上应用。

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
| <b>镜像平面位置</b> *浮点3* | 镜像平面中心的世界空间位置。<br>如果对称应用于多个轴，则所有镜像平面都将共享此位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>镜像轴</b> *整数3* | 设置所需的镜像轴。<br><br>例如，(1， 0， 0)将在X轴上应用对称。<br><br><i>默认值： (1， 0， 0)</i> |
| <b>翻转轴</b> *整数3* | 设置应翻转的轴。<br><br>例如，(1， 0， 0)将翻转X轴上的对称方向。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>预偏移</b> *浮点3* | 应用对称运算符之前，应用于形状的X、Y、Z轴上的偏移。 |
