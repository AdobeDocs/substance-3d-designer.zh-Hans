---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: 使用直方图渲染节点可以将直方图数据可视化作为分析和调试的纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方图渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# 直方图渲染

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向异性科威特灰度图标](../../../../../../assets/histogram_render.png "各向异性科威特灰度图标"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

绘制灰度图像的直方图。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 输出连接器

</td>
<td style="border: 0;" valign="top">

### 参数

</td>
</tr>
</table>

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度*&#x200B;主要 | 应为其绘制直方图的图像。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度* | 根据输入图像计算的直方图可视化。 |

## 参数

|  |  |
| --- | --- |
| <b>直方图分辨率</b> *整数* | 直方图的宽度。 值越高，值分布越精细。   可用分辨率为：256、512、1024、2048、4096（像素） |
| <b>自动缩放</b> *布尔值* | 如果为“True”，则重新映射直方图以使用图像的完整Height。   如果为“False”，则每列使用的Height像素数与输入图像中出现的值相同。 |
| <b>缩放</b> *Float* | 垂直缩放直方图，值1表示直方图的完整Height。 |
| <b>取样</b> *整数* | 直方图图像的筛选方法，当直方图分辨率和渲染分辨率不匹配时，会影响描摹结果：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>双线性：</b>将双线性的筛选应用于直方图，从而产生插值点</li> <li data-preserve-html="true"><b>最接近的：</b>对最近的像素进行采样，不进行筛选，导致平移</li> </ul> |
| <b>翻转Y轴</b> *布尔值* | 如果为“True”，则垂直镜像直方图。 |

## 示例

![直方图渲染：示例1](../../../../../../assets/histogram_render_example_1.png "直方图渲染：示例1"){zoomable="yes"}

![直方图渲染：示例2](../../../../../../assets/histogram_render_example_2.png "直方图渲染：示例2"){zoomable="yes"}
