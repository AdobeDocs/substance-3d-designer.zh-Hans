---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: 使用直方图均衡节点重新分布像素强度以提高对比度和亮度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方图均衡
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# 直方图均衡

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![直方图色调均化：图标](../../../../../../assets/histogram_equalize.png "直方图色调均化：图标"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使灰度图像的直方图均衡，有效地调整灰度值以实现均匀分布。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>灰度</i>主要 | 应为其均衡直方图的图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 应用直方图均衡化的结果图像。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>直方图分辨率</b> *整数* | 直方图的宽度。 值越高，值分布越精细。   可用分辨率为：256、512、1024、2048、4096（像素） |
| <b>直方图平滑</b> *浮动* | 可通过重新分布图像中的灰度值来平滑直方图，以使每个值之间的&#x200B;*差值*&#x200B;相等。   此参数调整该平滑的强度。 |

## 示例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![直方图均衡：示例1](../../../../../../assets/histogram_equalize_example_3.png "直方图均衡：示例1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![直方图均衡：示例2](../../../../../../assets/histogram_equalize_example_5.png "直方图均衡：示例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![直方图均衡：示例3](../../../../../../assets/histogram_equalize_example_6.png "直方图均衡：示例3"){zoomable="yes"}
