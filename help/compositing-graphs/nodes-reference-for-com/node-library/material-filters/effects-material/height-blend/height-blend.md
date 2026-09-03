---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: 使用“Height混合”节点根据Height贴图混合纹理，以创建逼真的材质过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Height混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend-01.png){width="128px"}

<b>进入：</b>材质过滤器>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据Height信息组合两个高度图。 生成混合高度图，但也会生成可以在其他地方使用的黑白蒙版。

当您要合并两个高品质的高度图时，此功能非常有用，但并非必须合并全部素材，这是[素材Height混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)所必需的。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Height顶部</b> <i>灰度输入</i> |  |
| <b>Height底部</b> <i>灰度输入</i> |  |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>Height偏移</b> <i>0.0 - 1.0</i> | 偏移高度图，以便沿着轴移动混合级别。 这是混合的主要控件。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整混合的对比度，使过渡更锐利。 |
| <b>模式</b> <i>平衡Height，底部Height优先级</i> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 混合前景Height的不透明度，使其淡入或淡出。 |
