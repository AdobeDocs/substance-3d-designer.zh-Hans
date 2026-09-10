---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/bnw-spots-1.html"
breadcrumb-title: ''
description: 使用“BnW污点1”节点生成黑白斑点图案，用于创建纹理变化和细节蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > BnW spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BnW点1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# BnW点1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![BnW斑点1 — 图标](bnw-spots-1.resources/bnw_spots_1.png "BnW斑点1 — 图标"){width="200px"}

<b>在：</b>纹理生成器>杂色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

粗糙的<b>黑白(BnW)斑点</b>噪声的变体。

另请参阅： [BnW斑点2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md)、[BnW斑点3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-3/bnw-spots-3.md)

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
| <b>无序anisotropy angle</b> <i>浮动</i> | 当<b>无序位移</b>参数不为零时，控制<b>无序</b>参数应用的各向异性的方向。 |
| <b>粗糙度</b> <i>浮动</i> | 平衡八度噪声，较高的值将使较高的八度频率更加明显。 |
| <b>拼贴偏移</b> <i>浮点2</i> | 控制用于渲染杂色的无限平面部分的位置。 |
| <b>非方形扩展</b> <i>布尔值</i> | 在非方形图像中，保持生成的拼贴方形，并将杂色生成扩展到图像边界。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnW斑点1 — 示例1](bnw-spots-1.resources/bnw_spots_1_1.png "BnW斑点1 — 示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnW斑点1 — 示例2](bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.6_aniso0.gif "BnW斑点1 — 示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnW斑点1 — 示例3](bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.6_aniso1.gif "BnW斑点1 — 示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnW斑点1 — 示例4](bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.3_aniso0.6.gif "BnW斑点1 — 示例4"){zoomable="yes"}

</td>
</tr>
</table>
