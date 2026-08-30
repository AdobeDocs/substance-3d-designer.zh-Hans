---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: 使用“UV映射器灰度”节点沿样条映射灰度纹理，以生成程序化纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV映射器灰度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# UV映射器灰度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](uv-mapper-grayscale.resources/uv-mapper-grayscale-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用UV输入中提供的坐标映射输入灰度图像。

</td>
</tr>
</table>

>[!NOTE]
>
> 另请参阅[UV映射器颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>UV</b> <i>颜色</i> | 以彩色图像的红色(U)和绿色(V)通道编码的图像坐标。 |
| <b>输入</b> <i>颜色</i> | 应映射到UV输入中提供的坐标的灰度图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>颜色</i> | 使用输入UV坐标作为灰度图像映射输入图像的结果。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapperGrayscale-Variant1-After.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapper-Variant2-After.jpg" alt="UVMapper-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![节点示例1](uv-mapper-grayscale.resources/UVMapper-Graph.jpg "节点示例1")
