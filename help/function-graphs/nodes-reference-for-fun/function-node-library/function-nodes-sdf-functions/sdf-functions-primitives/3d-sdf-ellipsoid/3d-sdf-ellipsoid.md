---
title: 椭球
description: Designer >Substance合成图形>Substance合成图形的节点引用>节点库>SDF 函数>基元>椭球
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%
---

# 椭球

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![椭球图标](./3d-sdf-ellipsoid.png "椭球")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

椭球的SDF 函数，椭球是可调三维半径的圆形状。

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> 要了解有关涉及SDF 函数的概念和工作流的更多信息，请转到专用页面： [使用SDF 函数](../../../../../../learning-tutorials/nodes/working-with-sdf-functions/working-with-sdf-functions.md)

## 输入

|  |  |
| :--- | :--- |
| <b>半径</b> *Float3* | 椭球半径（X、Y和Z）。<br><br><i>默认值： (0.35、0.35、0.5)</i> |
| <b>中心位置</b> *Float3* | 椭球的透视的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
