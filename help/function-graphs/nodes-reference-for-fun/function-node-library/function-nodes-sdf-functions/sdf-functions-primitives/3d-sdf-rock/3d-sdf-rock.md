---
title: 岩石
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>基元>岩石
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# 岩石

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![摇滚图标](./3d-sdf-rock.png "摇滚")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种使用SDF 函数构建的参数化和随机化岩石形状的SDF 函数。

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
| <b>最大 小平面</b> *整数* | 岩石的最大刻面数（最多32个）。<br><br><i>默认值： 8</i> |
| <b>Smoothness</b> *浮动* | 应用于岩石边缘的圆角弧的半径。<br><br><i>默认值： 0</i> |
| <b>随机性</b> *浮动* | 使表面方向和到中心的距离抖动。<br>因此，值越大，岩石越小。<br><br><i>默认值： 0</i> |
| <b>种子</b> *浮动* | 为<b>Randomness</b>参数提供种子。<br><br><i>默认值： 0</i> |
| <b>缩放</b> *浮动* | 岩石形状的全局缩放。<br>在<b>随机性</b>之后和<b>Smoothness</b>之前应用。<br><br><i>默认值： 0.5</i> |
| <b>中心位置</b> *浮点3* | 岩石圆点的世界空间位置。<br><br><i>默认值： (0， 0， 0.5)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><i>默认：未变换的世界空间位置。</i> |
