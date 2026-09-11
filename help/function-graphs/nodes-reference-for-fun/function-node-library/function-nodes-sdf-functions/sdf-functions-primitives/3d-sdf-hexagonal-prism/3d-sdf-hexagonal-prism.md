---
title: 六角棱镜
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>基元>六角棱镜
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 六角棱镜

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![六角棱镜图标](./3d-sdf-hexagonal-prism.png "六角棱镜")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种Height、半径和边缘圆角可调的六面棱镜SDF 函数。

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
| <b>Height</b> *Float* | 六角棱镜的Z向上Height。<br><br><i>默认值： 1</i> |
| <b>半径</b> *Float* | 六角棱镜的半径。<br><br><i>默认值： 0.5</i> |
| <b>舍入</b> *Float* | 应用于六角棱镜边缘的圆角弧的半径。<br><br><i>注意：</i>硬边缘可能出现在圆角半径相交的地方。<br><br><i>默认值： 0</i> |
| <b>中心位置</b> *Float3* | 六角棱镜的支点的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
