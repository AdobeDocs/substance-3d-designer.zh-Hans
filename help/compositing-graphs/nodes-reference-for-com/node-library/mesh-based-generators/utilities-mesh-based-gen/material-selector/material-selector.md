---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: 使用材质选择器节点，根据网格数据选择材质，以创建多材质纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质选择器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# 材质选择器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## 材质选择器

**在：** *基于网格的生成器**/Utilities*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

将全色ID映射转换为二进制、黑白蒙版。 允许将不同的颜色混合并组合到一个蒙版中。

如果您不想使用[多材质混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)并且更喜欢手动使用蒙版，或者如果您想在其他位置手动使用这些相同的蒙版，这样做将非常方便。

## 参数

* **材质**： 1 - 16\
  设置为其启用合并的材质数。
* **启用材质#1-16**： False/True\
  将颜色混合和组合切换到最终输出蒙版。 可以启用任意多个要组合的颜色。
* **材质#1-16**： （颜色值）\
  将转换为黑白的素材颜色的拾色器。
* **拾色器参数**\
  修改颜色混合以及将颜色转换为黑白色。
  * **模糊**： 0.01 - 1.0\
    与相邻颜色混合的程度。
  * **填充**： 0.0 - 1.0\
    过渡的锐度，如对比度。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
