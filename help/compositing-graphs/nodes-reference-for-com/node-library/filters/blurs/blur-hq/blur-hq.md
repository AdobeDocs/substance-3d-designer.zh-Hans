---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: 使用“Blur HQ”（模糊HQ）纹理将高品质模糊效果应用到照片中，打造专业水准的模糊效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 模糊 HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# 模糊 HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-1.png){width="128px"}

![](blur-hq.resources/blur-hq-grayscale.png){width="128px"}

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对结果执行“高品质高斯模糊”。 质量比[标准原子盒模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [好得多。](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“模糊总部”，对灰度输入使用“模糊总部”。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>0.0 - 16.0</i> | 模糊的强度（半径）。 此值越高，模糊效果越明显。 |
| <b>质量</b> <i>0 - 1</i> | 以较低的计算速度增加内部采样量可获得更高的品质。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/hqblur-example.gif" />
        </td>
    </tr>
</table>
