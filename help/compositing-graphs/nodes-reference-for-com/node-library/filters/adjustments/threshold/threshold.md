---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: 使用“阈值”节点，根据用于创建蒙版的阈值将灰度纹理转换为黑白。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 阈值
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# 阈值

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## 阈值

**范围：** *滤镜/调整*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

如果输入像素值相对于&#x200B;**阈值**&#x200B;值符合&#x200B;**模式**&#x200B;参数中设置的&#x200B;*比较标准*，则返回白色。\
类似于[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)，但对比度始终处于最高水平。 用于获得与直方图扫描相似的结果的更精确、更快速的方式。

### 参数

* **阈值**： *0.0 - 1.0*\
  与输入像素值比较的明亮度值。
* **模式**：\
  输入像素值应与&#x200B;**阈值**&#x200B;值比较的条件：
  * *大于*
  * *大于或等于*
  * *下移*
  * *小于或等于*

## 示例图像

</td>
</tr>
</table>
