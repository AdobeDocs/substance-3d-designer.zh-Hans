---
title: 角锥体
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>基元>金字塔
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# 角锥体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![金字塔图标](./3d-sdf-pyramid.png "金字塔")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种Height可调、基部尺寸可调、基部位置可调的金字塔的SDF 函数。

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
| <b>Height</b> *浮动* | 金字塔顶点从其底部开始的Z-upHeight。<br><br><i>默认值： 1</i> |
| <b>基本大小</b> *浮点2* | 金字塔底面在X和Y中的大小。<br><br><i>默认值： (1， 1)</i> |
| <b>基本位置</b> *浮点3* | 金字塔基底的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *浮点3* | 改变的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
