---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: 使用“环境遮蔽”(RTAO)节点，从Height地图生成实时的环境遮蔽地图，以实现逼真的着色。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境遮蔽(RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 环境遮蔽(RTAO)

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RTAO节点图标](../../../../../../assets/rt-ao.png "RTAO节点图标")

<b>进入：</b> *滤镜/效果*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

基于遮蔽映射输入生成环境Height映射。

与HBAO相比，该滤波器计算结果更精确，但由于计算时间的原因，不能与CPU (SSE)引擎结合使用。

请参阅[环境遮蔽(HBAO)（滤镜节点）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md)以获取更快、更简单的替代方案。

</td>
</tr>
</table>

## 参数

<b>使用物理尺寸</b> *布尔值*\
切换以使用物理尺寸设置来确定Height比例。

<b>物理尺寸</b> *浮点3* （在<b>使用物理尺寸</b>设置为&#x200B;*True*&#x200B;时可用）\
根据表面的真实物理尺寸调整Height比例

<b>示例&#x200B;</b>*整数*\
用于计算环境遮蔽的光线数。\
较高的值会以牺牲性能为代价，提供更平滑、更精确的结果。

<b>Height比例</b> *浮动* （在<b>使用物理尺寸</b>设置为&#x200B;*False*&#x200B;时可用）\
Height映射输入强度的乘数。

<b>分布</b> *整数*&#x200B;设置分布方法。 影响阴影区域的衰减，

<b>最大距离</b> *浮动*\
设置光线可传播以被遮挡的最大距离。

<b>扩散角</b> *浮动*\
设置要拍摄的光线的扩散角度。 值1表示整个半球。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RTAO节点 — 示例1](../../../../../../assets/image2021-6-18-11-7-48.png "RTAO节点 — 示例1")

</td>
<td style="border: 0;" valign="top">

![RTAO节点 — 示例2](../../../../../../assets/image2021-6-18-11-9-0-1.png "RTAO节点 — 示例2")

</td>
</tr>
</table>
