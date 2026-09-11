---
title: 设置材质
description: 设置SDF材料的base color、粗糙度和金属量。
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# 设置材质

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![设置材料图标](set-material.png "设置材料")

<b>In：</b> 3D Function > Material

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

设置SDF材料的base color、粗糙度和金属量。

然后，可以在[形状飞溅v2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)的输出中检索所有飞溅SDF形状的这些值。

</td>
</tr>
</table>

>[!INFO]
> 
> 要了解有关涉及SDF 函数的概念和工作流的更多信息，请转到专用页面： [使用SDF 函数](../../working-with-sdf-functions.md)

## 输入

|                            |                                  |
|----------------------------|----------------------------------|
| <b>SDF场景</b> *浮动* | 输入SDF场景。 |
| <b>基色</b> *浮点3* | 要设置的RGB基色值。 |
| <b>金属性</b> *浮动* | 要设置的金属值。 |
| <b>粗糙度</b> *浮动* | 要设置的粗糙度值。 |
