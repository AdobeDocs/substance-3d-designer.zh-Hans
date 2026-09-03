---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: 使用“Flood Fill到灰度”节点，用灰度颜色填充连接的区域，以创建单色图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill为GrayscaleColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Flood Fill为灰度/彩色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/flood-fill-to-grayscale-color-01.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/flood-fill-to-grayscale-color-02.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用Flood Fill数据生成灰度或颜色值色板。 与[Flood Fill到随机灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)不同，这两个节点允许更好地控制设置确切的变化和色调，并具有额外的输入图来确定要基于每个单元格进行随机化的基值。

它是一个功能强大的系统，可以为每个细胞提供独特的价值或颜色，同时仍然保持控制，并以预先确定的输入为基础。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>颜色输入</i> |  |
| <b>灰度/彩色输入</b> <i>灰度/彩色输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>明亮度/色彩调整</b> <i>-1.0 - 1.0</i> | 设置节点的偏差或基值。 当使用灰度或彩色输入时，这用于将初始值更改为一个起点。 |
| <b>明亮度/颜色随机</b> <i>-1.0 - 1.0</i> | 设置变化量。 |
