---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: 使用Scratches生成器节点创建程序化的划痕图案，以增加材料的磨损和损坏。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scratches生成器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Scratches生成器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Scratches生成器（正常）

**英寸：** *纹理生成器**/Patterns*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

这将放置带有许多自定义选项的随机划痕，例如，允许您设置方向、扩展和扭曲。

Scratches生成器的一个特殊版本是Scratches生成器Normal，它根据这些划痕的深度生成正常映射。 大多数选项完全相同，但它有一些额外的参数明确标记为“正常”设置（请参阅下文）。

## 参数

* **样条数**： *1 - 512*&#x200B;要放置的划痕（样条）量。
* **每个样条的最大段数**： *2 - 256*&#x200B;划痕长度上的段/子分割数。 导致曲线和扭曲更平滑。 扭曲值越高，效果越明显。
* **样条旋转**： *0.0 - 1.0*&#x200B;所有样条统一旋转，以沿某一方向定向它们。
* **样条旋转随机**： *0.0 - 1.0*&#x200B;角度变化，随机旋转每个样条。
* **样条缩放**： *0.0 - 1.0*&#x200B;统一缩放所有样条。
* **样条随机**： *0.0 - 1.0*&#x200B;分别随机缩放每个样条。
* **样条扭曲**： *0.0 - 1.0*&#x200B;所有样条的扭曲级别一致。
* **样条扭曲随机**： *0.0 - 1.0*&#x200B;分别随机化每个样条的扭曲级别。
* **样条扭曲频率**： *0.0 - 1.0*&#x200B;设置扭曲频率，控制扭曲细节的比例。
* **样条宽度**： *0.0 - 2.0*&#x200B;统一设置所有样条宽度。
* **样条宽度随机**： *0.0 - 1.0*&#x200B;分别随机化每个样条的样条宽度。
* **样条位置随机**： *0.0 - 1.0*&#x200B;分别随机化每个样条的位置。 此值越低，群集到画布中心的样条越多。 可用于创建划痕点。
* **以像素为单位设置样条宽度**： *False/True*&#x200B;确定用于样条宽度设置的单位。
* **随机明亮度（仅限灰度版本）**： *0.0 - 1.0*&#x200B;分别随机化每个样条的明亮度。
* **正常强度（仅限正常版本）**： *0.0 - 1.0*&#x200B;全局设置每个样条正常效果的强度。
* **&#x200B;法线强度随机**（仅限法线版本）****： *0.0 - 1.0*分别随机化每个样条的法线强度。
* **&#x200B;普通格式**（仅限普通版本）****： *DirectX，OpenGL*\
  在不同正常映射格式之间切换（反转绿色通道）。
* **淡化模式**：*无、开始、结束、开始+结束*&#x200B;设置样条是否淡化以及淡化方向。
* **渐隐长度**： *0.0 - 1.0*&#x200B;设置渐隐效果的长度（如果在上面启用）。
* **非正方形扩展**： *False/True*\
  启用以非方形比例补偿挤压和拉伸。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
