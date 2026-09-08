---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: 利用“选择性Dirt”节点，根据Dirt几何形状生成选择性网格累积蒙版，用于逼真风化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 可选Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 8%

---


# 可选Dirt

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)蒙版表示凸形边缘上的简单Dirt效果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>曲率</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>变体蒙版</b> <i>灰度输入</i> | 可选的变体映射，可通过参数启用。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>级别</b> <i>0.0 - 1.0</i> | 设置效果的总级别，逐渐显示出来。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整结果的对比度。 |
| <b>变体</b> <i>0.0 - 1.0</i> | 设置要混合到效果中的变化/污渍量。 |
| <b>覆盖变体蒙版</b> <i>False/True</i> | 允许用自定义输入插槽覆盖变化。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/selective-dirt-ex.gif" />
        </td>
    </tr>
</table>
