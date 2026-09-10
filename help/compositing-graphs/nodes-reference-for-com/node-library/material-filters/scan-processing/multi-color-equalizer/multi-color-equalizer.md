---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: 使用“多Color Equalizer”节点可在多个Texture通道之间均衡颜色，以实现一致的扫描材料处理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# 多Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-color-equalizer.resources/color-equalizer-multi.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这是[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)的多输入版本。 它可以平衡色差，并以用户可选的比例去除不需要的色调。 它主要用于多角度照片，然后与[多角度至反照率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)或[多角度至法线](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)组合。

>[!NOTE]
>
> 有关详细信息，请参阅原始的[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入1-8</b> <i>颜色输入</i> | 要处理的多个输入。 |
| <b>蒙版输入</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输入计数</b> <i>1 - 8</i> | 设置要并行处理的输入数。 |
| <b>输入平铺</b> <i>False/True</i> | （可选）保留边上的拼贴。 |
| <b>半径</b> <i>0.0 - 50.0</i> | 设置均衡半径。 较大的半径只能移除较大的色差。 这需要调整每个图像。 |
| <b>明亮/暗平衡</b> <i>0.0 - 1.0</i> | 用于保留或删除较暗色调的偏差设置。 |
| <b>自定颜色变化</b> <i>False/True</i> | 允许您将效果更改为用户指定的颜色。 |
| <b>颜色变化</b> | 仅在启用“自定颜色变化”时处于活动状态。 设置允许您选择要均衡的色调偏移。 |
| <b>色相</b> <i>0.0 - 360.0</i> |  |
| <b>色度</b> <i>0.0 - 1.0</i> |  |
| <b>亮度</b> <i>0.0 - 1.0</i> |  |
| <b>蒙版源</b> <i>无，图像平均值，颜色参数，输入</i> | 设置是否应进行任何蒙版。 颜色参数启用下面的其他设置，输入切换到用户定义的蒙版输入。 |
| <b>蒙版</b> | 仅在使用颜色参数蒙版时有效。 包含用于根据图像本身确定蒙版的其他蒙版参数。 以下参数允许您将色调精确转换为应用了均衡的二进制蒙版。 请注意，使用这些设置时，“半径”参数的效果可能会变得不那么明显。 |
| <b>颜色</b> <i>（颜色值）</i> |  |
| <b>色相范围</b> <i>0.0 - 360.0</i> |  |
| <b>色度范围</b> <i>0.0 - 1.0</i> |  |
| <b>亮度范围</b> <i>0.0 - 1.0</i> |  |
| <b>模糊</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
