---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: 使用3D Linear gradient节点可根据空间效果的3D世界位置创建线性渐变。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-linear-gradient.resources/3d-linear-gradient.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据输入位置映射创建体积渐变。 在3D空间的2点之间有效地生成从黑到白的过渡。 仅打算与GPU引擎结合使用。

另请参阅[3D体积蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)，了解类似效果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>点位置模式</b> <i>UV位置，世界空间位置</i> | 如果要手动输入精确位置，请选择渐变点在UV空间中（在2D 视图中设置它们时效果最佳）还是在3D坐标中有效。 |
| <b>点1</b> | 渐变的起始点。 可以是基于“位置”模式的2D或3D坐标。 |
| <b>点2</b> | 渐变的终点。 可以是基于“位置”模式的2D或3D坐标。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整结果的对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-linear-gradient.resources/3d-gradient.gif" />
        </td>
    </tr>
</table>
