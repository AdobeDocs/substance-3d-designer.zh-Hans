---
title: 细长圆柱体
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>基元>伸长圆柱体
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# 细长圆柱体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![细长圆柱图标](./3d-sdf-elongated-cylinder.png "细长圆柱体")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种用于边长度、半径和圆角可调的长圆柱体的SDF 函数。<br>拉长圆柱是两个圆柱桥接的结果。

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
| <b>Height</b> *浮动* | 起始圆柱和结束圆柱的基面的Z向上Height。<br><br><i>默认值： 0.5</i> |
| <b>半径</b> *浮动* | 起始圆柱和结束圆柱的半径。<br><br><i>默认值： 0.5</i> |
| <b>舍入</b> *浮动* | 应用于细长圆柱边缘的圆角弧的半径。<br><br><i>注意：</i>硬边缘可能出现在圆角半径相交的地方。<br><br><i>默认值： 0</i> |
| <b>中心位置</b> *浮点3* | 伸长圆柱的轴心的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>延长距离</b> *浮动* | 起始圆柱沿其拉长的距离。<br>即起始圆柱和结束圆柱中心之间的距离。<br><br><i>默认值： 0.5</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
