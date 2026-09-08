---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: 使用“反应漫射快速”节点，针对程序化的纹理使用快速反应漫射算法生成有机模式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 反应漫射快速
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# 反应漫射快速

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![反应漫射节点图标](../../../../../../assets/reaction-diffusion.png "反应漫射节点图标")

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点对输入灰度图像执行反应漫射效果。

反应漫射是物质扩散（扩散）并与其他物质相互作用（反应）的过程。 它是一种数学模型，可以模拟自然界中某些图案在动物皮肤上形成时会发生什么。

此节点已针对性能进行了优化，并且确实在速度方面做出了一些精确的权衡。

</td>
</tr>
</table>

## 输入连接器

<b>输入</b> *灰度*&#x200B;应应用反应漫射效果的灰度图像。

## 输出连接器

<b>输出&#x200B;</b>*灰度*&#x200B;表示应用于输入图像的反应漫射效果的灰度图像。

## 参数

<b>半径</b> *Float*&#x200B;效果应传播多远。

<b>对比度</b> *Float*\
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
