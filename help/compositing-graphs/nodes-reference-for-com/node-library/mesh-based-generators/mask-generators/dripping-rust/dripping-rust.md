---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: 使用“滴落铁锈”节点，根据铁锈几何和重力方向生成网格滴落图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 滴落铁锈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# 滴落铁锈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dripping-rust.resources/dripping-rust.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白色蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版呈现铁锈薄片和斑点，漏洞会不断消失。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>弯曲</b> <i>灰度输入</i> | 烘焙或生成的映射有助于放置铁锈。 |
| <b>Ambient occlusion</b> <i>灰度输入</i> | 烘焙或生成的映射有助于放置铁锈。 |
| <b>位置</b> <i>灰度输入</i> | 已烘焙或生成的滴落方向地图。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>铁锈分摊</b> <i>0.0 - 1.0</i> | 铁锈量的主控件。 |
| <b>铁锈对比度</b> <i>0.0 - 1.0</i> | 设置所生成铁锈斑点的对比度（不影响滴落）。 |
| <b>正在分配Smoothness</b> <i>0.0 - 1.0</i> | 应用于铁锈斑点的模糊/涂抹效果的量。 |
| <b>液滴强度</b> <i>0.0 - 1.0</i> | 设置斑点滴的强度和长度。 |
| <b>滴Smoothness</b> <i>0.0 - 1.0</i> | 应用于滴落的模糊和平滑量。 |
| <b>滴样量</b> <i>0 - 32</i> | 设置滴落效果的质量级别（步骤）。 对速度略有影响。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dripping-rust.resources/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
