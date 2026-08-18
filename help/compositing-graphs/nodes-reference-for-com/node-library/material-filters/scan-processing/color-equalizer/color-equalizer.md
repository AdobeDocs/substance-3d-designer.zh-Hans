---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**在：** *材质筛选器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点的工作方式类似于高品质的[高反差保留](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)。 正常高反差移除饱和度并可能引入不需要的锐化程度，而Color Equalizer则适合使色差变得较平缓并以用户可选的尺度去除不需要的色调。

如果照片或扫描文档存在不需要的颜色差异或需要去除的色调，此功能将非常有用。 如果您已使用[高通](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)，则此节点应该感觉很熟悉。

蒙版选项用于移除非常特定的色调或仅用于特定值范围内的操作。 如果您认为效果过于宽泛，请使用这些选项。

## 参数

### 输入

* **输入**： *颜色输入*
* **蒙版输入**：*灰度输入*\
  用于遮盖节点效果的遮罩槽。 仅在“蒙版”设置为“输入”时处于活动状态。

### 参数

* **输入拼贴**： *False/True*&#x200B;选择性地保留边缘上的拼贴。
* **半径**： *0.0 - 50.0*&#x200B;设置均衡半径。 较大的半径只能移除较大的色差。 这需要调整每个图像。
* **明亮/暗平衡**： *0.0 - 1.0*&#x200B;用于保留或移除较暗色调的偏差设置。
* **自定义颜色变化**： *False/True*&#x200B;允许将效果更改为用户指定的颜色。
* **颜色变化**\
  仅在启用“自定颜色变化”时处于活动状态。 设置允许您选择要均衡的色调偏移。
  * **色相**： *0.0 - 360.0*
  * **色度**： *0.0 - 1.0*
  * **亮度**： *0.0 - 1.0*
* **蒙版源**： *无，图像平均值，颜色参数，输入*&#x200B;设置是否应发生任何类型的蒙版。 颜色参数启用以下附加设置，输入切换到用户定义的蒙版输入。
* **蒙版**\
  这仅在“颜色参数蒙版”中有效。 用于根据图像本身确定蒙版的其他蒙版参数。 下列参数允许您将色调精确转换为应用了均衡化的二进制蒙版。 请注意，使用这些设置时，“半径”参数的效果可能会变得不那么明显。
  * **颜色**： *（颜色值）*
  * **色相范围**： *0.0 - 360.0*
  * **色度范围**： *0.0 - 1.0*
  * **亮度范围**： *0.0 - 1.0*
  * **模糊**： *0.0 - 2.0*
  * **Smoothness**： *0.0 - 2.0*

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
