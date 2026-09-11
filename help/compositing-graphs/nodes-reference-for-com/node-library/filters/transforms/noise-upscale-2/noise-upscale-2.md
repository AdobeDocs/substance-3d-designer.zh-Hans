---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: 使用“噪声放大2”纹理，通过基于噪声的插值放大节点，以保持较大尺寸的纹理质量。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪声放大2
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 6%

---


# 噪声放大2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-2.resources/noise-upscale.png){width="128px"}

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

程序化获取输入噪声并将其放大到双分辨率，保留细节但不会引入过多的拼贴。 使用“X”类型的蒙版并以比原始输入更低对比度进行混合（内部混合模式为“最大”和“最小”）。

此节点主要用于优化使用重型、大噪声的慢图形。 它允许您使用更高的分辨率，而不会引入过多的额外计算时间。

另请参阅[噪声放大1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md)和[噪声放大3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md)，了解此过程的不同变化。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>偏移1X</b> <i>0.0 - 1.0</i> | 在X轴上滑动顶部和底部。 |
| <b>偏移1Y</b> <i>0.0 - 1.0</i> | 在Y轴上滑动顶部和底部。 |
| <b>偏移2X</b> <i>0.0 - 1.0</i> | 在X轴上滑动左右部件。 |
| <b>偏移2年</b> <i>0.0 - 1.0</i> | 在Y轴上滑动左右部分。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-2.resources/noise2ex.png" />
        </td>
    </tr>
</table>
