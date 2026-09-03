---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: 使用HDR合并节点可以将多个HDR图像合并到单个全景图中，以创建复合环境图。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HDR 合并
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# HDR 合并

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge-01.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

合并多个摄影曝光以创建高动态范围图像。 第一个输入是公开最不足的图像。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入1-16</b> <i>颜色输入</i> | 输入图像。 可用数量取决于参数。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输入</b> <i>2 - 16</i> | 设定可用输入值。 |
| <b>曝光增量(EV)</b> <i>0.0 - 4.0</i> | 设置不同图像之间解释的曝光度差异。 |
| <b>白场</b> <i>0.0 - 13.0</i> | 设置白场以便对最终结果执行一些调整。 |
