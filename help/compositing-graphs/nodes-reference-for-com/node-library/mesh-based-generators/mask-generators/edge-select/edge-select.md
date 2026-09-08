---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: 使用“Edge Select”（边缘选择）网格生成蒙版，选择节点边缘创建基于边缘的风化磨损效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 边缘选择
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# 边缘选择

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白色蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版是根据弯曲选择任何边缘类型的最佳方法。 凸的、凹的、任何层级或对比度都可以隔离，这提供了绝佳的快捷键，可以避免通过[层节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)手动执行此操作。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>弯曲</b> <i>灰度输入</i> | 用于加亮边的已烘焙贴图。 必填！ |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>级别</b> <i>0.0 - 1.0</i> | 为“凸的”和“凹的”设置边加亮的总量。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整“凸的”和“凹的”高光对比度。 |
| <b>凸的</b> |  |
| <b>凸边缘宽度</b> <i>0.0 - 1.0</i> | 设置凸边加亮的宽度。 请记住，略微增加“柔和度”会导致边缘变细。 |
| <b>凸软度</b> <i>0.0 - 1.0</i> | 为凸形边缘设置过渡的柔和度。 |
| <b>凸强度</b> <i>0.0 - 1.0</i> | 设置凸边的“边”加亮的最大强度。 设置为0将不突出显示。 |
| <b>凹形</b> |  |
| <b>凹边宽度</b> <i>0.0 - 1.0</i> | 为“凹边”设置加亮的宽度。 请记住，略微增加“柔和度”会导致边缘变细。 |
| <b>凹形柔和度</b> <i>0.0 - 1.0</i> | 设置凹边过渡的柔和度。 |
| <b>凹面强度</b> <i>0.0 - 1.0</i> | 设置“凹边”的“边”加亮的最大强度。 设置为0将不突出显示。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-select-ex.gif" />
        </td>
    </tr>
</table>
