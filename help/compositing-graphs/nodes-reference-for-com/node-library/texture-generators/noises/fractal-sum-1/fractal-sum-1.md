---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-1.html"
breadcrumb-title: ''
description: 使用“分形求和1”节点，通过求和多个八度音阶来生成精细纹理，从而生成分形噪点图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 分形求和1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# 分形求和1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![分形求和1 — 图标](../../../../../../assets/fractal_sum_1.png "分形求和1 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>分形求和</b>噪声的变化。

另请参阅：[分形求和库](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md)、[分形求和2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md)、[分形求和3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)、[分形求和4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>无序</b> <i>浮动</i> | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b> <i>浮动</i> | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![分形求和1 — 示例1](../../../../../../assets/fractal_sum_1_1.png "分形求和1 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![分形求和1 — 示例2](../../../../../../assets/noise_fractal_sum_1_v2_speed0.6_aniso0.gif "分形求和1 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>
