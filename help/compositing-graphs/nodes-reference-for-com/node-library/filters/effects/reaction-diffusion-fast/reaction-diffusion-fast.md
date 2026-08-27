---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: 使用“反应扩散”快速节点，使用程序纹理的快速反应 — 扩散算法生成有机图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 快速反应扩散
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# 快速反应扩散

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![反应扩散节点图标](../../../../../../assets/reaction-diffusion.png "反应扩散节点图标")

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点对输入灰度图像执行反应 — 扩散效果。

反应 — 扩散是物质扩散（扩散）并与其他物质相互作用（反应）的过程。 它是一种数学模型，可以模拟自然界中某些图案在动物皮肤上形成时会发生什么。

此节点已针对性能进行了优化，并且确实在速度方面做出了一些精确的权衡。

</td>
</tr>
</table>

## 输入连接器

<b>输入</b> *灰度*&#x200B;应用反应扩散效果的灰度图像。

## 输出连接器

<b>输出&#x200B;</b>*灰度*&#x200B;表示应用于输入图像的反应扩散效果的灰度图像。

## 参数

<b>半径</b> *浮动*&#x200B;效果应扩散的距离。

<b>对比度</b> *浮动*\
调整输入内容的对比度，有点像是主动变更。

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![示例1](../../../../../../assets/reactdiff03.png "示例1")

</td>
<td style="border: 0;" valign="top">

![示例2](../../../../../../assets/reactdiff02.png "示例2")

</td>
<td style="border: 0;" valign="top">

![示例3](../../../../../../assets/reactdiff01.gif "示例3")

</td>
</tr>
</table>
