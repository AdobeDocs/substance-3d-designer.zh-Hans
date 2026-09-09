---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
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
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# 阈值

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](threshold.resources/threshold-2.png){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

如果输入像素值相对于&#x200B;**阈值**&#x200B;值符合&#x200B;**模式**&#x200B;参数中设置的&#x200B;*比较标准*，则返回白色。\
类似于[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)，但对比度始终处于最高水平。 用于获得与直方图扫描相似的结果的更精确、更快速的方式。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>阈值</b> <i>0.0 - 1.0</i> | 与输入像素值比较的明亮度值。 |
| <b>模式</b> | 输入像素值应与&#x200B;**阈值**&#x200B;值比较的条件：<br><br>- *大于*<br>- *大于或等于*<br>- *下*<br>- *下或等于* |
