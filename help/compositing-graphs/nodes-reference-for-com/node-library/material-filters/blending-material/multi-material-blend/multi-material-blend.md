---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: 使用“多材质混合”节点将多个材质混合在一起，以创建复杂的材质组合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多材质混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# 多材质混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## 多材质混合

**范围：** *素材滤镜/混合*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点基于材质ID/颜色ID映射合并多种材质，一种可以从网格中生成。 无论您在“通道”组中启用哪种通道，它最多都需要16种不同的完整素材。

在对全部道具进行纹理处理时，此节点非常有用，因为它允许将材质完全参数化，同时仍动态组合所有材质。 非常适合使用具有适当ID标记的简单到复杂的道具进行纹理贴图，甚至适合创建完全符合团队标准的完全流水线“模板”Substance。

请记住，使用此选项时，“材料1”、“槽1”始终是缺省材料，并且将在没有其他材料出现的任何位置出现。 这就是您无法为它设置颜色的原因。 如果您想安全地播放此音频，例如可以插入设置为粗黑的[基础材质](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)。

## 参数

### 输入

* **1-16个全材质插槽**&#x200B;插槽数量由&#x200B;**材质**&#x200B;下拉菜单确定。
* **颜色ID**： *颜色输入*\
  烘焙颜色ID映射。

### 参数

* **材质**：*2、3、4、5、6、7、8、9、10、11、12、13、14、15、16*&#x200B;设置要混合的不同材质的最大数量。
* **频道**\
  在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **材质2-16**&#x200B;启用的每个材质均显示一个组。
  * **颜色**： *（颜色值）*要从与此素材槽匹配的ID图中选择的颜色。
  * **模糊**： *0.01 - 1.0*&#x200B;溢流到邻近颜色。
  * **填充**： *0.0 - 1.0*&#x200B;过渡的硬度：蒙版对比。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
