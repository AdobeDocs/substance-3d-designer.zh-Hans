---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ""
description: 使用“变形”节点将扭曲效果应用于纹理，以创建变形和位移效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 变形
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 9%
---

# 变形

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![原子节点：变形](warp.resources/comp_warp_1.png "原子节点：变形"){width="100%"}

<b>在：</b>个原子节点中

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

根据从单独的渐变输入计算出的斜率来置换输入图像中的像素值，从而导致变形。

与“方向变形”不同，此节点会朝着由“渐变输入”的斜率或渐变定义的方向均匀地推离白色区域。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="warp.resources/warp-tooltip.gif" alt="变形工具提示" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

在处理节点时可能会有些棘手，因为效果在很大程度上取决于渐变输入：对渐变进行较小的微调可以使用相同的强度值产生巨大的视觉差异。 确保尝试使用“Gradient Input”（渐变输入）的“Contrast”（对比度）、“Luminance”（明亮度）和“Scale”（缩放），以及这个节点上的“Intensity”（强度）滑块。

如果您熟悉法线图，则可以想象此节点的操作类似于将渐变输入转换为[法线图](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)，然后沿法线图矢量定义的方向扭曲基本输入。 事实上，使用[矢量变形](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)也可以实现同样的效果。 在[斜率模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)中也可以找到类似的效果。



## 参数

|  |  |
| --- | --- |
| <b>强度</b> *浮动* | 设置变形的强度。 |
| <b>输入筛选模式</b> *布尔值* | 控制是使用最接近还是筛选对输入内容进行取样。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色*&#x200B;主要 | 彩色或灰度图像。 |
| <b>渐变输入</b> *灰度* | 灰度输入图像的渐变斜率决定了输出图像中的变形效果。 |


## 示例

*即将推出。*
