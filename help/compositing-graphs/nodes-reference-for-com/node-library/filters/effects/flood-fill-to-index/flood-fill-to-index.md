---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: 使用“Flood Fill到索引”节点，用索引值填充区域，以创建带编号和标签的图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 索引Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# 索引Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## 索引Flood Fill

**范围：** *滤镜/效果*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

“Flood Fill到索引”会根据每个Flood Fill单元格的索引编号将其转换为值，从左上角的0开始。 它可以用于以规范化形式（0.0到1.0，除以Flood Fill找到的单元格数目）返回灰度色调，也可以用作HDR的未固定值（0到n，其中n是单元格数目）。

此外，索引Flood Fill使用[值](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)，返回找到的形状数量以及可选的内部数据表。

### 输入

* **Flood FillBbox**： *颜色输入*&#x200B;标准Flood Fill输入图。 必需。
* **特殊形状信息**： *色彩输入*&#x200B;额外的Flood Fill映射，需要在以前的Flood Fill节点上明确启用并且需要连接！

### 参数

* **输出**： *标准化，整数*&#x200B;确定输出是否在LDR 0-1范围或HDR 0-n范围内。
* **忽略小于**&#x200B;的形状： *0.0 - 1.0*&#x200B;忽略小形状的容差值。
* **显示Flood Fill数据表**： *False/True*&#x200B;返回额外的（调试）数据以供高级使用。

## 示例

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
