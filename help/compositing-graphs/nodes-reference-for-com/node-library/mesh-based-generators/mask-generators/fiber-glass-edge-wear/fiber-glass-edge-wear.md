---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: 利用纤维玻璃Edge Wear节点，根据网格曲率生成玻璃纤维边缘的磨损蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 玻璃纤维Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 6%

---


# 玻璃纤维Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

表示专门用于玻璃纤维类型的衣服的蒙版，可能用于布料。 由于纤维非常平铺、重复的特性，可以任选地启用三平面混合。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰度输入</i> | 用于边缘突出显示的已烘焙贴图。 必填！ |
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于遮盖被遮盖区域的已烘焙贴图。 不需要，但绝对推荐。 |
| <b>污渍输入</b> <i>灰度输入</i> | 可选的自定义插槽以覆盖光纤模式。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>世界空间正常</b> <i>颜色输入</i> | 仅用于三平面。 |
| <b>位置</b> <i>颜色输入</i> | 仅用于三平面。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>磨损级别</b> <i>0.0 - 1.0</i> | 像[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)一样，逐步显示磨损情况。 |
| <b>佩戴对比度</b> <i>0.0 - 1.0</i> | 设置总效果对比度。 |
| <b>边缘Smoothness</b> <i>0.0 - 16.0</i> | 设置高亮边缘的出血/模糊。 |
| <b>污渍量</b> <i>0.0 - 1.0</i> | 设置要在边缘之间混合多少纤维效果。 结合磨损程度对此进行调整，以获得最大程度的控制。 |
| <b>Ambient occlusion蒙版</b> <i>0.0 - 1.0</i> | 设置AO对隐藏效果的影响量。 |
| <b>弯曲粗细</b> <i>0.0 - 1.0</i> | 设置弯曲凸边的影响量。 |
| <b>使用自定义污渍</b> <i>False/True</i> | 用自定义映射覆盖内置光纤。 |
| <b>使用三平面</b> <i>False/True</i> | 启用[三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)以隐藏接缝。 |
| <b>三平面混合对比度</b> <i>0.0 - 1.0</i> | 控制三平面效果的对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/fiber-glass-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
