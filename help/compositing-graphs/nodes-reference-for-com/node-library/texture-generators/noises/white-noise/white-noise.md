---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ""
description: 使用“白色噪声”节点生成白色噪声模式，以创建纹理变化和随机效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 白杂色
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 5%
---

# 白杂色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![白色噪声 — 图标](white-noise.resources/white_noise_v2.png "白色噪声 — 图标"){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用针对不同直方图形状的三种方法之一生成白色噪声：均匀、高斯和三角形。

</td>
</tr>
</table>

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 生成的灰度位图噪声。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>噪声分发</b> <i>整数</i> | 将食材分布到目标直方图形状的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>一致：</i>平面直方图。</li> <li data-preserve-html="true"><i>高斯：</i>表示正态分布的直方图，类似于钟形曲线。</li> <li data-preserve-html="true"><i>三角形：</i>三角形直方图。</li> </ul> |
| <b>无序</b> <i>Float</i> | 置换噪声的组成部分。    这可用于为噪声制作动画。 |
| <b>无序速度</b> <i>Float</i> | 调整<b>无序</b>参数应用的位移的距离。    在为噪声制作动画时，这可用于控制位移的速度。 |

## 示例

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="white-noise.resources/white_noise_v2_1.png" class="modal-image" alt="白色噪声 — 示例1" />
        </td>
        <td style="border: 0;">
            <img src="white-noise.resources/white_noise_v2_speed0.6_aniso0.gif" class="modal-image" alt="白噪声 — 示例2" />
        </td>
        <td style="border: 0;"></td>
    </tr>
</table>
