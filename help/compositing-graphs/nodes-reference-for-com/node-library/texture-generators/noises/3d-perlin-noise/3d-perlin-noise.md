---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: 使用3D Perlin噪声节点在3D空间中生成平滑的Perlin噪声图案，用于创建自然外观的体积纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin噪声
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# 3D Perlin噪声

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise.resources/3dperlinnoise.png){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>3D Perlin噪声</b>节点基于<b>位置映射</b>输入在3D空间中生成Perlin噪声。

此节点可以使用[Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

</td>
</tr>
</table>

>[!WARNING]
>
> 此噪声仅适用于<i>GPU引擎</i>（即<b>Direct3D</b>或<b>OpenGL</b>）。 转到<b>工具>切换引擎...</b>或按<b>F9</b>键以选择所需的引擎。

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>反转</b> <i>布尔值</i> | 反转输出图像。 |
| <b>缩放</b> <i>Float</i> | 控制3D Perlin噪声的比例。 |
| <b>大小</b> <i>Float3</i> | 控制<b>X</b>、<b>Y</b>和<b>Z</b>轴中的3D Perlin噪声的大小。 值不一致会产生<i>拉伸或挤压</i>效果。 |
| <b>偏移</b> <i>Float3</i> | 将偏移应用于<b>X</b>、<b>Y</b>和<b>Z</b>轴中的3D Perlin噪声的<i>位置</i>。 |
| <b>扭曲强度</b> <i>Float</i> | 控制应用于3D Perlin噪声的<i>变形效果</i>的强度。 |
| <b>扭曲比例乘数</b> <i>浮动</i> | 控制变形效果中使用的<i>变形图案</i>的比例，该比例由<b>扭曲强度</b>控制。 |
| <b>基线</b> <i>浮动</i> | 将<i>偏移</i>应用于3D Perlin杂色值分布的基线<i>明亮度</i>值。 |
| <b>对比度</b> <i>浮动</i> | 调整3D Perlin噪声的对比度。 |
| <b>绝对</b> <i>布尔值</i> | 使用3D Perlin噪声中的绝对值。 这实际上<i>反转</i>低于0.5</i>的值<i>的值分布。 |
| <b>启用拼贴</b> <i>布尔值</i> | 调整3D Perlin噪声，使其生成的图案<i>在X、Y和Z轴中重复</i>。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlin.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant.jpg" />
        </td>
    </tr>
</table>
