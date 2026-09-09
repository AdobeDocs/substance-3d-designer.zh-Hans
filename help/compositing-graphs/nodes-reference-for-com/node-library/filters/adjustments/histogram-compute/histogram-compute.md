---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: 使用直方图计算节点计算纹理中的直方图数据，以便进行分析和处理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方图计算
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# 直方图计算

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![直方图计算：图标](histogram-compute.resources/histogram_compute.png "直方图计算：图标"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

计算灰度图像的直方图。

直方图被编码为图像中的像素行，其中每个像素值是与像素在X轴上的位置匹配的颜色值的&#x200B;*种群*。\
例如，75的像素值(0.25， 0)表示图像中具有0.25颜色值的75个像素。

</td>
</tr>
</table>

该节点还输出为图像计算的&#x200B;*累积分布函数* (CDF)。

可使用节点计算的数据创建自定义工具，如自定义蒙版，如下面的“示例”部分所示。

>[!IMPORTANT]
>
> 所有超出[0,1]范围的值都会被固定，因此直方图对于HDR图像可能并不准确。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>灰度</i>主要 | 应为其计算直方图的图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>直方图</b> <i>灰度</i> | 为输入图像计算的直方图，编码为一行像素，其中每个像素值是与像素在X轴上的位置匹配的颜色值的&#x200B;*总体*。   例如，75的像素值(0.25， 0)表示图像中具有0.25颜色值的75个像素。 |
| <b>CDF</b> <i>灰度</i> | 为图像计算的&#x200B;*累积分布函数* (CDF)的结果，以像素行编码，其中每个像素是其左侧所有像素值的总和。   然后，该和相对于图像中的像素总数为&#x200B;*规范化*。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>直方图分辨率</b> *整数* | 直方图的宽度。 值越高，值分布越精细。   可用分辨率为：256、512、1024、2048、4096（像素） |

## 示例

![直方图计算：示例1](histogram-compute.resources/histogram_compute_example_1.jpg "直方图计算：示例1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>
