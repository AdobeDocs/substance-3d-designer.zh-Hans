---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: 使用“混合”节点可以基于高度图混合纹理，以创建逼真的材料过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# 混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## 混合

**范围：** *材质过滤器/效果*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据Height信息组合两个高度图。 生成混合高度图，但也会生成可在其他地方使用的黑色和白色蒙版。

当您要合并两个高品质的Heightmap时，此功能非常有用，但并非必须合并完整材料，如[材料Height混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)所需。

## 参数

### 输入

* **顶部Height**： *灰度输入*
* **底部Height**： *灰度输入*
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **Height偏移**： *0.0 - 1.0*&#x200B;偏移高度图，以便沿着Height轴移动混合级别。 这是混合的主要控件。
* **对比度**： *0.0 - 1.0*\
  调整混合的对比度，使过渡更锐利。
* **模式**： *平衡Height，底部Height优先级*&#x200B;在两种不同的混合模式之间切换。
* **不透明度**： *0.0 - 1.0*\
  混合前景Height的不透明度，使其淡入或淡出。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
