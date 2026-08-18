---
title: 细长
description: Designer >Substance合成图形>用于Substance合成图形的节点引用>节点库>SDF 函数>变换>拉长
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# 细长

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![细长的图标](./3d-sdf-transform-elongate.png "细长")

<b>进入：</b>SDF 函数>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从可调整位置拉长SDF形状。<br>从可调切片开始有效地线性扩展SDF形状的体积。

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
| <b>延长</b> *浮点3* | X、Y、Z轴上的延伸长度。 |
| <b>中心位置</b> *浮点3* | 形状将从其伸长的世界空间位置。<br>，即切片伸长的位置。 |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
