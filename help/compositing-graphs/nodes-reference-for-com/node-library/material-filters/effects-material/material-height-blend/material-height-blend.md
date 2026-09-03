---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# 材质Height混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-height-blend.resources/material-height-blend-01.png){width="128px"}

<b>进入：</b>材质过滤器>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点是[混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md)的更高级版本，它根据两个材料的高度图混合它们。 由于没有用户定义的蒙版，因此必须有两个高度图，每个材料一个高度图，其中至少一个高度图不是统一值。

如果合并两种不同的高品质材料而没有高品质blending mask，则此功能非常有用。

如果要混合在水中或雪中，则可以使用[Snow覆盖](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)和[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)节点。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 |
| <b>Height偏移</b> <i>0.0 - 1.0</i> | 偏移高度图，以便沿着轴移动混合级别。 这是混合的主要控件。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整混合的对比度，使过渡更锐利。 |
| <b>模式</b> <i>平衡Height，底部Height优先级</i> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 混合前景Height的不透明度，使其淡入或淡出。 |
| <b>反照率匹配</b> <i>0.0 - 1.0</i> | 在反照率之间执行的内部颜色匹配量。 |
