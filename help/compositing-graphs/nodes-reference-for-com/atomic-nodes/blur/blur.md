---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ""
description: 使用模糊节点将模糊效果应用于纹理，以平滑细节并创建柔和的聚焦效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 模糊
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 6%
---

# 模糊

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![模糊节点图标](blur.resources/blur-9.png){width="20%"}

**在：**&#x200B;个原子节点中

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

模糊节点执行“方框模糊”操作：在设定的距离上平均像素值，从而产生模糊、不锐利的外观。 它提供了[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中可用的最简单、最快、最基本的模糊操作。

虽然模糊适用于快速、简单的操作（如略微柔化某些边缘），但在任何更苛刻的场景中，[模糊总部](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md)都是更好的选择，可以牺牲性能来换取质量。

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="blur.resources/blur-tooltip.gif" alt="模糊工具提示" /></div>

## 参数

* **强度**： 0-unlimited\
  设置模糊的强度或距离。 该数字没有上限，但如果使用较高的值，则整个图像会变为平均颜色。

以下示例显示了使用高值（本例中为50）时此节点的“模糊”在左侧与右侧的“[模糊HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md)”。 在1-2左右的值时，差异不会很明显。

| 模糊（原子） | 模糊 HQ |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-hq.png"/></div> |
