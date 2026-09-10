---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: 使用样条流映射器节点沿样条路径创建流动的纹理图案以获得有机效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条流映射器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# 样条流映射器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-flow-mapper.resources/spline-flow-mapper-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

绘制流图，其中流矢量数据是沿着输入样条绘制的。

这样，您就可以使用样条控制流动的方向、轨迹、强度和Thickness，以及使用渐变斜坡将绘制的数据淡入中性背景。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 当使用极低的Thickness值时，结果可能包括样条包络外的不期望伪像。 这是一个已知问题。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |
| <b>衰减剖面曲线</b> <i>灰度</i> | <span id="_Hlk135812146"></span>使用曲线第一行像素值描述曲线的图像。 当衰减配置文件参数设置为“输入配置文件曲线”时，此输入用于控制沿样条绘制的流矢量数据的衰减的渐变斜坡。<br>您可以使用[曲线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)节点来创作曲线。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>颜色</i> | 以彩色图像编码的输出流图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>段数量</b> <i>整数</i> | 在矢量流数据遍历样条之前，样条被简化为段。 段数越多，沿曲线绘制的流图就越平滑。 |
| <b>模式</b> <i>整数</i> | 选择绘制矢量流数据的样条的方法：<br><br>-<i>绘制样条列表</i>：使用输入列表中的所有样条；<br>-<i>绘制单样条</i>：只使用具有指定索引的样条；<br>-<i>绘制样条范围</i>：只使用索引包含在指定范围内的样条。 |
| <b>绘制样条索引</b> <i>整数</i>（在“模式”设置为“绘制单样条”时可用） | 绘制矢量流数据时所应遵循的样条的索引。 |
| <b>绘制样条范围</b> <i>整数2</i>（在“模式”设置为“绘制样条范围”时可用） | 用于绘制矢量流数据的样条的索引范围。 |
| <b>Thickness模式</b> <i>整数</i> | 设置绘制的矢量流数据Thickness<br><br>- <i>手动</i>的方法：使用任意值显式设置Thickness；<br>- <i>来自样条</i>：使用样条的Thickness。 |
| <b>Thickness</b> <i>Float</i>（在“Thickness模式”设置为“手动”时可用） | 沿样条绘制的矢量流数据的Thickness的任意值。 |
| <b>Thickness乘数</b> <i>Float</i>（在“Thickness模式”设置为“来自样条”时可用） | 一个全局乘数，用于Thickness沿样条绘制的矢量流数据，当该Thickness由样条驱动时。 |
| <b>方向</b> <i>整数</i> | 矢量流相对于样条线的方向。<br><br>- <i>正切</i>：使用样条的正切矢量；<br>- <i>法向</i>：使用样条法向矢量；<br>- <i>法向镜像</i>：使用样条法向矢量的镜像版本。 |
| <b>翻转方向</b> <i>布尔值</i> | 反转样条方向，这也会影响流矢量的方向。 |
| <b>衰减配置文件</b> <i>整数</i> | 用于绘制沿样条绘制的流矢量数据的衰减的渐变斜坡：<br><br>-<i>线性</i>：使用线性渐变斜坡；<br>-<i>高斯</i>：使用高斯渐变斜坡<br>-<i>输入轮廓曲线</i>：使用为衰减轮廓曲线输入提供的曲线作为渐变斜坡。 |
| <b>开始衰减</b> <i>布尔值</i> | <span id="_Hlk135769398"></span>在样条线的开头添加一个半圆。 半圆采用与样条相同的衰减。 |
| <b>结束衰减</b> <i>布尔值</i> | 在样条末端添加一个半圆。 半圆采用与样条相同的衰减。 |
| <b>样条Height衰减</b> <i>浮动</i> | 沿样条绘制的流矢量数据的强度与样条的Height相乘，其中绘制的数据随着Height越接近0而渐隐为背景的中性(0.5， 0.5， 0)颜色。 |
| <b>非方形校正</b> <i>布尔值</i> | 调整点的位置和Thickness以保持样条形状的非方形分辨率。 这也会影响均匀分布。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-flow-mapper.resources/SplineFlowMapper-Demo.gif "节点示例2")

</td>
</tr>
</table>
