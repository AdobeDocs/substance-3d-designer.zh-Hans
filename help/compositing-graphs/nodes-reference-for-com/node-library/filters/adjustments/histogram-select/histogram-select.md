---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-select.html"
breadcrumb-title: ''
description: 使用直方图选择节点从纹理直方图中选择并提取特定范围以进行目标调整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方图选择
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---


# 直方图选择

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-select.resources/histogram-select.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

与[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)类似，此效果设置灰度值位置，并在其周围设置淡出范围。 可以调整对比度以使范围更清晰。

[单击此处观看关于直方图选择的Substance学院视频。](https://youtu.be/p9wcmJBFyGA?t=535)

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>位置</b> <i>0.0 - 1.0</i> | 设置进行范围选择的中间位置。 |
| <b>范围</b> <i>0.0 - 1.0</i> | 设置选择范围的宽度。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整结果的对比度/衰减。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-select.resources/histoselect-ex.gif" />
        </td>
    </tr>
</table>
