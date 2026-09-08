---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: 使用油漆磨损节点可根据网格几何生成油漆磨损蒙版，以创建逼真的油漆碎裂效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 油漆磨损
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# 油漆磨损

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示油漆在边缘处脱落和磨损。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>曲率</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>变体蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>级别</b> <i>0.0 - 1.0</i> | 设置油漆磨损的总量，逐渐显现。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整结果的对比度。 |
| <b>遮蔽</b> <i>0.0 - 1.0</i> | 设置烘焙的AO对防止较暗区域磨损的作用量。 |
| <b>半径</b> <i>0.0 - 2.0</i> | 设置碎屑效果与凸形边缘的距离。 |
| <b>变体</b> <i>0.0 - 1.0</i> | 设置要混合到效果中的变化量(污渍)。 |
| <b>覆盖变体蒙版</b> <i>False/True</i> | 启用自定义变化(污渍)映射输入槽。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/paint-wear-ex.gif" />
        </td>
    </tr>
</table>
