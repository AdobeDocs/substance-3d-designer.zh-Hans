---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: 使用“法向Sobel”节点，通过Sobel边缘检测对表面细节使用高度图生成法线图。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 普通Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# 普通Sobel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-sobel-01.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将Heightmap输入转换为正常映射输出。 此节点是[普通原子节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)的一个稍微高级的版本，它使用Sobel采样而不是标准采样方法。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>0.0 - 3.0</i> | 转换的法线的强度。 |
| <b>正常格式</b> <i>OpenGL，DirectX</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
