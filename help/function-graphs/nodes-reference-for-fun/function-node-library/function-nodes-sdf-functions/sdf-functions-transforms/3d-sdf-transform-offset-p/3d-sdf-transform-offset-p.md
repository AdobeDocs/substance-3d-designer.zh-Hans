---
title: 位移P
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>变换>偏移P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# 位移P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![偏移P图标](./3d-sdf-transform-offset-p.png "偏移P")

<b>进入：</b>SDF 函数>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

沿矢量偏移世界空间。<br>输出变换世界位置可以连接到大多数SDF 函数的<b>P</b>输入，以在此变换世界空间中定义它们。<br><br><i>提示：</i>P变换可以链接，但请记住结果取决于运算顺序。

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
| <b>偏移</b> *浮点3* | 世界空间在X、Y和Z方向将发生偏移的距离。 |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
