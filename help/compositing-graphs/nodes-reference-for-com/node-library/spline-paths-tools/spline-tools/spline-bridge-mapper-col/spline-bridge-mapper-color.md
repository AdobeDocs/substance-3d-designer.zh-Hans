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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# 样条桥映射器颜色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-icon.png "节点图标")

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

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |
| <b>彩图</b> <i>颜色</i> | 应跨输入样条映射的输入颜色图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>颜色</b> <i>灰度</i> | 将输入彩色图像作为彩色图像在背景上跨样条映射的结果。 |
| <b>Height</b> <i>灰度</i> | 映射跨样条的样条作为灰度图像的Height。 |
| <b>UV</b> <i>颜色</i> | 用彩色图像的红色(U)和绿色(V)通道编码的映射图像的UV（即坐标）。 |
| <b>蒙版</b> <i>灰度</i> | 跨样条映射的蒙版。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>段数量</b> <i>整数</i> | 在图像坐标遍历样条之前，将样条简化为段。 段数量越多，沿曲线映射就越平滑。 |
| <b>减少UV伸缩</b> <i>布尔值</i> | 调整用于将图像坐标从一个样条插值到下一个样条的方法，以便在样条之间的距离不均匀时使拉伸最小化。 |
| <b>UV 缩放</b> <i>浮点2</i> | 调整图像坐标的比例。 值越高，拼贴的图像就越致密。 |
| <b>UV旋转</b> <i>浮动</i> | 围绕图像坐标中心旋转图像坐标。 |
| <b>背景颜色</b> <i>浮点4</i> | 输出图像中的背景颜色。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-color.resources/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Demo.gif "节点示例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Variant1-After1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Graph.jpg "节点示例2")

</td>
</tr>
</table>
