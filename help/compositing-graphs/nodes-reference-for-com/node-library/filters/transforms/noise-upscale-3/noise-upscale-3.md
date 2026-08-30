---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: 使用噪声Upscale 3纹理，使用基于噪声的高级算法来放大节点，以便在更高分辨率下保留细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 噪声放大3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# 噪声放大3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-3.resources/noise-upscale.png){width="128px"}

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

程序化获取输入噪声并将其放大到双分辨率，保留细节但不会引入过多的拼贴。 使用用户定义的蒙版在噪声原始比例之上混合颜色。

此节点主要用于优化使用重型、大噪声的慢图形。 它允许您使用更高的分辨率，而不会引入过多的额外计算时间。

另请参阅[噪声放大1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md)和[噪声放大2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)，在大多数情况下，它们往往在隐藏拼贴方面稍好一些。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>灰度</b> <i>灰度输入</i> | 目标噪声图像。 |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-3.resources/noise3ex.png" />
        </td>
    </tr>
</table>
