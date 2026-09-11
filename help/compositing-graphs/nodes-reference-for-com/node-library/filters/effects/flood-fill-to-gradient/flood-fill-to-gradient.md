---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: 使用“Flood Fill到渐变”节点，用渐变值填充区域，以创建平滑的颜色过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渐变Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# 渐变Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/floodfill-to-gradient.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)基转换为（随机方向）渐变。 对于创建拼贴随机倾斜和倾斜的高度图非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>颜色输入</i> | 基本Flood Fill数据。 |
| <b>角度输入</b> <i>灰度输入</i> | 可选映射，用于确定每个单元格与外部映射的角度。 |
| <b>输入斜率</b> <i>灰度输入</i> | 用于确定每个单元格渐变强度的可选映射。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>角度</b> <i>0.0 - 1.0</i> | 为所有拼贴设置统一的全局角度/方向。 |
| <b>角度变化</b> <i>0.0 - 1.0</i> | 分别随机选择每个拼贴的角度。 这是最有用且最强大的参数！ |
| <b>乘以定界框大小</b> <i>0.0 - 1.0</i> | 根据拼贴的单个定界框大小缩放整个线性效果。 这意味着较小的拼贴最终会比较大的拼贴暗。 |
| <b>角度图像输入乘数</b> <i>0.0 - 1.0</i> | 设置可选的“角度”输入图对生成的渐变方向的影响 |
| <b>图像输入乘数</b>斜率 <i>0.0 - 1.0</i> | 设置可选斜率输入映射对生成的渐变斜率强度的影响。 |
| <b>乘以斜率强度</b> <i>0.0 - 1.0</i> |  |
| <b>平面斜率颜色</b> <i>（灰度值）</i> | 允许为平整斜率设置实心值。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex1.png" />
        </td>
    </tr>
</table>
