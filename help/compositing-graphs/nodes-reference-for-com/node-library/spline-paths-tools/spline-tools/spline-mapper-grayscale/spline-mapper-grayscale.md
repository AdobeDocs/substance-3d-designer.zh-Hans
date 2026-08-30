---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: 使用“样条映射器灰度”节点沿带有可自定义参数的样条路径映射灰度纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条映射器灰度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---


# 样条映射器灰度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-mapper-grayscale.resources/spline-mapper-grayscale-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将输入灰度图像映射到沿输入样条拉伸的基本形状上。

原始形状可以是平面、半圆柱或圆柱体。 圆柱体可以沿着样条线扭转，从而相应地使映射的图像变形。

</td>
</tr>
</table>

该节点将映射的图像输出为灰度图像，以及诸如Height、UV（即图像坐标）和用于独立地选择每个映射样条的ID蒙版等其他信息。

>[!IMPORTANT]
>
> 当使用极低的Thickness值时，结果可能包括样条包络外的不期望伪像。 这是一个已知问题。

>[!NOTE]
>
> 另请参阅[样条映射器颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |
| <b>彩图</b> <i>灰度</i> | 应沿输入样条映射的输入灰度图像。 |
| <b>Height映射</b> <i>灰度</i> | 应沿输入样条映射的输入灰度高度图。 |
| <b>Twist Curve</b> <i>灰度</i> | 使用曲线第一行像素的值描述曲线的图像。<br>当<b>形状</b>参数设置为<i>半圆柱体</i>或<i>圆柱体</i>时，此输入用于控制形状周围的UV扭曲。 用<b>扭转UVs曲线乘数</b>参数控制其影响。<br>曲线为沿样条线的旋转量提供一个轮廓，行中的第一个像素是样条线开始处的旋转，最后一个像素是样条线结束处的旋转。 灰度值表示若干转弯。<br>您可以使用[曲线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)节点来创作曲线。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>颜色</b> <i>灰度</i> | 在输入样条之间映射输入彩色图像作为灰度图像的结果。 |
| <b>Height</b> <i>灰度</i> | 在输入样条上映射输入Height图像作为灰度图像的结果。 |
| <b>UV</b> <i>颜色</i> | 在彩色图像中编码的跨输入样条映射的UV（即坐标）。 |
| <b>ID</b> <i>灰度</i> | 沿输入样条映射的图像蒙版，其中白色值从一个样条向下一个样条递增1，以便可以独立选择每个形状。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>段数量</b> <i>整数</i> | 在图像坐标遍历样条之前，将样条简化为段。<br>段数量越多，沿曲线的映射就越平滑。 |
| <b>自动缩放UV</b> <i>布尔值</i> | 沿样条映射正方形图像时，自动调整坐标的比例以保留该图像。 |
| <b>UV 缩放</b> <i>浮点2</i> | 在X（水平）和Y（垂直）中调整映射坐标的比例。<br>值越高，拼贴图像的密度越大。 |
| <b>模式</b> <i>整数</i> | 选择图像应映射的样条的方法： <br>- <i>绘制样条列表</i>：使用输入列表中的所有样条；<br>- <i>绘制单样条</i>：仅使用具有指定索引的样条；<br>- <i>绘制样条范围</i>：仅使用索引包含在指定范围内的样条。 |
| <b>绘制样条索引</b> <i>整数</i> | （当“模式”设置为“绘制单样条”时可用）图像应映射到的样条的索引。 |
| <b>绘制样条范围</b> <i>整数2</i> | （当“模式”设置为“绘制样条范围”时可用）应沿其映射图像的样条索引范围。 |
| <b>开始</b> <i>浮动</i> | 偏移应映射的样条部分的起点。<br>该值表示样条的规范化长度。 |
| <b>结束</b> <i>浮动</i> | 偏移应映射的样条部分的终点。<br>该值表示样条的规范化长度。 |
| <b>Thickness模式</b> <i>整数</i> | 设置映射图像的Thickness的方法： <br>- <i>手动</i>：使用任意值显式设置Thickness；<br>- <i>来自样条</i>：使用样条的Thickness。 |
| <b>Thickness</b> <i>浮动</i> | （当“Thickness模式”设置为“手动”时可用）映射图像沿样条的Thickness的任意值。 |
| <b>Thickness乘数</b> <i>浮动</i> | （当“Thickness模式”设置为“来自样条”时可用）映射图像沿样条的Thickness的全局乘数，当该Thickness由样条驱动时。 |
| <b>形状</b> <i>整数</i> | 用于沿样条映射图像坐标的基本形状： <br>- <i>平面</i>：坐标映射到平面上；<br>- <i>半圆柱体</i>：坐标映射到基圆的轴沿样条方向的一个半圆柱体；<br>- <i>圆柱体</i>：坐标映射到基圆的轴沿样条方向的一个圆柱体。 |
| <b>柱面Height乘数</b> <i>浮动</i> | （当“形状”设置为“半圆柱体”或“圆柱体”时可用）圆柱体Height在Height输出中贡献的强度的乘数。<br>Height调整是累积的。 |
| <b>圆柱体Height偏移</b> <i>浮动</i> | （当“形状”设置为“半圆柱体”或“圆柱体”时可用）将圆柱体或半圆柱体形状轮廓的中心从样条曲面偏移到曲面下面的一个直径。 |
| <b>扭转UV强度</b> <i>浮动</i> | （当“形状”设置为“半圆柱体”或“圆柱体”时可用）围绕圆柱体的图像坐标的扭曲，以匝数为单位。<br>扭曲仅涉及在样条线的末端旋转圆柱体。 然后沿样条插入旋转。 |
| <b>扭转UV曲线乘数</b> <i>浮动</i> | （当“形状”设置为“半圆柱体”或“圆柱体”时可用）Twist Curve输入对圆柱体扭曲的贡献强度的乘数。<br>曲线为沿样条线的旋转量提供一个轮廓，行中的第一个像素是样条线开始处的旋转，最后一个像素是样条线结束处的旋转。 灰度值表示若干转弯。 |
| <b>扭转UV曲线偏移</b> <i>浮动</i> | （当“形状”设置为“半圆柱体”或“圆柱体”时可用）将全局偏移应用于Twist Curve提供的旋转值（轮次数）。 |
| <b>样条Height乘数</b> <i>浮动</i> | 调整样条Height输入对Height输出的贡献强度。<br>Height调整是累积的。 |
| <b>输入Height乘数</b> <i>浮动</i> | 调整高度图输入对Height输出的贡献强度。<br>Height调整是累积的。 |
| <b>非方形校正</b> <i>布尔值</i> | 调整点的位置和Thickness以保持样条形状的非方形分辨率。<br>这也会影响均匀分布。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-mapper-grayscale.resources/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-mapper-grayscale.resources/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-mapper-grayscale.resources/SplineMapperGrayscale-Demo.gif "节点示例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例3](spline-mapper-grayscale.resources/SplineMapperGrayscale-Variant1-After1.jpg "节点示例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
