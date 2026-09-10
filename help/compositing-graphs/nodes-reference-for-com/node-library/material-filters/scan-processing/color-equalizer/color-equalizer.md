---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: 使用Color Equalizer节点可平衡扫描素材中的颜色变化，以获得一致的纹理外观。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点的工作方式类似于高品质的[高反差保留](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)。 正常高反差移除饱和度并可能引入不需要的锐化程度，而Color Equalizer则适合使色差变得较平缓并以用户可选的尺度去除不需要的色调。

如果照片或扫描文档存在不需要的颜色差异或需要去除的色调，此功能将非常有用。 如果您已使用[高通](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)，则此节点应该感觉很熟悉。

蒙版选项用于移除非常特定的色调或仅用于特定值范围内的操作。 如果您认为效果过于宽泛，请使用这些选项。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色输入</i> |  |
| <b>蒙版输入</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 仅在“蒙版”设置为“输入”时处于活动状态。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输入平铺</b> <i>False/True</i> | （可选）保留边上的拼贴。 |
| <b>半径</b> <i>0.0 - 50.0</i> | 设置均衡半径。 较大的半径只能移除较大的色差。 这需要调整每个图像。 |
| <b>明亮/暗平衡</b> <i>0.0 - 1.0</i> | 用于保留或删除较暗色调的偏差设置。 |
| <b>自定颜色变化</b> <i>False/True</i> | 启用将效果更改为用户指定颜色的功能。 |
| <b>颜色变化</b> | 仅在启用“自定颜色变化”时处于活动状态。 设置允许您选择要均衡的色调偏移。 |
| <b>色相</b> <i>0.0 - 360.0</i> |  |
| <b>色度</b> <i>0.0 - 1.0</i> |  |
| <b>亮度</b> <i>0.0 - 1.0</i> |  |
| <b>蒙版源</b> <i>无，图像平均值，颜色参数，输入</i> | 设置是否应发生任何类型的蒙版。 颜色参数启用以下附加设置，输入切换到用户定义的蒙版输入。 |
| <b>蒙版</b> | 这仅在“颜色参数蒙版”中有效。 用于根据图像本身确定蒙版的其他蒙版参数。 下列参数允许您将色调精确转换为应用了均衡化的二进制蒙版。 请注意，使用这些设置时，“半径”参数的效果可能会变得不那么明显。 |
| <b>颜色</b> <i>（颜色值）</i> |  |
| <b>色相范围</b> <i>0.0 - 360.0</i> |  |
| <b>色度范围</b> <i>0.0 - 1.0</i> |  |
| <b>亮度范围</b> <i>0.0 - 1.0</i> |  |
| <b>模糊</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
