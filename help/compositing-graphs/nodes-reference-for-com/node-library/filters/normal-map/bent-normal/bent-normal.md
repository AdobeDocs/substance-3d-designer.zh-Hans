---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: 使用“弯曲法线”节点生成考虑ambient occlusion和间接光照的弯曲法线图。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弯曲法线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# 弯曲法线

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![弯曲正常节点图标](../../../../../../assets/rt-bent-normal.png "弯曲正常节点图标")

<b>进入：</b> *筛选器/法线图*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

根据高度图输入生成弯曲法线图。 弯曲法线图是[正常](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)和[Ambient occlusion(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)的特殊版本，生成具有嵌入ambient occlusion的法线图。\
这可用于实时引擎，以将Ambient occlusion烘焙到正常映射中，例如，使金属上的遮蔽反射更准确。

由于计算时间，不应将此节点与CPU (SSE)引擎结合使用。

</td>
</tr>
</table>

## 参数

<b>使用物理尺寸</b> *布尔值*\
切换以使用物理尺寸设置来确定Height比例。

<b>物理尺寸</b> *Float3* （在<b>使用物理尺寸</b>设置为&#x200B;*True*&#x200B;时可用）\
根据曲面的真实物理尺寸调整Height比例。

<b>示例</b> *整数*\
用于计算弯曲法线的射线数。\
“较高”能够以牺牲性能为代价，提供更流畅、更精确的结果。

<b>Height比例</b> *Float（当“使用物理尺寸”设置为False时可用）*\
高度图输入强度的乘数。

<b>分发</b> *整数*\
设置分布方法。 影响向阴影区域的衰减。

<b>最大距离</b> *Float*\
设置光线可传播以被遮挡的最大距离。

<b>扩散角度</b> *Float*\
设置要拍摄的光线的扩散角度。 值1表示整个半球。

<b>正常格式</b> *整数*\
反转输出的绿色通道。

## 示例图像

![弯曲正常节点 — 示例1](../../../../../../assets/bent-normal-ex-1.jpg "弯曲正常节点 — 示例1")
