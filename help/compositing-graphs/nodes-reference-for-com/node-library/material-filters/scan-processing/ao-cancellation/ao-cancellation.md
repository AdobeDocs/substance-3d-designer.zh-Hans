---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: 使用“AO取消”节点从扫描素材中移除环境遮蔽，以进行干净的纹理处理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO取消
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# AO取消

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## AO取消

**在：** *材质筛选器/扫描处理*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点尝试根据单独的AO映射输入，从反照率（基色）映射中移除任何环境遮蔽光照信息。 使用它可以确保反照率信息的PBR正确，并且基本上不含（强）光照信息。

一个有用的节点，可用于从扫描的网格生成已烘焙的AO映射，或甚至从“Height”或“正常”信息生成的AO映射。

## 参数

* **AO取消**： *0.0 - 1.0*&#x200B;用于删除光照信息的强度。
* **AO饱和度**： *0.0 - 1.0*(De)饱和度补偿去除光照的区域。 这可用于恢复较暗区域中的任何颜色损失。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
