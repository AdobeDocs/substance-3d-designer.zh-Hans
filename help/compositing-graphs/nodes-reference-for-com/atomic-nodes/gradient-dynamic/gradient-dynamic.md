---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: 使用“渐变（动态）”节点创建可由输入参数和值控制的动态渐变。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渐变（动态）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# 渐变（动态）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：渐变动态](../../../../assets/comp_dyngradient_1.png "原子节点：渐变动态"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

使用另一图像中某行或某列像素生成的渐变，重新映射图像的灰度值。

它可以作为渐变节点的细微替代品，但与“渐变”节点不同，“渐变”颜色键不是在内部定义的，而是来自外部输入。

</td>
</tr>
</table>

这主要可以避免由于颜色参数移动到节点外部而导致参数无法公开的问题。 这就是它的“动态性”所在。

虽然渐变（动态）本身并不是很难使用的节点，但其用例更加先进：大多数标准用例可以由常规渐变节点覆盖。

当您受到渐变编辑器的关键系统的过度限制，并且希望颜色和渐变位置由图表的其他输入、参数和部分驱动时，此节点即会发挥作用。

或者，可以使用渐变输入位置滑块在单个渐变输入中存储的多个渐变之间切换。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 参数

</td>
<td style="border: 0;" valign="top">

### 输入连接器

</td>
<td style="border: 0;" valign="top">

### 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>渐变寻址</b> *布尔值* | 设置渐变是重复（拼贴）还是固定。   此参数确定如何处理灰度输入的[0， 1]范围之外的HDR像素：最多可夹持或折叠[0， 1]。 |
| <b>渐变方向</b> *整数* | 设置应沿其对“渐变输入”进行采样的轴：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>水平：</i>在X轴上取样一行像素。</li> <li data-preserve-html="true"><i>垂直：</i>对Y轴上的像素列进行取样。</li> </ul> |
| <b>渐变输入位置</b> *浮动* | 要在“渐变输入”中取样的像素的行或列的规范化位置。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>灰度输入</b> *灰度*&#x200B;主要 | 要重新映射的灰度图像。 |
| <b>渐变输入</b> *彩色/灰度* | 渐变将从此图像中取样 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *彩色/灰度* |  |

## 示例

*即将推出。*
