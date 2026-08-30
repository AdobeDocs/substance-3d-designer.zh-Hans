---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: 使用“颜色匹配”节点来匹配纹理之间的颜色，以创建一致的调色板并协调纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 颜色匹配
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# 颜色匹配

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-match.resources/color-match-3.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

尝试将定义的&#x200B;*源颜色*&#x200B;范围与&#x200B;*目标颜色*&#x200B;范围匹配，并且支持输入槽来定义源和目标。

有关更简单的版本，请参阅[替换颜色范围](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md)或[替换颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色输入</i> | 要修改结果的主输入。 |
| <b>源颜色</b> <i>颜色输入</i> | 源颜色的输入槽，仅在“源颜色模式”设置为&#x200B;*输入*&#x200B;时使用。 |
| <b>目标颜色</b> <i>颜色输入</i> | 目标颜色的输入槽，仅在“目标颜色模式”设置为&#x200B;*输入*&#x200B;时使用。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>源颜色模式</b> <i>平均值，参数，输入</i> | 设置是通过平均输入图像、通过设置参数还是通过使用输入插槽来定义源颜色。 |
| <b>源颜色</b> <i>（颜色值）</i> | 如果“源颜色模式”设置为&#x200B;*参数*，则此参数确定源颜色。 |
| <b>目标颜色模式</b> <i>参数，图像输入</i> | 设置是通过平均输入图像、设置参数还是使用输入插槽来定义源颜色。 |
| <b>目标颜色</b> <i>（颜色值）</i> | 如果“目标颜色模式”设置为&#x200B;*参数*，则此参数确定目标颜色。 |
| <b>自定颜色变化</b> <i>False/True</i> | 启用其他颜色变化。 |
| <b>颜色变化</b> | 在启用时为结果设置色相、色度或明亮度变化。 |
| <b>使用蒙版</b> <i>False/True</i> | 根据下面的“蒙版模式”，切换“蒙版输入”或“输出”的使用。 |
| <b>蒙版模式</b> <i>参数，输入</i> | 参数模式输出一个蒙版，其中详细说明了颜色是如何变化的。 输入模式允许蒙版控制色彩匹配效果的强度。 |
| <b>蒙版</b> | 输出一个蒙版，其中显示确切应用“颜色匹配”效果的位置，并包含其他用于平滑和模糊生成的蒙版的控件。 |
