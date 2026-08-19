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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
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

“Flood Fill到索引”会根据每个Flood Fill单元格的索引编号将其转换为值，从左上角的0开始。 它可以用于以规范化形式（0.0到1.0，除以Flood Fill找到的单元格数）或作为HDR未钳制值（0到n，其中n是单元格数）返回灰度色调。

此外，索引Flood Fill使用新的[值系统，返回包含找到的形状量和可选的内部数据表的额外值](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/sddoc/values-in-substance-3d-graphs-180192235.html)。

### 输入

* **Flood FillBbox**： *颜色输入*&#x200B;标准Flood Fill输入映射。 必需。
* **特殊形状信息**： *色彩输入*&#x200B;额外的Flood Fill映射，需要在以前的Flood Fill节点上明确启用并且需要连接！

### 参数

* **输出**： *规范化，整数*&#x200B;确定输出是否在LDR 0-1范围或HDR 0-n范围中。
* **忽略小于**&#x200B;的形状： *0.0 - 1.0*&#x200B;忽略小形状的容差值。
* **显示Flood Fill数据表**： *False/True*&#x200B;返回额外的（调试）数据以供高级使用。

## 示例

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
