---
title: 无限平面
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>基元>无限平面
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# 无限平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![无限平面图标](./3d-sdf-infinite-plane.png "无限平面")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

可调整方向和位置的无限平面的SDF 函数。

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
| <b>正常</b> *Float3* | 控制其方向的无限平面的世界空间法线矢量。<br>矢量已规范化。<br><br><i>默认值： (0， 0， 1)</i> |
| <b>中心位置</b> *Float* | 平面的枢轴的世界空间位置，作为沿平面法线与世界原点的距离。<br><br><i>默认值： 0</i> |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
