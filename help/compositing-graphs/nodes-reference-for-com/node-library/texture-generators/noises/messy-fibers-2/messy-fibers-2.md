---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-2.html"
breadcrumb-title: ''
description: 使用“杂乱纤维2”节点生成中间纤维图案，用于创建编织和纺织纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 杂乱纤维2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5a6c28b9acabf15714a1fd8bb4e7593192555fa2
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# 杂乱纤维2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![杂乱纤维2 — 图标](messy-fibers-2.resources/messy_fibers_2.png "杂乱纤维2 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>杂乱纤维</b>结构噪声的变化。

另请参阅：[杂乱纤维1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md)，[杂乱纤维3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 生成的杂色作为灰度位图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>缩放</b> <i>整数</i> | 使用网格细分生成噪声拼贴。    值越高，所绘制的拼贴就越多，噪音也越浓。 |
| <b>无序</b> <i>浮动</i> | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b> <i>浮动</i> | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |
| <b>无序各向异性</b> <i>浮动</i> | 控制<b>无序</b>参数应用的位移的方向跨度，值越高，方向越窄，定义越明确。    方向由<b>无序各向异性角</b>参数控制。 |
| <b>无序anisotropy angle</b> <i>浮动</i> | 当“无序位移”参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>角度</b> <i>浮动</i> | 用于设置螺纹方向的角度，以匝数为单位，从右下方开始。 |
| <b>角度随机</b> <i>浮动</i> | 应用于<b>角度</b>值的随机变化的最大值（轮次数）。 |
| <b>行号</b> <i>浮动</i> | 应用于基螺纹的拼贴量，值越高，螺纹越密集、越细。 |
| <b>拼贴偏移</b> <i>浮点2</i> | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![杂乱纤维2 — 示例1](messy-fibers-2.resources/messy_fibers_2_1.png "杂乱纤维2 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![杂乱纤维2 — 示例2](messy-fibers-2.resources/noise_messy_fibers_2_v2_speed0.1_aniso0.gif "杂乱纤维2 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![杂乱纤维2 — 示例3](messy-fibers-2.resources/noise_messy_fibers_2_v2_speed0.1_aniso1.gif "杂乱纤维2 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![杂乱纤维2 — 示例4](messy-fibers-2.resources/noise_messy_fibers_2_v2_speed0.1_aniso0.6.gif "杂乱纤维2 — 示例4"){zoomable="yes"}

</td>
</tr>
</table>
