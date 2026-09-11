---
title: 旋转
description: Designer >Substance合成图形>Substance合成节点参考>图形库>SDF 函数>变换>旋转
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# 旋转

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![旋转图标](./3d-sdf-transform-rotate.png "旋转")

<b>进入：</b>SDF 函数>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从一个可调整的枢轴点依次围绕一个或多个轴旋转SDF形状。<br>使用<b>3D查看器</b>的<b>变换透视</b>助手来可视化执行的旋转。

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
| <b>角度</b> *浮动* | SDF形状旋转的角度。<br><br>该角度由<b>3D查看器</b>的<b>变换透视</b>助手中的圆圈可视化。 对齐相机以看到<b>轴</b>箭头作为此圆的中心，从而清楚地看到旋转的角度只是转弯的一部分。<br><br><i>默认值： 0</i> |
| <b>轴</b> *浮点3* | 定义SDF形状围绕其旋转的轴的归一化向量。<br>例如， (0， 1， 0)将围绕SDF本地枢轴点的Y轴旋转SDF形状。<br><br>轴在<b>3D查看器</b>的<b>变换透视</b>助手中以箭头显示。 箭头的颜色映射到该矢量的XYZ组件上。<br><br><i>默认值： (0， 1， 0)</i> |
| <b>中心点位置</b> *浮点3* | SDF形状的局部轴心的世界空间位置，其中(0， 0， 0)将轴心放在SDF形状的中心。 定义旋转的原点。<br><br>透视<b>3D查看器</b>的<b>透视变换透视</b>助手中箭头的起点可视化。 |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
