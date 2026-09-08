---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: 使用“UV映射器颜色”节点沿样条映射颜色纹理以生成程序化的纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV映射器颜色
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# UV映射器颜色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/uv-mapper-color-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用在UV输入中提供的坐标映射输入彩色图像。

</td>
</tr>
</table>

>[!NOTE]
>
> 另请参阅[UV映射器灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>UV</b> <i>颜色</i> | 以彩色图像的红色(U)和绿色(V)通道编码的图像坐标。 |
| <b>输入</b> <i>颜色</i> | 应映射到UV输入中提供的坐标的彩色图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>颜色</i> | 使用输入UV坐标将输入图像映射为彩色图像的结果。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>背景颜色</b> <i>Float4</i> | 输出图像的背景色。<br>背景在未定义UV的图像区域中可见(即，值为(0， 0， 0， 0))。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![图形中的节点](../../../../../../assets/UVMapperColor-Graph.jpg "图形中的节点")
