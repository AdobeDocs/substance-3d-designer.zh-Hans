---
title: 圆环体
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>基元>圆环
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# 圆环体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![环面图标](./3d-sdf-torus.png "环面")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

圆环面的SDF 函数，它是沿着主圆扫描一个小圆而形成的形状。<i>两个圆的半径均可调整。

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
| <b>大半径</b> *Float* | 小圆盘沿其扫掠以形成环面的圆半径。<br><br><i>默认值： 0.5</i> |
| <b>次径</b> *Float* | 沿主圆扫掠的圆的半径形成环面。<br><br><i>默认值： 0.2</i> |
| <b>中心位置</b> *Float3* | 环面的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
