---
title: 立方体
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>基元>多维数据集
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# 立方体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![多维数据集图标](./3d-sdf-cube.png "多维数据集")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

立方体的SDF 函数，具有可调整的XYZ大小和边缘的圆化。

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
| <b>大小</b> *浮点3* | X、Y和Z上的多维数据集的大小。<br><br><i>默认值： (1， 1， 1)</i> |
| <b>舍入</b> *浮动* | 应用于立方体边缘的圆角弧的半径。<br><br><i>注意：</i>硬边缘可能出现在圆角半径相交的地方。<br><br><i>默认值： 0</i> |
| <b>中心点位置（本地）</b> *浮点3* | 多维数据集本地透视表的世界空间位置，其中(0， 0， 0)将透视表放置在多维数据集的中心。<br><br><i>默认值： (0， 0， -0.5)</i> |
| <b>中心位置</b> *浮点3* | 多维数据集的透视世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
