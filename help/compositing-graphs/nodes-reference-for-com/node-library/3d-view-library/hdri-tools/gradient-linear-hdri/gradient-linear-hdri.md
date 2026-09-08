---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: 使用渐变线性HDRI节点可在HDRI环境中为自定义光照设置创建线性渐变。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渐变线性(HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# 渐变线性(HDRI)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/gradient-linear.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

创建一个位于中心且包含用户放置点的线性渐变。 与常规[渐变线性1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)不同，最终结果会针对球面投影进行调整。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>点位置</b> | 用于确定渐变方向的点的位置。 |
| <b>顶部颜色</b> <i>（颜色值）</i> | 渐变顶部的颜色（在点处） |
| <b>底色</b> <i>（颜色值）</i> | 渐变底部颜色（远离点）。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整结果的对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/gradient-ex1.gif" />
        </td>
    </tr>
</table>
