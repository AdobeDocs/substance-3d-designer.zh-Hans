---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: 使用“斜率模糊”节点可根据创建运动模糊的高度图斜率应用方向模糊效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜率模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# 斜率模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

执行高级、高质量模糊，其中各向异性/方向由灰度“斜率映射”驱动。 将其想象为遵循斜率映射的斜率的斜率模糊效果，就像它是Heightmap，类似于[定向翘曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)（它基于内部）。

这是Designer中最有趣、最强大的模糊之一。 它可用于实现一些非常有趣和意料之外的效果，如碎裂和风化边缘，或污迹和泄漏Dirt或铁锈。

重要提示：请确保使用适用于您的输入的版本！ 对彩色输入使用“斜率模糊”，对灰度输入使用“斜率模糊灰度”。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>斜率</b> <i>灰度输入</i> | 斜率映射到各向异性的驱动角度。 理想情况下，应包含倾斜渐变；严苛、锐利的过渡将无法很好地发挥作用！ |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>示例</b> <i>0 - 32</i> | 样本的数量会影响质量，但速度会受到影响。 |
| <b>强度</b> <i>0.0 - 16.0</i> | 模糊量或强度。 |
| <b>模式</b> <i>模糊，最小，最大</i> | 后续模糊刀路的混合模式。 “模糊”的行为更像标准[各向异性模糊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)，而“最小值”将“去除”现有区域，“最大值”将“去除”白色区域。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/slopeblur01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/slopeblur02.gif" />
        </td>
    </tr>
</table>
