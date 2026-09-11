---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: 使用“多混合”节点将多个材料混合在一起，以创建复杂的材料组合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# 多混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-material-blend.resources/multi-material-blend.png){width="128px"}

<b>进入：</b>材质过滤器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点根据材料ID/颜色Id 图合并多个材料，一个可以从网格中烘焙。 无论您在“声道”组中启用哪种声道，它最多需要16种不同的完整材料。

在对全部属性添加纹理时，节点非常有用，因为它允许对材料进行完全参数化，同时仍动态组合所有属性。 非常适合具有适当ID烘焙的从简单到复杂的道具的纹理化，甚至适合创建完全符合团队标准的完全流水线“模板”Substance。

请记住，使用此材料时，“插槽1”始终是默认材料，并且在任何不显示其他材料的位置都会出现。 这就是您无法为它设置颜色的原因。 如果您想安全地播放此音频，例如可以插入设置为粗黑的[基础材质](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>1-16个完整材料插槽</b> | 插槽数量由<b>材料</b>下拉菜单决定。 |
| <b>颜色ID</b> <i>颜色输入</i> | 烘焙的颜色Id 图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>材料</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | 设置要混合的不同材料的最大数量。 |
| <b>频道</b> | 在此组中打开和关闭材料声道，例如，在使用Specular/光泽度映射而非金属/粗糙度时。 |
| <b>材料2-16</b> | 启用的每个材料均会显示一个组。 |
| <b>颜色</b> <i>（颜色值）</i> | 从与此材料插槽匹配的Id 图中拾取的颜色。 |
| <b>模糊</b> <i>0.01 - 1.0</i> | 出血到邻近颜色。 |
| <b>填充</b> <i>0.0 - 1.0</i> | 过渡硬度：蒙版对比度。 |
