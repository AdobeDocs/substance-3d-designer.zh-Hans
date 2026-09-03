---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: 使用“PBR BaseColor金属验证”节点验证并更正PBR素材的基色和金属色值。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR BaseColor金属验证
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR基色/金属验证

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-basecolor-metallic-validate.resources/pbr-basecolor-metallic-validate-01.png){width="128px"}

<b>进入：</b>材质过滤器> PBR实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据PBR标准生成值正确或不正确的好坏“热图”的实用程序节点。

它作为PBR的学习工具非常有用，因为它提供了关于错误及其查找位置的非常清晰的视觉反馈。

不要将此工具用作最终工具，但仍要确保您始终清楚地了解为什么要违反此工具可能突出显示的任何规则。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>验证模式</b> <i>反照率，金属，已合并</i> | 设置是仅检查反照率模式、金属模式还是同时检查这两种模式作为概述模式。 |
| <b>反照率的深色范围阈值</b> <i>50 sRGB， 30 sRGB</i> | 将反照率下限设置为50或30 sRGB。 可以减小或增大红色区域的容差。 |
| <b>金属反射范围</b> <i>70-100%反光，60-100%反光</i> | 将金属范围更改为正确。 可以减小或增大红色区域的容差。 |
| <b>叠加地图</b> <i>False/True</i> | 通过快速调试模式叠加输入图，可更快地跟踪问题区域。 |
