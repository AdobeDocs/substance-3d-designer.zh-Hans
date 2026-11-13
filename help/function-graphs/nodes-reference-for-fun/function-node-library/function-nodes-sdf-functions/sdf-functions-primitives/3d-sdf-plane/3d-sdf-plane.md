---
title: 平面
description: Designer >Substance合成图形>Substance合成图形的节点参考>节点库>SDF 函数>基元>平面
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%
---

# 平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![平面图标](./3d-sdf-plane.png "平面")

<b>In：</b>SDF 函数>基元

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

用于可调整方向、位置和大小的平面的SDF 函数。

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
| <b>正常</b> *Float3* | 平面的世界空间法线矢量，用于控制其方向。<br>矢量已规范化。<br><br><i>默认值： (0， 0， 1)</i> |
| <b>大小</b> *Float2* | X和Y中平面的大小。<br><br><i>默认值： (1， 1)</i> |
| <b>Thickness</b> *Float* | 应用于所有方向的平面的Thickness。<br>当Thickness增加时，平面将四舍五入。<br><br><i>默认值： 0</i> |
| <b>中心位置</b> *Float3* | 平面的世界空间位置。<br><br><i>默认值： (0， 0， 0)</i> |
| <b>P</b> *Float3* | 变换的世界空间位置。 使用此输入可使用<b>偏移P</b>和<b>旋转P</b>节点来应用其他变换。<br><br><i>默认：未变换的世界空间位置。</i> |
