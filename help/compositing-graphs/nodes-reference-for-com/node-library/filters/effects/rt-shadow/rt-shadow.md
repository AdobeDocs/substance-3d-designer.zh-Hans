---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: 使用“RT阴影”节点计算来自几何的实时阴影信息，以创建动态光照效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT阴影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# RT阴影

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RT阴影节点图标](../../../../../../assets/rt-shadow.png "RT阴影节点图标")

<b>进入：</b> *滤镜/效果*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

从Height映射输入生成光线跟踪阴影。

由于计算时间的原因，不应将此节点与CPU (SSE)引擎结合使用。

</td>
</tr>
</table>

## 参数

<b>示例</b> *整数*\
用于计算阴影的光线数。\
值越高，结果越平滑和精确，但会降低性能。

<b>模式</b> *整数*\
在曲面上绘制阴影的方法。

<b>Height缩放</b> *浮动*\
输入Height映射强度的乘数。

<b>光源位置&#x200B;</b>*浮点2*\
围绕曲面的球面上的光源位置：
* <b>X</b>：水平位置，匝数；
* <b>Y</b>：垂直位置，其中0.5表示顶点，0/1表示地平线。

<b>光照强度</b> *浮动*\
光源的强度。

<b>光源大小</b> *浮点2* （在<b>模式</b>设置为&#x200B;*阴影*&#x200B;时可用）\
作为矩形的光源大小。

<b>光度（柔和阴影）</b> *浮动*\
<b>光线大小</b>对光线方向的贡献的乘数。\
值越高，阴影越平滑。

<b>保持光照在水平线之上</b> *布尔值*\
如果<b>光照位置</b>的设置方式将光线放置在地平线以下，则此参数可防止光线越过该阈值，这意味着Y值会被固定在[0；1]范围内。

<b>阴影不透明度</b> *浮动*\
在表面上绘制的阴影不透明度的乘数。

<b>阴影衰减</b> *浮动*\
阴影距离主光栅越远，衰减的乘数。\
值为0时将产生均匀的阴影（仍然应用柔和的阴影）。

<b>最大阴影长度</b> *浮动*\
阴影可从其光栅绘制的最大距离。\
值为0时不会产生可见阴影。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RT阴影节点 — 示例1](../../../../../../assets/RTShadows-01.jpg "RT阴影节点 — 示例1")

</td>
<td style="border: 0;" valign="top">

![RT阴影节点 — 示例2](../../../../../../assets/RTShadows-02.jpg "RT阴影节点 — 示例2")

</td>
<td style="border: 0;" valign="top">

![RT阴影节点 — 示例3](../../../../../../assets/RTShadows-03.jpg "RT阴影节点 — 示例3")

</td>
</tr>
</table>
