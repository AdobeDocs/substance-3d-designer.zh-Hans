---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: 使用分形求和基节点生成基分形噪声图案，用于创建复杂的有机纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 分形求和基础
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# 分形求和基础

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![分形求和库 — 图标](fractal-sum-base.resources/fractal-sum-base-01.png "分形求和库 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一种可自定义的分形噪声，具有可调的范围和八度音阶平衡。

<b>分形求和</b>系列噪声均基于此节点。

另请参阅：[分形求和1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md)、[分形求和2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md)、[分形求和3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)、[分形求和4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>粗糙度</b> <i>浮动</i> | 噪声八度音量达到平衡。    值越大，显示的频率越高，八度音越明显。 |
| <b>分钟。 级别</b> <i>整数</i> | 噪声中使用的最小八度音阶。    值越大，噪声频率越高。 |
| <b>最大 级别</b> <i>整数</i> | 噪声中使用的最大八度音阶。    值越大，噪声频率越高。 |
| <b>无序</b> <i>浮动</i> | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b> <i>浮动</i> | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |
| <b>对比度</b> <i>浮动</i> | 最终结果的对比度。 |
| <b>全局不透明度</b> <i>浮动</i> | 噪声八度不透明度叠加在最终结果中。    较高的值可能导致某些区域被烧成白色。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![分形求和基数 — 示例1](fractal-sum-base.resources/fractal-sum-base-02.png "分形求和基数 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![分形求和基 — 示例2](fractal-sum-base.resources/fractal-sum-base-03.gif "分形求和基 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>
