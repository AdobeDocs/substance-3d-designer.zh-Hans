---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: 使用“各向异性模糊”节点应用方向模糊效果以创建运动模糊和条纹效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 各向异性模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# 各向异性模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

执行高品质的[方向模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)，只需一些设置即可自定义外观。 也称为“运动模糊”。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“各向异性模糊”，对灰度输入使用“各向异性模糊灰度”。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>0.0 - 16.0</i> | 模糊的强度（半径）。 此值越高，模糊效果越明显。 |
| <b>各向异性</b> <i>0.0 - 1.0</i> | 模糊的方向性。 将此值设置为0.0与执行常规模糊相同。 |
| <b>角度</b> <i>0.0 - 1.0</i> | 设置模糊方向的角度。 |
| <b>质量</b> <i>0 - 1</i> | 在内部在[框模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)和HQ模糊之间切换。 以速度换取质量。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
