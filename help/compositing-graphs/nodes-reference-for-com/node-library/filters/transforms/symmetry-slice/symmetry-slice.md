---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 使用“对称切片”节点沿对称轴切片纹理，以创建镜像图案和效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 对称切片
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# 对称切片

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/symmetry-slice-01.png){width="128px"}

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

复杂的对称/镜像操作节点。 允许使用完全控制进行各种几何操作，但需要一些试验。

与[镜像](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md)和[对称](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)相比，此节点具有更多选项。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>对称模式</b> <i>0 - 6</i> | 选择对称几何/镜像直线。 选项包括“水平”、“垂直”、“左对角”、“左对角”、“垂直反相”、“边角”和“对角角”。 |
| <b>传输模式</b> <i>0 - 6</i> | 混合模式。 选项包括： |
| <b>混合</b> <i>0.0 - 1.0</i> | 将原始图像混合回结果。 |
| <b>翻转</b> <i>False/True</i> | 反向原点，表示操作的原点侧反向。 例如，从左到右对称将变为从右到左。 |
| <b>翻面2</b> <i>False/True</i> | 仅在对称模式为5或6时使用。 反向角原点。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symmetry-slice-02.png" />
        </td>
    </tr>
</table>
