---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: 使用“锐化”节点来增强纹理细节和边缘，以创建清晰、定义的表面细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 锐化
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# 锐化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![锐化节点图标](sharpen.resources/sharpen-4.png "锐化节点图标")

<b>在：</b>个原子节点中

</td>
<td style="border: 0;" valign="top">

## 描述

锐化节点对输入执行锐化操作。 它是对图像应用最后锐化修饰的有用节点。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="sharpen.resources/sharpen-tooltip.gif" alt="锐化工具提示" /></div>

从数学上讲，它与Photoshop的“USM锐化”非常相似，尽管名称不同。 对于基色图之类的效果很好，但在法线图和金属图等地图上应避免使用它。

## 输入

<b>输入</b> *彩色/灰度*（主要）\
应锐化的图像。

## 参数

<b>强度</b> *浮动*\
设置锐化效果的强度。

<b>穿透Alpha</b> *布尔值*（当彩色图像连接到<b>输入</b>时可用）\
确定应锐化图像的Alpha通道还是应保持其不变。

## 示例

![锐化节点 — 示例1](sharpen.resources/sharpen-ex.png "锐化节点 — 示例1")
