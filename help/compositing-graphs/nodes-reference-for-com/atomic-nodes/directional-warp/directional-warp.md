---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ''
description: 使用“方向变形”节点将方向扭曲应用于纹理，以创建流畅和运动效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 定向翘曲
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 9%

---


# 定向翘曲

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：方向变形](../../../../assets/comp_directionalwarp_1.png "原子节点：方向变形"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根据强度图在指定方向上置换像素，可能会产生变形效果。

以用户设置方向扭曲输入，并乘以用户设置强度图。 它的工作方式与“变形”类似，但只是朝着特定的方向进行。

</td>
</tr>
</table>

“变形”节点是一个相当简单但有用的节点，可以用作其他更高级效果的良好基础。 还有更高级的替代项，例如其他感兴趣的相关节点是[斜率模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)和[矢量变形](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)。

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

## 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>强度</b> *浮动* | 设置变形的强度。 |
| <b>变形角度</b> *浮动* | 设置变形效果的角度（以转角数为单位）。 |
| <b>输入筛选模式</b> *布尔值* | 控制是否使用最近或双线性滤波对<b>输入</b>进行采样。 |
| <b>强度图偏移</b> *浮动* | 此值从<b>强度输入</b>图像值中减去。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色*&#x200B;主要 | 应对其应用变形效果的灰度或彩色输入图像。 |
| <b>强度输入</b> *灰度* | 灰度图像，定义应应用于<b>输入</b>图像的变形量。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向变形 — 示例1](../../../../assets/dir-warp.gif "方向变形 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向变形 — 示例2](../../../../assets/dir-warp02.gif "方向变形 — 示例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向变形 — 示例3](../../../../assets/dir-warp03.gif "方向变形 — 示例3"){zoomable="yes"}

</td>
</tr>
</table>
