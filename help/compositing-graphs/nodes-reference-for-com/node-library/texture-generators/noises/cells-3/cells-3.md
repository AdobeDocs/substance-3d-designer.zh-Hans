---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: 使用细胞3节点生成用于创建有机和生物纹理效果的中间细胞图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 细胞3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 细胞3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![细胞3 — 图标](cells-3.resources/cells-3-01.png "细胞3 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>细胞</b>壁噪声的变化。

盘交叉产生具有不均匀柔软度的薄壁的单元。

另请参阅：[细胞1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、[细胞2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、[细胞4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>硬度</b> <i>浮动</i> | 单元格壁的定义，其中较高的值导致更清晰、清晰的壁。 |
| <b>反转</b> <i>布尔值</i> | 反转图像输出的灰度值。 |
| <b>无序</b> <i>浮动</i> | 替换噪点的成分。    这可用于为噪声设置动画。 |
| <b>无序速度</b> <i>浮动</i> | 调整<b>无序</b>参数应用的位移的距离。    这可用于在制作噪声动画时控制位移的速度。 |
| <b>无序各向异性</b> <i>浮动</i> | 控制<b>无序</b>参数应用的位移的方向跨度，值越高，方向越窄，定义越明确。    方向由<b>无序各向异性角</b>参数控制。 |
| <b>无序anisotropy angle</b> <i>浮动</i> | 当“无序位移”参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>图案大小</b> <i>浮点2</i> | 单元中散布的磁盘大小的乘数，其中1.0是单元的整个跨度。 |
| <b>图案缩放</b> <i>浮动</i> | <b>图案大小</b>的乘数，其中1.0为全尺寸。 |
| <b>角度</b> <i>浮动</i> | 用来设置磁盘方向的角度，以匝数为单位，从右水平方向开始。 |
| <b>角度随机</b> <i>浮动</i> | 应用于<b>角度</b>值的随机变化的最大值（轮次数）。 |
| <b>拼贴偏移</b> <i>浮点2</i> | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![细胞3 — 示例1](cells-3.resources/cells-3-02.png "细胞3 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![细胞3 — 示例2](cells-3.resources/cells-3-03.gif "细胞3 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![细胞3 — 示例3](cells-3.resources/cells-3-04.gif "细胞3 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![细胞3 — 示例4](cells-3.resources/cells-3-05.gif "细胞3 — 示例4"){zoomable="yes"}

</td>
</tr>
</table>
