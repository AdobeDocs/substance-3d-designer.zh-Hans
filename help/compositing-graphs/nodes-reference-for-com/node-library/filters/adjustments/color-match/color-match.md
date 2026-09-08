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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# 颜色匹配

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## 颜色匹配

**范围：** *滤镜/调整*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

尝试将定义的&#x200B;*源颜色*&#x200B;范围与&#x200B;*目标颜色*&#x200B;范围匹配，并且支持输入槽来定义源和目标。

有关更简单的版本，请参阅[替换颜色范围](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md)或[替换颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)。

## 参数

### 输入

* **输入**： *颜色*&#x200B;输入\
  要修改结果的主输入。
* **源颜色**： *颜色输入*\
  源颜色的输入槽，仅在“源颜色模式”设置为&#x200B;*输入*&#x200B;时使用。
* **目标颜色**： *颜色输入*&#x200B;目标颜色的输入槽，仅在“目标颜色模式”设置为&#x200B;*输入*&#x200B;时使用。

### 参数

* **源颜色模式**： *平均，参数，输入*&#x200B;设置源颜色是通过平均输入图像、通过设置参数还是使用输入插槽定义的。
* **源颜色**： *（颜色值）*&#x200B;如果源颜色模式设置为*参数*，则此参数确定源颜色。
* **目标颜色模式**： *参数，图像输入*&#x200B;设置源颜色是通过平均输入图像、设置参数还是使用输入插槽定义的。
* **目标颜色**： *（颜色值）*&#x200B;如果“目标颜色模式”设置为*参数*，则此参数确定目标颜色。
* **自定义颜色变量**： False/True\
  启用其他颜色变化。
* **颜色变化**\
  设置结果的色相、色度或明亮度变化（如果已启用）。
* **使用蒙版**： *False/True*\
  根据下面的“蒙版模式”，切换“蒙版输入”或“输出”的使用。
* **蒙版模式**： *参数，输入*&#x200B;参数模式输出一个蒙版，其中详细说明了颜色的更改方式。 输入模式启用蒙版以控制色彩匹配效果的强度。
* **蒙版**\
  输出一个蒙版，其中显示确切应用“颜色匹配”效果的位置，并包含其他用于平滑和模糊生成的蒙版的控件。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
