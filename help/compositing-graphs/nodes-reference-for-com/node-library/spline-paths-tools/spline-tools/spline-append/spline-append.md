---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: 使用“样条附加”节点将多个样条附加在一起，以创建更长的连续路径。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 添加样条
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# 添加样条

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-append.resources/spline-append-01.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

样条被打包为列表。 此节点将输入样条（设置#2）列表附加到现有列表（设置#1）上。

列表的顺序保持不变，意味着将列表D-E-F附加到列表A-B-C时将生成列表A-B-C-D-E-F。

</td>
</tr>
</table>

>[!TIP]
>
> 请注意附加样条的顺序，因为其他节点（如[样条散点](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md)、[样条桥](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md)节点等）中也会考虑此顺序。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>预览#1</b> <i>灰度</i> | 第一组输入样条作为灰度图像的预览。 |
| <b>样条#1坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的第一组输入样条点的坐标。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条#1数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的第一组输入样条的附加数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条#1量</b> <i>整数</i> | 第一组输入样条的数量。 |
| <b>预览#2</b> <i>灰度</i> | 第二组输入样条作为灰度图像的预览。 |
| <b>样条#2坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的第二组输入样条点的坐标。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条#2数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的第二组输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条#2量</b> <i>整数</i> | 第二组输入样条的数量。 |

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
| <b>反向样条#1方向</b> <i>布尔值</i> | 反转第一组中样条的方向。 |
| <b>反向样条#2方向</b> <i>布尔值</i> | 反转第二组中样条的方向。 |
| <b>预览</b> |  |
| <b>段数量</b> <i>整数</i> | 调整用于在“预览”输出中绘制样条可视化效果的段数。 值越高，线条越平滑。 |
| <b>显示方向帮助程序</b> <i>布尔值</i> | 在“预览”输出中，在样条的起始处显示一个点，在其结尾处显示一个箭头。 |
| <b>显示Thickness信封</b> <i>布尔值</i> | 在样条Thickness的边显示附加线。 |
| <b>Thickness（像素）</b> <i>浮动</i> | 调整预览输出中样条可视化的Thickness（以像素为单位）。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](spline-append.resources/spline-append-02.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-append.resources/spline-append-03.jpg "节点示例2")

</td>
</tr>
</table>

![节点演示](spline-append.resources/spline-append-04.gif "节点演示")
