---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: 使用“Flood Fill到灰度”节点，用灰度颜色填充连接的区域，以创建单色图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill为GrayscaleColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# Flood Fill为灰度/彩色

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

## Flood Fill为随机灰度/彩色

**范围：** *滤镜/效果*

**&#x200B;**&#x200B;简单&#x200B;**&#x200B;**

</td>
<td style="border: 0;" valign="top">

## 描述

使用Flood Fill数据生成灰度或颜色值色板。 与[Flood Fill到随机灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)不同，这两个节点允许更好地控制设置确切的变化和色调，并具有额外的输入图来确定要基于每个单元格进行随机化的基值。

它是一个功能强大的系统，可以为每个细胞提供独特的价值或颜色，同时仍然保持控制，并以预先确定的输入为基础。

## 参数

### 输入

* **Flood Fill**： *颜色输入*
* **灰度/彩色输入**： *灰度/彩色输入*

### 参数

* **明亮度/色彩调整**： *-1.0 - 1.0*&#x200B;设置节点的偏差或基值。 当使用灰度或彩色输入时，这用于将初始值更改为一个起点。
* **明亮度/颜色随机**： *-1.0 - 1.0*&#x200B;设置变化量。

</td>
</tr>
</table>
