---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: 在最终渲染之前，使用“曝光度预览”节点预览HDRI环境中的曝光度调整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曝光度预览
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# 曝光度预览

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/exposure-preview-01.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

用于预览曝光步骤的助手节点。 用户设置最小值和最大值，节点将使用原始输入的公开版本生成一个大得多的图像。 不同版本总是水平栈叠，数量取决于节点或图形的分辨率。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>最大曝光度(EV)</b> <i>-8.0 - 8.0</i> | 顶部的最大曝光度，最亮的图像。 |
| <b>分钟曝光(EV)</b> <i>-8.0 - 8.0</i> | 最低限度的底部曝光度，最暗的图像。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exposure-preview-02.png" />
        </td>
    </tr>
</table>
