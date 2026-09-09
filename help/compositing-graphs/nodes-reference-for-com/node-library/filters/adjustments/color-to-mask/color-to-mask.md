---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: 使用“颜色到蒙版”节点将特定颜色转换为蒙版，以创建选择性处理和蒙版效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 将颜色转换为蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# 将颜色转换为蒙版

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![颜色到蒙版 — 图标](color-to-mask.resources/color_to_mask.png "颜色到蒙版 — 图标"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从彩色图像中的选定颜色提取灰度蒙版。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色</i> | 基于蒙版的颜色应从中提取蒙版的输入彩色图像。 |
| <b>颜色输入</b> <i>颜色</i>   *当“使用颜色输入”设置为“真”时可用* | 用于定义每个像素的参考颜色的输入颜色图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 生成的灰度位图蒙版。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>使用颜色输入</b> *布尔值* | 为了定义每个像素的参考颜色，请使用输入图像而不是统一颜色。    输入图像由<b>颜色输入</b>提供。 |
| <b>颜色</b> *Float3* *在“使用颜色输入”设置为“False”时可用* | 应围绕其执行颜色选择的参考统一颜色。 |
| <b>阈值</b> *浮动* | 到参照颜色的距离，在参照颜色下面将选取颜色。 |
| <b>选择渐隐</b> *浮动* | 根据到参考颜色的距离渐隐颜色选区。 |
| <b>距离色彩空间</b> *整数* | 色调均化流程涉及比较颜色以确定两者之间的距离。 某些色彩空间和距离算法更适合特定的用例。   通过此下拉列表，您可以选择用于比较颜色的色彩空间：<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB（数据）：</i></b>颜色被分为红色、绿色和蓝色通道，并沿这些轴直接分布，而不考虑人类感觉。 这适合用于包含原始数据的图像。</li> <li data-preserve-html="true"><i>线性sRGB（颜色）：</i>颜色被拆分为红色、绿色和蓝色通道，并与像素光照强度成线性关系分布。 这适合用于显示器上可能显示的图像。</li> <li data-preserve-html="true"><b><i>明亮度（颜色）：</i></b>颜色被拆分为色相、色度、明亮度值，其中比较中仅使用明亮度值。 这适合用于显示器上可能显示的图像。</li> <li data-preserve-html="true"><i>Lab（颜色）：</i>标准的可感知色彩空间，它以这样一种方式分配颜色，“感觉”接近的颜色实际上在立方体中靠近。 这适合用于显示器上可能显示的图像。</li> <li data-preserve-html="true"><i>角度（法向）：</i>颜色被分割为矢量的X、Y、Z轴，并通过点积进行比较。 这适合用于包含相切空间法线的图像。</li> </ul> |
| <b>距离权重</b> *浮点3* | Lab颜色距离算法(DeltaE2000)为每个亮度、色度和色相值引入一定的权重因子。   较低的值会减小色差算法中各种因素的影响。   由于眼睛通常接受比色度(C)或色相(H)更大的明度(L)差异，因此(L:C:H)的默认比率为(0.5:1:1)。 0.5:1:1比例将产生两倍于色度或色相的光度差异。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
