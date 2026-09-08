---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: 使用“多Color Equalizer”节点可在多个纹理通道之间实现色彩均化，以便进行一致的扫描材料处理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# 多Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## 多Color Equalizer

**位置：** *材质过滤器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

这是[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)的多输入版本。 它可以平衡色差，并以用户可选的比例去除不需要的色调。 它主要用于多角度照片，然后与[多角度至反照率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)或[多角度至法线](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)组合。

>[!NOTE]
>
> 有关详细信息，请参阅原始的[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)。

## 参数

### 输入

* **输入1-8**： *颜色输入*&#x200B;要处理的多个输入。
* **蒙版输入**：*灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **输入计数**： *1 - 8*&#x200B;设置并行处理的输入数。
* **输入平铺**： *False/True*&#x200B;可选择保留边缘的拼贴。
* **半径**： *0.0 - 50.0*&#x200B;设置均衡半径。 较大的半径只能移除较大的色差。 这需要调整每个图像。
* **明亮/暗平衡**： *0.0 - 1.0*&#x200B;用于保留或移除较暗色调的偏差设置。
* **自定颜色变化**： *False/True*&#x200B;允许您将效果更改为用户指定的颜色。
* **颜色变化**\
  仅在启用“自定颜色变化”时处于活动状态。 设置允许您选择要均衡的色调偏移。
  * **色相**： *0.0 - 360.0*
  * **色度**： *0.0 - 1.0*
  * **亮度**： *0.0 - 1.0*
* **蒙版源**： *无，图像平均值，颜色参数，输入*&#x200B;设置是否应进行任何蒙版。 颜色参数启用下面的其他设置，输入切换到用户定义的蒙版输入。
* **蒙版**\
  仅在使用颜色参数蒙版时有效。 包含用于根据图像本身确定蒙版的其他蒙版参数。 以下参数允许您将色调精确转换为应用了均衡的二进制蒙版。 请注意，使用这些设置时，“半径”参数的效果可能会变得不那么明显。
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
