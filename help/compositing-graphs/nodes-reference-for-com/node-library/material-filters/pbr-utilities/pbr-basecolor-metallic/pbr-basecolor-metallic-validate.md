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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR基色/金属验证

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR基色/金属验证

**在：** *材质滤镜/PBR实用工具*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据PBR标准生成值正确或不正确的好坏“热图”的实用程序节点。

它作为PBR的学习工具非常有用，因为它提供了关于错误及其查找位置的非常清晰的视觉反馈。

不要将此工具用作最终工具，但仍要确保您始终清楚地了解为什么要违反此工具可能突出显示的任何规则。

## 参数

* **验证模式**： *反照率、金属、组合*&#x200B;设置是否仅检查反照率、金属或两者组合作为概述模式。
* **反照率暗范围阈值**： *50 sRGB， 30 sRGB*&#x200B;将反照率下限设置为50或30 sRGB。 可以减小或增大红色区域的容差。
* **金属反射范围**： *70-100%反射，60-100%反射*&#x200B;改变金属范围，认为正确。 可以减小或增大红色区域的容差。
* **叠加图**： *False/True*&#x200B;用于叠加输入图的快速调试模式，可更快地跟踪问题区域。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
