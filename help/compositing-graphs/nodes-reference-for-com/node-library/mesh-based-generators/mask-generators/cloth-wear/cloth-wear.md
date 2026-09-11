---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: 根据网格曲率和接触区域，使用布料磨损节点在布料表面生成磨损蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 布料磨损
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# 布料磨损

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cloth-wear.resources/cloth-wear.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

蒙版表示布料上的模糊边缘。 它使用布料细节高度图来确定大多数外观；如果没有适当的地图，效果看起来非常基本。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>布料Height</b> <i>灰度输入</i> | 仅Height布料图案。 这不是您（烘焙）对象的Height，而是拼贴细节图案。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>曲率</b> <i>灰度输入</i> | 烘焙/生成的曲率用于确定凸边。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>硬边数量</b> <i>0.0 - 1.0</i> |  |
| <b>柔和度</b> <i>0.0 - 5.0</i> | 确定磨损边缘的模糊/柔和程度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cloth-wear.resources/cloth-wear-ex.gif" />
        </td>
    </tr>
</table>
