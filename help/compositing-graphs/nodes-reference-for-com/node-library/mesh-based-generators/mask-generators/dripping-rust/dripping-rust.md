---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: 使用“滴落铁锈”节点，根据网格几何形状和重力方向生成铁锈滴落图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 滴落铁锈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# 滴落铁锈

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## 滴落铁锈

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版呈现铁锈薄片和斑点，漏洞会不断消失。

## 参数

### 输入

* **曲率**： *灰度输入*\
  生成或烘焙的地图以帮助铁锈放置。
* **环境遮蔽**： *灰度输入*\
  生成或烘焙的地图以帮助铁锈放置。
* **位置**： *灰度输入*\
  已生成或已生成的滴落方向图。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **铁锈分配**： *0.0 - 1.0*&#x200B;铁锈量的主控件。
* **铁锈对比度**： *0.0 - 1.0*&#x200B;设置生成的铁锈杂点中的对比度数量（不影响滴落）。
* **分摊Smoothness**： *0.0 - 1.0*&#x200B;要应用于铁锈杂色的模糊/涂抹效果量。
* **滴漏强度**： *0.0 - 1.0*&#x200B;设置斑点滴漏的强度和长度。
* **滴落Smoothness**： *0.0 - 1.0*&#x200B;应用于滴落的模糊和平滑量。
* **滴样量**： *0 - 32*&#x200B;设置滴落效果的质量级别（步骤）。 对速度略有影响。

## 示例图像

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
