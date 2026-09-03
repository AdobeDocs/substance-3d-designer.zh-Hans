---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: 使用“AO取消”节点从扫描的材料中删除ambient occlusion，以便进行干净的纹理处理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO取消
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# AO取消

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancellation-01.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点尝试根据单独的AO映射输入，从反照率（基色）映射中移除任何环境遮蔽光照信息。 使用它可以确保反照率信息的PBR正确，并且基本上不含（强）光照信息。

一个有用的节点，可用于从扫描的网格生成已烘焙的AO映射，或甚至从“Height”或“正常”信息生成的AO映射。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>AO取消</b> <i>0.0 - 1.0</i> | 用于删除光照信息的强度。 |
| <b>AO饱和度</b> <i>0.0 - 1.0</i> | (De)对光照被移除的区域进行饱和度补偿。 这可用于恢复较暗区域中的任何颜色损失。 |
