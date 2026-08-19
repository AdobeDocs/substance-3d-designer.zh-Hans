---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: 使用焦散线节点生成焦散光图案，用于创建水下和折射光照效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焦散
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 焦散

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**在：** *纹理生成器**/杂波*

**复杂**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

基于Height映射和光方向生成投影焦散线。有灰度版本和颜色版本时，差异都非常细微，但颜色版本会添加颜色分散效果。 光线从单点投射，不使用环境映射。

</td>
</tr>
</table>

## 参数

* **输出色彩空间**： *原始，sRGB*\
  设置输出色彩空间。
* **光子网格大小**：*自动、512、1024、2048、4096*\
  通过调整网格大小设置品质，但默认为匹配输入。 可用于加速计算。
* **表面Height比例**： *0.0 - 1.0*\
  用于确定如何解释Height的乘数。
* **表面Height位置**： *0.0 - 1.0*\
  设置折射曲面到投影的距离。
* **表面IOR**： *1.0 - 2.0*\
  设置折射率，在彩色版本中，这会增加更多的色散。
* **光子大小**： *1.0 - 50.0*\
  光子大小影响效果的锐度。
* **色差**： *0.0 - 0.01（仅限颜色版本）*\
  仅影响颜色色散。 IOR值较低时不可见。
* **抖动**： *0.0 - 1.0*\
  为投射的光子粒子添加不规则的抖动。
* **光源位置**：\
  移动光源位置。 也可以通过2D视图中的小工具来完成。
* **背景颜色**： *（颜色值）（仅限颜色版本）*\
  更改背景颜色。 灰度版本仅限黑色。
* **非正方形扩展**： *False/True*\
  启用使用非方形比率补偿挤压和拉伸。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
