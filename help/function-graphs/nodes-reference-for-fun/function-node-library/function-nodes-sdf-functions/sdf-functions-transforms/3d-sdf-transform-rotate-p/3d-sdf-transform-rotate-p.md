---
title: 旋转P轴
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>变换>旋转P
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

以可调整的角度围绕轴旋转世界空间。<br>变换后的输出世界位置可以连接到大多数SDF 函数的<b>P</b>输入，以在此变换后的世界空间中定义它们。<br><br>使用<b>3D查看器</b>的<b>变换透视</b>帮助程序来可视化执行的旋转。<br><br><i>提示：</i>P变换可以链接在一起，但请记住结果取决于操作的顺序。

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
| <b>角度</b> *浮动* | 世界空间旋转的角度。<br><br>角度由<b>3D查看器</b>的<b>变换透视</b>帮助程序中的圆圈可视化。 对齐相机，以看到<b>轴</b>箭头是此圆的中心，从而清楚地看到旋转的角度是转弯的几分之一。 |
| <b>轴</b> *浮点3* | 定义世界空间围绕其旋转的轴的归一化向量。<br>例如： (0， 1， 0)将围绕枢轴点的Y轴旋转世界空间。<br><br>该轴在<b>3D查看器</b>的<b>变换透视</b>帮助程序中由箭头可视化。 箭头的颜色映射到该矢量的XYZ组件上。<br><br><i>默认值： (0， 1， 0)</i> |
| <b>中心点位置</b> *浮点3* | 定义旋转原点的旋转轴的全球空间位置。<br><br>透视图点通过<b>3D查看器</b>的<b>变换透视</b>帮助程序中的箭头的开始可视化。 |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
