---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: 使用“路径上的四次变换”节点可将二次变换应用于沿路径曲线的元素。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径上的四次变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 1%

---


# 路径上的四次变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/quad-transform-on-paths-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用4个手柄使路径变形。

</td>
</tr>
</table>

## 输入连接器

<b>路径</b> *颜色*\
已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或另一个&#x200B;*路径*&#x200B;处理节点。

## 输出连接器

<b>路径</b> *颜色*\
变换后的路径。 您可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)了解结果所代表的内容，使用其他路径处理节点，或将其输入到[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)以进一步将其处理为样条。

## 参数

<b>p00</b> *浮点2*\
左上角手柄的位置。

<b>p01</b> *浮点2*\
右上角手柄的位置。

<b>p02</b> *浮点2*\
左下手柄的位置。

<b>p03</b> *浮点2*\
右下角手柄的位置。

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
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

![节点示例1](../../../../../../assets/QuadTransformOnPaths-Demo2.gif "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/QuadTransformOnPaths-Demo1.gif "节点示例2")

</td>
</tr>
</table>
