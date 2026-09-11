---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: 使用3D单面噪声节点可生成3D单面噪声图案，用于创建平滑、自然的体积纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D单面噪声
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 5%

---


# 3D单面噪声

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-simplex-noise.resources/3d-simplex-noise.png){width="128px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将烘焙的位置映射插入输入插槽时生成程序化噪声。 它仅适用于GPU引擎。\
与[3D Perlin噪声](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)类似，但是对于性能和速度很重要的情况，它更快、更简单。

可以使用[Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers)作为输入而不是实际已烘焙贴图来测试此噪声（如下面的示例图像所示）。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>缩放</b> <i>0.0 - 64.0</i> | 设置效果的全局比例。 |
| <b>大小</b> <i>0.0 - 2.0</i> | 分别对X、Y和Z轴执行非均匀缩放。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-simplex-noise.resources/3d-simplex.gif" />
        </td>
    </tr>
</table>
