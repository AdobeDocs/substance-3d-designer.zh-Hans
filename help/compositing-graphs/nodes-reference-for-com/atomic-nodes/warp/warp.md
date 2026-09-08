---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: 使用“变形”节点将扭曲效果应用于纹理，以创建变形和位移效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 变形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---


# 变形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：变形](../../../../assets/comp_warp_1.png "原子节点：变形"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根据从单独的渐变输入计算出的斜率来置换输入图像中的像素值，从而导致变形。

与定向翘曲不同，此节点会按照由“渐变输入”的斜率或渐变定义的方向均匀地推离白色区域。

</td>
</tr>
</table>

在处理节点时可能会有些棘手，因为效果在很大程度上取决于渐变输入：对渐变进行较小的微调可以使用相同的强度值产生巨大的视觉差异。 确保尝试使用“Gradient Input”（渐变输入）的“Contrast”（对比度）、“明亮度”和“Scale”（缩放），以及这个节点上的“Intensity”（强度）滑块。

如果您熟悉法线图，则可以想象此节点的操作类似于将渐变输入转换为[法线图](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)，然后沿法线图矢量定义的方向扭曲基本输入。 事实上，使用[矢量变形](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)也可以实现同样的效果。 在[斜率模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)中也可以找到类似的效果。

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
| <b>强度</b> *Float* | 设置变形的强度。 |
| <b>输入筛选模式</b> *布尔值* | 控制是使用最接近还是筛选对输入内容进行取样。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色*&#x200B;主要 | 颜色或灰度图像。 |
| <b>渐变输入</b> *灰度* | 灰度输入图像的渐变斜率决定了输出图像中的变形效果。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

*即将推出。*
