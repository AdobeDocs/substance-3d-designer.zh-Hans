---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: 使用“明亮度高通”节点从纹理中提取高频明亮度细节，以增强表面细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 明亮度高通
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# 明亮度高通

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

通过对输入的明亮度值执行[高通](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)来取消光照信息。 修复包含光照信息的拍摄纹理时有用。 可在[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中使用多个通道进行组合，以消除不同频率的光照细节。

与[光照取消低频](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)相比，在保留颜色方面效果稍好。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>半径</b> <i>0.0 - 64.0</i> | 高通效果的半径。 较小的半径会取消较小的光照，请调整以匹配输入图像。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/luminance-highpass-example.png" />
        </td>
    </tr>
</table>
