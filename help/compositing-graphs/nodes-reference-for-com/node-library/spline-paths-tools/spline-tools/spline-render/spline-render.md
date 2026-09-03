---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: 使用样条渲染节点将样条渲染为具有可自定义宽度、颜色和混合模式的纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# 样条渲染

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-render.resources/spline-render-01.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在输入<b>Background</b>上沿输入<b>样条</b>绘制段字符串。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>背景</b> <i>灰度</i> | 应在其上绘制样条的灰度图像。 |
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 在背景上绘制输入样条的结果图像。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>模式</b> <i>整数</i> | 选择应绘制哪些样条的方法： <br>- <i>绘制样条列表</i>：绘制输入列表中的所有样条；<br>- <i>绘制单样条</i>：仅从输入列表中绘制指定的样条；<br>- <i>绘制样条范围</i>：仅从输入列表中绘制指定范围内的样条。 |
| <b>绘制样条索引</b> <i>整数</i> | （当“模式”设置为“绘制单样条”时可用）应绘制的样条的索引。 |
| <b>绘制样条范围</b> <i>整数2</i> | （当“模式”设置为“绘制样条范围”时可用）应绘制的样条索引范围。 |
| <b>显示方向帮助程序</b> <i>布尔值</i> | 对于每个样条，在样条的起始处绘制一个点，在其终止处绘制一个箭头。 |
| <b>段数量</b> <i>整数</i> | 调整沿样条绘制的段数。<br>值越高，线条越平滑。 |
| <b>包络样条量</b> <i>整数</i> | 应沿每个样条的Thickness绘制的重复段数。 |
| <b>开始</b> <i>浮动</i> | 偏移应绘制的样条部分的起点。<br>该值表示样条的规范化长度。 |
| <b>结束</b> <i>浮动</i> | 偏移应绘制的样条部分的终点。<br>该值表示样条的规范化长度。 |
| <b>Thickness大小模式</b> <i>整数</i> | 计算绘制段Thickness的方法： <br>- <i>图像</i>：该值在纹理空间中规范化，其中1是图像的全宽。 Thickness相对于纹理分辨率；<br>- <i>像素</i>：该值是纹理中的绝对像素数，其中1是整像素。 Thickness与纹理分辨率是分开的。 |
| <b>Thickness（图像）</b> <i>浮动</i> | （当“Thickness大小模式”设置为“图像”时可用）在纹理空间中标准化的绘制段的Thickness，其中1是图像的全宽。 |
| <b>Thickness（像素）</b> <i>浮动</i> | （当“Thickness大小模式”设置为“像素”时可用）绘制线段的Thickness作为纹理中的绝对像素数，其中1表示完全像素。 |
| <b>启用接头</b> <i>布尔值</i> | 使用磁盘填充沿样条绘制的单个段之间的间隙。 |
| <b>非方形校正</b> <i>布尔值</i> | 调整点的位置和Thickness以保持样条形状的非方形分辨率。<br>这也会影响均匀分布。 |
| <b>颜色</b> |  |
| <b>背景强度</b> <i>浮动</i> | 该值与“背景”输入图像相乘。 |
| <b>样条样式</b> <i>整数</i> | 用于为样条着色的方法：<br>- <i>纯色</i>：使用统一的灰度值绘制段；<br>- <i>渐变</i>：沿每个段字符串从头到尾应用从黑到白的渐变；<br>- <i>Height</i>：样条的Height用作绘制段的灰度值。 |
| <b>样条颜色</b> <i>浮动</i> | 用于绘制线段的统一灰度值。<br>选择“纯色”以外的样条样式时，此颜色将乘以样式的颜色。 |
| <b>随机明亮度</b> <i>浮动</i> | 对于样条中每个未剪切的段字符串，将指定范围内的随机偏移应用于用于绘制该字符串的灰度值。 |
| <b>混合模式</b> <i>整数</i> | 沿样条绘制的背景和重叠段的颜色混合方法： <br>- <i>最大值</i>：使用最亮值；<br>- <i>相加</i>：将这些值相加。 |
| <b>随机段</b> |  |
| <b>随机段开始</b> <i>浮动</i> | 调整段串离样条起始点更近的被切割概率。 |
| <b>随机段结束</b> <i>浮动</i> | 调整接近样条端点的线段串被剪切的概率。 |
| <b>随机偏移</b> <i>浮动</i> | 设置沿每个切削段的法线应用的最大位移量。<br>当Start和End都设置为0时，此参数不起作用。 |
| <b>随机偏移中心</b> <i>浮动</i> | 沿每个剪切段的法线偏移应用于其随机位移的中心。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-02.jpg" alt="SplineRender-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-03.jpg" alt="SplineRender-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-04.jpg" alt="SplineRender-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-05.jpg" alt="SplineRender-Variant1-After">
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
      <img src="spline-render.resources/spline-render-04.jpg" alt="SplineRender-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-06.jpg" alt="SplineRender-Variant3">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例1](spline-render.resources/spline-render-07.gif "节点示例1")

</td>
</tr>
</table>
