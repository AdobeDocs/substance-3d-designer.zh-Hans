---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: 使用Height混合节点根据高度图混合多个材料以创建分层材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质Height混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# 材质Height混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

## 材质Height混合

**范围：** *材质过滤器/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点是[混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md)的更高级版本，它根据两个材料的高度图混合它们。 由于没有用户定义的蒙版，因此必须有两个高度图，每个材料一个高度图，其中至少一个高度图不是统一值。

如果合并两种不同的高品质材料而没有高品质blending mask，则此功能非常有用。

如果要混合在水中或雪中，则可以使用[Snow覆盖](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)和[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)节点。

## 参数

### 参数

* **频道**\
  在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **Height偏移**： *0.0 - 1.0*&#x200B;偏移高度图，以便沿着Height轴移动混合级别。 这是混合的主要控件。
* **对比度**： *0.0 - 1.0*\
  调整混合的对比度，使过渡更锐利。
* **模式**： *平衡Height，底部Height优先级*&#x200B;在两种不同的混合模式之间切换。
* **不透明度**： *0.0 - 1.0*\
  混合前景Height的不透明度，使其淡入或淡出。
* **反照率匹配**： *0.0 - 1.0*&#x200B;反照率之间执行的内部颜色匹配量。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
