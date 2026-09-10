---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: 使用“样条采样Thickness”节点沿样条采样Thickness值，以获得程序化的效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条采样Thickness
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 样条采样Thickness

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-sample-thickness.resources/spline-sample-thickness-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

通过将输入Thickness映射到输入样条上来修改输入样条的厚度图。

映射Height映射的效果可以通过更改其混合模式以及该效果的不透明度来调整。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>预览</b> <i>灰度</i> | 作为灰度图像的输入样条的预览。 |
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |
| <b>Thickness映射</b> <i>灰度</i> | 用于更改输入样条的Thickness的输入灰度图像。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>预览</b> <i>灰度</i> | 输出样条作为灰度图像的预览。 |
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输出样条点的坐标。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输出样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输出样条的数量。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>采样模式</b> <i>整数</i> | 将厚度图中的值映射到样条的方法： <br>- <i>纹理空间</i>：将这些值应用于样条，如果使用纹理的UV坐标将这些值放置在纹理中，则将这些值应用于样条。 这有效地将值应用于样条的“原位”；<br>- <i>沿样条水平</i>：值直接应用于编码后的样条坐标（请参阅样条坐标输入），其中每行从上到下应用于不同的样条；<br>- <i>Hor。 沿样条线(rand. 偏移X)</i>：值直接应用于已编码的样条坐标（请参阅样条坐标输入），并且在每个样条的“比例映射”（即，样条坐标中的每一行）中具有随机水平偏移；<br>- <i>Hor。 沿样条线(rand. 偏移Y)</i>：值直接应用于已编码的样条坐标（请参阅样条坐标输入），并且在每个样条的“比例映射”（即，样条坐标中的每一行）中具有随机垂直偏移。 |
| <b>不透明度</b> <i>浮动</i> | 厚度图输入对样条Thickness的贡献强度的乘数。 |
| <b>混合模式</b> <i>整数</i> | 将厚度图的数据与输入样条的<span id="_Hlk135820484"></span>Thickness混合的方法：<br>- <i>复制</i>：用高度图值覆盖样条的Thickness；<br>- <i>添加</i>：将厚度图值添加到样条的Thickness；<br>- <i>去除</i>：将厚度图值去除到样条的Thickness；<br>- <i>乘</i>：将厚度图值乘以样条的Thickness。 |
| <b>预览</b> |  |
| <b>段数量</b> <i>整数</i> | 调整用于在预览输出中绘制样条可视化效果的段数。<br>值越高，线条越平滑。 |
| <b>显示方向帮助程序</b> <i>布尔值</i> | 在“预览”输出中，在样条的起始处显示一个点，在其结尾处显示一个箭头。 |
| <b>显示Thickness信封</b> <i>布尔值</i> | 在样条Thickness的边显示附加线。 |
| <b>Thickness（像素）</b> <i>浮动</i> | 调整预览输出中样条可视化的Thickness（以像素为单位）。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
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

![节点示例1](spline-sample-thickness.resources/SplineSampleThickness-Variant1-After1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-sample-thickness.resources/SplineSampleThickness-Demo.gif "节点示例2")

</td>
</tr>
</table>
