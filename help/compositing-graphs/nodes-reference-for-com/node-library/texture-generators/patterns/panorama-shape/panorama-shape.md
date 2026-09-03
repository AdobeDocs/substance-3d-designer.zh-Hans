---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: 使用“全景形状”节点创建映射到全景坐标的形状，以便生成环境纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 全景形状
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# 全景形状

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-01.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对于生成程序化的“Studio”类型的全景图而言，这是一个有用的节点。 允许您放置和修改聚光灯图像，以及设置其HDR属性。 它可以链接在一起用于多个形状。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>形状矩阵</b> | 移动或平移描摹结果，可通过与画布直接交互进行修改。 |
| <b>形状</b> <i>方形，磁盘</i> | 设置形状类型。 |
| <b>形状颜色</b> <i>（颜色值）</i> | 设置形状颜色。 |
| <b>形状强度</b> <i>0.0 - 100.0</i> | 设置形状的HDR强度。 |
| <b>形状柔边框</b> <i>0.0 - 1.0</i> | 更改形状的边框柔和度。 |
| <b>热点强度</b> <i>0.0 - 100.0</i> | 设置形状热点的HDR强度。 |
| <b>热点大小</b> <i>0.0 - 1.0</i> | 更改形状中热点的大小。 |
| <b>热点衰减</b> <i>0.0 - 1.0</i> | 更改热点的衰减、边缘混合。 |
| <b>热点位置</b> <i>0.0 - 1.0</i> | 相对于形状移动热点。 |
| <b>启用背景</b> <i>False/True</i> | 允许用纯色填充背景。 请注意，这意味着您无法再通过混合将它们链接在一起。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 设置背景纯色。 |
| <b>启用纹理输入</b> <i>False/True</i> | 允许自定输入而不是预定义的形状类型。 |
