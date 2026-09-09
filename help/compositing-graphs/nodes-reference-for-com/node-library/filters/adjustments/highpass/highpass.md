---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: 使用“高通”节点从纹理中提取高频细节，用于创建锐化和细节增强效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高通
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# 高通

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](highpass.resources/high-pass-greyscale.png){width="128px"}

![](highpass.resources/high-pass.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

执行高反差滤镜，既可用于彩色版本，也可用于灰度版本。 与具有相同名称的Photoshop操作类似。\
可用于移除图像中的大明亮度差异，例如在清理纹理以拼贴时。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“高反差保留”，对灰度输入使用“高反差保留灰度”。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>半径</b> <i>0.0 - 64.0</i> | 滤镜半径：较小的半径可移除较小的差异，较大的半径可移除较大的区域。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-example.png" />
        </td>
    </tr>
</table>
