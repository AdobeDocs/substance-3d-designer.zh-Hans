---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: 使用“形状描边”节点为形状添加描边轮廓，以创建边框和边缘效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状描边
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# 形状描边

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-stroke.png){width="128px"}

![](../../../../../../assets/shape-stroke-grayscale.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

按照您从其他2D图像编辑应用程序中可能熟悉的方式，在黑白色蒙版（适用于灰度版本）或带Alpha 通道（适用于彩色版本）的形状周围添加描边或轮廓。 可以看作[边缘检测](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)的更完整版本。

适用于各种图像编辑效果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>宽度</b> <i>-1.0 - 1.0</i> | 描边效果的宽度。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 效果的全球不透明度。 |
| <b>（轮廓）颜色</b> <i>（颜色值）</i> | 用于轮廓效果的颜色。 |
| <b>蒙版颜色</b> <i>（颜色值）（仅限灰度版本）</i> | 用于透明度映射输出的纯色。 |
| <b>输入已预乘</b> <i>False/True（仅限颜色版本）</i> | 是否应假设输入为预乘。 |
| <b>预乘输出</b> <i>False/True</i> | 是否应预乘输出。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shapestroke-ex.png" />
        </td>
    </tr>
</table>
