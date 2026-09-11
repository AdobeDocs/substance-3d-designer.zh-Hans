---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: 使用边缘检测节点检测纹理的边缘，以创建轮廓和基于边缘的蒙版效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘检测
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# 边缘检测

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

检测黑白图像中的对比度，然后创建黑白蒙版以突出显示对比度。

适用于需要边缘某种蒙版的许多情况。 请记住，它最适合用于高对比度输入；如果需要，在传递到此节点之前调整对比度。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>边缘宽度</b> <i>1.0 - 16.0</i> | 边缘周围检测到的区域的宽度。 |
| <b>边缘圆度</b> <i>0.0 - 16.0</i> | 对生成的蒙版进行圆化、模糊和平滑处理。 |
| <b>反转</b> <i>False/True</i> | 反转结果。 |
| <b>容差</b> <i>0.0 - 1.0</i> | 用于显示边的容差阈值因子。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-ex.png" />
        </td>
    </tr>
</table>
