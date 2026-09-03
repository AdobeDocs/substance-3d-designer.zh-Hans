---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: 使用“MLV颜色模糊”滤镜将运动模糊效果应用于彩色纹理，以获得动态视觉效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLV颜色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---


# MLV颜色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV颜色：图标](mlv-color.resources/mlv-color-01.png "MLV颜色：图标")

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

MLV表示<b>“最小方差平均值”</b>。 此滤镜增强图像的边缘并消除杂色。

此滤镜查找图像中的结构区域，并使用它们来锐化和拼合图像。 在某些情况下，这可能会导致沿比结构区域宽的渐变执行步骤。

</td>
</tr>
</table>

>[!NOTE]
>
> 另请参阅[MLV灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色</i> | 应处理的彩色图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>颜色</i> | 已过滤的彩色图像。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> *浮动* | 应用于图像的筛选的强度。<br><br>值越高，细节的平滑程度越高，平面区域的噪声越平滑。 |
| <b>Smoothness</b> *浮动* | 应用于结构化区域的平滑强度，这会导致区域变圆并减小在较高的筛选强度下可能出现的步进效果。 |
| <b>条件</b> *整数* | 用于选择将定义图像中结构区域的值的标准。<br><br>换言之，像素应如何&#x200B;*分组*&#x200B;到应平滑的区域中。<br><br>*— 方差：*&#x200B;选择在平均值周围具有最低色散的值，这将导致像素群集彼此相似&#x200B;<br>*— 变异系数：*&#x200B;在考虑到平均值的情况下选择值，这将导致较亮区域反向变化较小 |
| <b>高斯</b> *布尔值* | 使用高斯分布将像素分组到结构化区域。<br><br>当值为“True”时，这将使区域更平滑，并减小拼合效果。 |
| <b>影响Alpha</b> *布尔值* | 如果为“True”，则还将筛选应用于图像的Alpha 通道。<br><br>当“False”时，Alpha 通道将被完全忽略，并保留为输出中的原样。 |
| <b>迭代</b> *整数* | 运行筛选器的次数，其中每个迭代都应用于前一个规则的结果。<br><br>更多的迭代会产生更平坦、更锐化的结构区域。 |

## 示例

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/mlv-color-02.png" alt="mlv_Variant4A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mlv-color.resources/mlv-color-03.png" alt="MLV_Variant4B">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/mlv-color-04.png" alt="mlv_Variant5A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mlv-color.resources/mlv-color-05.png" alt="MLV_Variant5B">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/mlv-color-06.png" alt="mlv_Variant3A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mlv-color.resources/mlv-color-07.png" alt="MLV_Variant3B">
      <br><i>之后</i>
    </td>
  </tr>
</table>
