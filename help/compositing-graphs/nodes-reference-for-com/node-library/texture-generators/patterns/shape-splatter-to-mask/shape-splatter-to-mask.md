---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: 使用“形状飞溅到蒙版”节点，将形状飞溅图案转换为蒙版，以实现素材混合和效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状飞溅到蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# 形状飞溅到蒙版

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据图案ID，将[形状飞溅](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)数据转换为黑白蒙版。 例如，允许您仅创建某种类型的蒙版。 提供了额外的选项，可选择图案ID的范围并随机隐藏一些形状。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>图案ID起始范围</b> <i>1 - 8</i> | 设置要选择的范围内的第一个图案ID。 |
| <b>模式ID结束范围</b> <i>1 - 8</i> | 设置要选择范围中的最后一个模式ID 。 |
| <b>随机蒙版</b> <i>0.0 - 1.0</i> | 设置图案比例以随机遮盖。 |
| <b>输出</b> <i>二进制蒙版，整数蒙版，灰度值</i> | 确定输出值的类型。 “二进制蒙版”只返回黑白色、0或1的值，“整数蒙版”将以HDR格式对每个图案编码较高的值（最多8个），“灰度值”将按比例在0和1之间扩展范围。 |
