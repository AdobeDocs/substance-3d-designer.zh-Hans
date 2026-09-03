---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-smooth.html"
breadcrumb-title: ''
description: 使用斜面平滑节点在形状和图案上创建逼真的表面的平滑斜边。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜面平滑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---


# 斜面平滑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向异性科威特灰度图标](bevel-smooth.resources/bevel-smooth-01.png "各向异性科威特灰度图标"){width="200px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从蒙版边界向外或向内绘制渐变或平面颜色，或同时从两者都绘制。

重叠渐变按反相归一化距离排序，以便绘制到最接近边框的距离。

可以使用距离图沿边界动态调整渐变的距离。

</td>
</tr>
</table>

>[!TIP]
>
> [方向距离](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md)节点提供了类似功能，其中扩展是在特定方向执行的。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版输入</b> <i>灰度</i>主要 | 应从中提取蒙版的图像。   所有高于“蒙版阈值”的值在该蒙版中均为白色。 |
| <b>源输入</b> <i>灰度</i> | 仅当“Output Mode”参数设置为“Displation”时才使用可选输入。   在这种情况下，该图像将叠加在蒙版的白色区域上，并且扩展边界处的灰度值。 |
| <b>距离图</b> <i>灰度</i> | “距离图乘数”参数的值大于0时使用的可选输入。   它用于调整沿蒙版边界的斜角/扩展距离，其中较暗的值导致较短的距离。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 结果图像，根据选定的“输出模式”。 |
| <b>UV</b> <i>颜色</i> | UV图，其中UV沿蒙版边界扩展。   可以将其连接到[UV映射器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md)节点，以使用这些扩展的UV映射任何其他图像。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输出模式</b> *整数* | 扩展蒙版边界的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>斜面：</b>绘制一个从1到0的渐变，其中0已达到最大“距离”</li> <li data-preserve-html="true"><b>膨胀：</b>绘制纯色远至“最大距离”。 此颜色为白色或蒙版边框处的“源输入”图像（如果已连接）</li> <li data-preserve-html="true"><b>距离：</b>距离最接近蒙版边框的原始距离，以规范化的图像空间表示，其中1是图像最短一侧的长度</li> </ul> |
| <b>方向</b> *整数* *在“输出模式”设置为“斜角”或“膨胀”时可用* | 应扩展的蒙版边框的一侧：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>进入：</b>向蒙版内部绘制</li> <li data-preserve-html="true"><b>向外：</b>向蒙版外部绘制</li> <li data-preserve-html="true"><b>入/出：</b>向蒙版的内部和外部绘制</li> </ul> |
| <b>最大距离</b> *浮动* | 在归一化图像空间中，膨胀的距离，其中1是输入图像的短边的长度。 |
| <b>蒙版Smoothness</b> *浮动* | 应用于蒙版的平滑程度。   该值是模糊的半径，1个单位是图像的1/256。 |
| <b>蒙版偏移</b> *浮动* | 向内或向外移动蒙版边界。 |
| <b>蒙版阈值</b> *浮动* | 用于检测“蒙版输入”图像中的蒙版边界的值。   高于此阈值的值是蒙版形状的&#x200B;*内*，低于此阈值的值是&#x200B;*外*。 |
| <b>缩放</b> *浮点2* | 调整扩展的水平(X)和垂直(Y)距离。   这些值是“最大距离”参数值的乘数。 |
| <b>距离图乘数</b> *整数* | 在“最大距离”上调整“距离图”的影响。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![斜面平滑：示例1](bevel-smooth.resources/bevel-smooth-02.gif "斜面平滑：示例1"){width="1024px" zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![斜面平滑：示例8](bevel-smooth.resources/bevel-smooth-03.jpg "斜面平滑：示例8"){width="1024px" zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-04.jpg" alt="bevel_smooth_example_4_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-05.jpg" alt="bevel_smooth_example_4_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-06.jpg" alt="bevel_smooth_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-07.jpg" alt="bevel_smooth_example_2_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-08.jpg" alt="bevel_smooth_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-09.jpg" alt="bevel_smooth_example_3_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-10.jpg" alt="bevel_smooth_example_5_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-11.jpg" alt="bevel_smooth_example_5_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-12.jpg" alt="bevel_smooth_example_7_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel-smooth-13.jpg" alt="bevel_smooth_example_7_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>
