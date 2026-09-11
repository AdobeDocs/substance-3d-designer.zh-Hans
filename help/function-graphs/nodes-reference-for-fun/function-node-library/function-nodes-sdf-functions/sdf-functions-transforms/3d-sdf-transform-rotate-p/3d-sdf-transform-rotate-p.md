---
title: 旋转P轴
description: Designer >Substance合成图形>Substance合成节点参考>图形库>SDF 函数>变换>旋转P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# 旋转P轴

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![旋转邮政图标](./3d-sdf-transform-rotate-p.png "旋转邮政信封")

<b>进入：</b>SDF 函数>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

以可调整的角度围绕轴旋转世界空间。<br>输出变换世界位置可以连接到大多数SDF 函数的<b>P</b>输入，以在此变换世界空间中定义它们。<br><br>使用<b>3D查看器</b>的<b>变换透视</b>助手来可视化所执行的旋转。<br><br><i>提示：</i>P变换可以链接在一起，但请记住，结果取决于操作的顺序。

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
| <b>角度</b> *Float* | 世界空间旋转的角度。<br><br>该角度由<b>3D查看器</b>的<b>变换透视</b>助手中的圆圈可视化。 对齐相机以看到<b>轴</b>箭头是此圆的中心，从而清楚地看到旋转的角度只是转弯的一部分。 |
| <b>轴</b> *Float3* | 定义世界空间围绕其旋转的轴的归一化向量。<br>例如， (0， 1， 0)将围绕旋转点的Y轴旋转世界空间。<br><br>轴在<b>3D查看器</b>的<b>变换透视</b>助手中以箭头显示。 箭头的颜色映射到该矢量的XYZ组件上。<br><br><i>默认值： (0， 1， 0)</i> |
| <b>中心点位置</b> *Float3* | 定义旋转原点的枢轴的世界空间位置。<br><br>透视<b>3D查看器</b>的<b>透视变换透视</b>助手中箭头的起点将透视。 |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
