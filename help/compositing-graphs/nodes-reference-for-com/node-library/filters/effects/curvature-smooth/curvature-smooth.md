---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: 使用“曲率平滑”节点从Height图生成平滑曲率图以提取曲面细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率平滑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# 曲率平滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![曲率平滑节点图标](curvature-smooth.resources/CurvatureSmooth.png "曲率平滑节点图标"){width="200px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

计算由法线映射描述的曲面的曲率。

曲率图表示曲面的凹和凸区域。\
平面区域为50%灰色。 凸出区域较亮，而凹入区域较暗。

</td>
</tr>
</table>

凹形和凸形区域也将分割为其自己的输出，以便根据这些特性更轻松地选择区域或对其进行蒙版。

>[!TIP]
>
> 查看[曲率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)以获得更清晰的版本，或者[曲率Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)（如果您需要更多选项）。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>正常</b> <i>颜色</i> <b>主要</b> | 描述应该计算曲率的曲面的法线图。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰度</i> | 从输入法线映射计算的曲率映射。   平面区域为50%灰色。 凸出区域较亮，而凹入区域较暗。 |
| <b>凸性</b> <i>灰度</i> | 从输入法线映射计算出的凸度映射。   区域越凸起，地图中的区域就越亮。  平坦或凹进区域为黑色。 |
| <b>凹陷</b> <i>灰度</i> | 从输入法线映射计算出的凹面映射。   区域越凹陷，地图中的区域就越亮。  平坦或凸出区域为黑色。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>正常格式</b> *整数* | 输入法线图的格式。 有效地反转绿色通道。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX：</b> Y轴指向上</li> <li data-preserve-html="true"><b style="">OpenGL：</b> Y轴指向下</li> </ul> |

## 示例

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![曲率平滑：示例2](curvature-smooth.resources/curvature_smooth_example_2.jpg "曲率平滑：示例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![曲率平滑：示例3](curvature-smooth.resources/curvature_smooth_example_3.jpg "曲率平滑：示例3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_before.jpg" alt="curvature_smooth_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_after.jpg" alt="curvature_smooth_example_4_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![曲率平滑：示例4](curvature-smooth.resources/curvature_smooth_example_5.jpg "曲率平滑：示例4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![曲率平滑：示例5](curvature-smooth.resources/curvature_smooth_example_6.jpg "曲率平滑：示例5"){zoomable="yes"}

</td>
</tr>
</table>
