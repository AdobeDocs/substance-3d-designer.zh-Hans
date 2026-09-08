---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: 使用“中间值滤镜颜色”节点可减少杂色并保留彩色纹理的边缘。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 中间值滤镜颜色
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# 中间值滤镜颜色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![中间值滤镜颜色：图标](../../../../../../assets/MedianFilter_Icon_Color.png "中间值滤镜颜色：图标")

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此滤镜平滑图像中的杂色同时保留边缘。

对于每个像素，节点根据像素的相邻像素的中值来计算颜色值。

</td>
</tr>
</table>

>[!NOTE]
>
> 另请参阅[中间值滤镜灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色</i> | 应该应用滤镜的彩色图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>颜色</i> | 通过将滤镜应用于输入彩色图像而计算的彩色图像。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>内核大小</b> *整数* | 内核是筛选器计算中使用的一组特定值。 在此上下文中，其值为相邻像素的值。<br><br>对于每个像素，此滤镜将在该像素周围的所有邻居以方形核取出，并计算所有邻居的中值。<br><br>此参数控制方形核的大小（以像素为单位）。 较大的内核会产生更强、更远的平滑效果，但会损失一些细节。<br><br>*- 3x3：*&#x200B;内核宽度为3像素，高度为3像素，总计为8个相邻像素。<br>*- 5x5：*&#x200B;内核宽度为5像素，高度为5像素，总计为24个相邻像素。 |
| <b>筛选器类型</b> *整数* | 应用于内核中取样的邻居的计算。<br><br>*— 中间值：*&#x200B;直接使用所有邻居的中值。<br>*- MLMAD：*&#x200B;表示“最小中间值绝对偏差中间值”。 此偏差解释了数值与中间值的差异。 MLMAD方法没有直接使用中间值，而直接使用所有偏差的中间值，中间值可能由高偏差的异常像素偏斜。 此方法产生更加强大的平滑效果，可能会根据内核大小拼合区域。 |
| <b>影响Alpha</b> *布尔值* | 控制是否应将滤镜应用于图像的Alpha 通道。 当&#x200B;*True*&#x200B;时，Alpha通道保持不变。 |

## 示例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>之后</i>
    </td>
  </tr>
</table>
