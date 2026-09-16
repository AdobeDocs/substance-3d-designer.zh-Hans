---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/curve.html"
breadcrumb-title: ""
description: 使用“曲线”节点可通过可自定义的曲线调整纹理值，以实现精确的颜色和亮度控制。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Curve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲线
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 2%
---

# 曲线

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：曲线](curve.resources/comp_curve_1.png "原子节点：曲线")

</td>
<td style="border: 0;" valign="top">

使用自定义曲线重新映射图像中的值。

该节点提供了到图像色调重新映射的界面，类似于其他2D图像编辑应用程序。 用户可以放置点并调整贝塞尔曲线以重新映射输入，可以是灰度或彩色。当与渐变过渡一起使用以将其重新映射到特定Height配置文件时，该功能特别有用，它允许对斜面配置文件等进行非常精确的建模。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="curve.resources/curve-tooltip.gif" alt="曲线工具提示" /></div>

与大多数其他节点不同，“曲线”节点不具有带有滑块和参数的典型标准界面，而是提供成熟的曲线编辑器。 有关如何使用它的信息，请参阅下面可展开的部分。

[但是，这确实意味着Curve子图中的所有参数都不能向Node公开](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)。 此处的唯一选项是使用[多开关](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)在不同的曲线配置文件之间切换。



## 参数

|  |  |
| --- | --- |
| <b>应用/公开曲线</b> *布尔值* | 允许将用户曲线复制到输出，而不是将其应用于输入图像 |
| <b>曲线寻址</b> *布尔值* | 此参数确定如何处理输入中[0， 1]范围之外的HDR像素：最多可夹持或折叠[0， 1]。 |
| <b>曲线</b> *曲线键数组* | 用于映射输入灰度值的自定曲线。   可以使用[曲线编辑器](#curve-editor)进行编辑。 |

## 曲线编辑器

### 创建和移动点

要创建点，只需双击“曲线”视图上的任意位置：

![](curve.resources/createmovepoint.gif)

### 控制点影响

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

为了得到精确的结果，曲线节点为每个点提供了不同的模式：

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](curve.resources/image2017-2-17-14-5-36.png)

</td>
</tr>
</table>

![](curve.resources/image2017-2-17-14-13-27.png)将点模式重置为默认值。

![](curve.resources/image2017-2-17-14-12-6.png)锁定/解锁2个贝塞尔曲线处理程序，以便用户可以一起或独立移动它们。

![](curve.resources/image2017-2-17-14-14-0.png)点的两侧由贝塞尔曲线处理程序控制。

![](curve.resources/image2017-2-17-14-16-22.png)点的右侧由贝塞尔曲线处理程序控制，而左侧保持平坦。

![](curve.resources/image2017-2-17-14-18-25.png)点的左侧由贝塞尔曲线处理程序控制，而右侧保持平坦。

![](curve.resources/image2017-2-17-14-19-32.png)点边保持平坦

![](curve.resources/curvepointsmodes.gif)

### 显示输入直方图

只需单击![](curve.resources/image2017-2-17-14-50-13.png)，即可显示/隐藏输入的直方图

![](curve.resources/image2017-2-17-14-48-35.png)

### 单独控制每个通道（颜色输入）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

当输入颜色节点时，您可以调整每个通道的曲线：

只需在右上方的下拉菜单中选择要调整的曲线：

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](curve.resources/image2017-2-17-14-52-43.png)

</td>
</tr>
</table>

在“RGB曲线”模式下，可以通过按/按![](curve.resources/image2017-2-17-14-55-0.png)来隐藏/显示各个通道曲线：

![](curve.resources/image2017-2-17-14-55-38.png)

### 对齐、镜像和翻转

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

如果右键单击曲线视图，将会显示更多选项。

<b>顶部对齐：</b>将所选点与最高的点水平对齐。

<b>居中对齐：</b>将所选点水平对齐到选区的平均Height。

<b>下对齐：</b>将所选点与最低点水平对齐。

</td>
<td width="50.00%" style="border: 0;" valign="top">

![](curve.resources/image2017-6-27-16-11-9.png)

</td>
</tr>
</table>

<b>水平/垂直分布：</b>在所选轴上分布点

<b>水平/垂直翻转：</b>根据所选轴翻转所选点。

<b>水平/垂直镜像：</b>根据所选轴镜像整个曲线

### 键盘快捷键

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>LMB +拖动</b>

绘制一个选择框。

</td>
<td style="border: 0;" valign="top">

![](curve.resources/ctrl.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>按住Shift并拖动</b>

限制在X轴或Y轴上移动。

</td>
<td style="border: 0;" valign="top">

![](curve.resources/shift.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Alt + LMB +拖动</b>

暂时断开手柄可单独移动它们。

</td>
<td style="border: 0;" valign="top">

![](curve.resources/altclick.gif)

</td>
</tr>
</table>

### 调整曲线的构图

调整处理程序时，您可能会遇到一个处理程序越过曲线视图的情况。

在这种情况下，可以使用![](curve.resources/image2017-2-20-19-11-53.png)按钮使大小适合内容。

![](curve.resources/image2017-2-20-19-12-45.png)按钮将缩放级别重置为1

![](curve.resources/viewzoom.gif)

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色*&#x200B;主要 | 要处理的图像。 |


## 示例

*即将推出。*
