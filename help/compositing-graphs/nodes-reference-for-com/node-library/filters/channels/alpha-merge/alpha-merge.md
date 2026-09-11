---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: 使用“Alpha合并”节点可将RGB纹理与Alpha通道相结合，以创建RGBA纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alpha合并
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# Alpha合并

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](alpha-merge.resources/rgb-a-merge.png)

<b>范围：</b>滤镜>通道

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将Alpha通道添加到没有Alpha通道的输入中。 不要与[RGBA合并](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)混淆，此节点更为简单，仅添加Alpha！

当您只是想要遮盖某些内容或您的结果需要Alpha时，可以使用简单但方便的节点。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>RGB</b> <i>颜色输入</i> | 不含Alpha的彩色图像 |
| <b>A</b> <i>灰度输入</i> | 用作结果Alpha的灰度图像。 |
