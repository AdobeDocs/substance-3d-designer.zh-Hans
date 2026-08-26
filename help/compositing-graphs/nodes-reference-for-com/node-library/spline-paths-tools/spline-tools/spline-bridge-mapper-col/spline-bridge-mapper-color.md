---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: 使用“样条桥映射器颜色”节点可通过颜色映射在两个样条之间桥接纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条桥映射器颜色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 样条桥映射器颜色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-bridge-mapper-color-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将彩色图像映射到一个输入样条列表中，以便图像按顺序遍历这些样条。

</td>
</tr>
</table>

>[!TIP]
>
> 映射从列表中的第一个样条转到最后一个样条，并严格遵循列表中这些样条的顺序来遍历中间样条。
> 
> 因此，您应留意预先将样条附加在一起的顺序。

>[!NOTE]
>
> 另请参阅[样条桥映射器灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md)。

## 输入连接器

<b>样条坐标</b> *颜色*&#x200B;在彩色图像的RGBA通道中编码的输入样条点的坐标：\
<b> R</b> - X位置\
<b> G</b> - Y位置\
<b> B</b> -Height\
<b>A</b> — 打包的数据：\
*符号：样条是封闭的（负）或开放的（正）；\
*绝对值：Thickness+ 1。

<b>样条数据</b> *颜色*&#x200B;编码在彩色图像的RGBA通道中的输入样条的其他数据。\
<b> R</b> — 切线X\
<b> G</b> — 切线Y\
<b> B</b> — 未使用\
<b> A</b> — 未使用

<b>样条量</b> *整数*&#x200B;输入样条的数量。

<b>颜色映射&#x200B;</b>*颜色*&#x200B;应跨输入样条映射的输入颜色图像。

## 输出连接器

<b>颜色</b> *灰度*&#x200B;将输入彩色图像作为彩色图像在背景上跨样条映射的结果。

<b>Height</b> *灰度*&#x200B;作为灰度图像，跨样条映射的样条的Height。

<b>UV</b> *颜色*&#x200B;用彩色图像的红色(U)和绿色(V)通道编码的映射图像的UV（即坐标）。

<b>蒙版</b> *灰度*&#x200B;跨样条映射的蒙版。

## 参数

<b>段数量</b> *整数*&#x200B;样条在图像坐标遍历之前被简化为段。\
段数量越多，沿曲线映射就越平滑。

<b>减少UV伸缩</b> *布尔值*&#x200B;调整用于将图像坐标从一个样条插值到下一个样条的方法，以便在样条之间的距离不均匀时最小化拉伸。

<b>UV 缩放</b> *浮点2*&#x200B;调整图像坐标的比例。 值越高，拼贴的图像就越致密。

<b>UV旋转</b> *浮动*&#x200B;围绕图像坐标中心旋转图像坐标。

<b>背景颜色</b> *浮点4*&#x200B;输出图像中的背景颜色。

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "节点示例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "节点示例2")

</td>
</tr>
</table>
