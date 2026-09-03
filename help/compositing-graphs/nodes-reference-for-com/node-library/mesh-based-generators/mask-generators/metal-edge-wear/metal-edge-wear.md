---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: 使用“金属Edge Wear”节点，根据网格曲率和位置在金属边上生成磨损蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金属Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# 金属Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear-01.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示金属对象上的边缘磨损，凸起的凸起边缘上出现划痕和碎片，可能会被烘焙的AO暗区遮盖。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>污渍输入</b> <i>灰度输入</i> |  |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>世界空间正常</b> <i>颜色输入</i> |  |
| <b>位置</b> <i>颜色输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>磨损级别</b> <i>0.0 - 1.0</i> | 设置总磨损量，逐渐显现。 |
| <b>佩戴对比度</b> <i>0.0 - 1.0</i> | 设置最终结果的对比度。 |
| <b>边缘Smoothness</b> <i>0.0 - 16.0</i> | 设置从弯曲边缘衰减的Smoothness。 |
| <b>污渍量</b> <i>0.0 - 1.0</i> | 设置要在边缘之间混合的污渍量。 |
| <b>污渍比例</b> <i>1 - 16</i> | 设置污渍的比例。 |
| <b>Ambient occlusion蒙版</b> <i>0.0 - 1.0</i> | 设置AO对最终效果（暗区被遮盖）的影响量。 |
| <b>弯曲粗细</b> <i>0.0 - 1.0</i> | 设置弯曲的凸边对最终效果的作用量。 |
| <b>使用自定义污渍</b> <i>False/True</i> | 启用自定义污渍映射输入槽。 |
| <b>使用三平面</b> <i>False/True</i> | 启用[Tri 平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)投影以隐藏接缝。 |
| <b>三平面混合对比度</b> <i>0.0 - 1.0</i> | 设置三平面投影的混合对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-02.gif" />
        </td>
    </tr>
</table>
