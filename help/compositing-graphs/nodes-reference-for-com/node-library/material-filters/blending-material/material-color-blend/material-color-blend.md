---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: 使用“素材颜色混合”节点可在素材之间混合颜色通道，以创建复合素材效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 素材颜色混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# 素材颜色混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>进入：</b>材质过滤器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点允许在顶部混合纯色，从而调整多通道全材质。 这是[材质调整混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)的主要区别，它只允许对通道进行[色阶](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)类型的调整，而此节点使用具有纯色的[混合](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)类型的调整。

此节点在您想要将平淡颜色提示引入漫射或基色时，或者当您想要通过使用设置的纯色值“平淡”其他通道时，最有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>颜色ID</b> <i>颜色输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>灰度蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 当使用“Specular/光泽度”映射而不是“金属/粗糙度”时，可打开和关闭此组中的素材通道。 |
| <b>扩散</b> |  |
| <b>颜色</b> <i>（颜色值）</i> | 要在Diffuse通道顶部混合的颜色值。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 在前景和背景之间混合不透明度。 |
| <b>混合模式</b> <i>正常，相加，去除，相乘，相加/次相加，最大，最小，开关</i> | 操作中使用的混合模式。 |
| <b>基色</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>正常</b> |  |
| <b>源</b> <i>Height，蒙版</i> |  |
| <b>混合模式</b> <i>合并，混合</i> |  |
| <b>Height强度</b> <i>0.0 - 1.0</i> |  |
| <b>Height不透明度</b> <i>0.0 - 1.0</i> |  |
| <b>格式</b> <i>DirectX， OpenGL</i> |  |
| <b>Specular</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>具发射性</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>光泽度</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>粗糙度</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>金属质感</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>Specular level</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>环境遮蔽</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>Height</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>不透明度</b> | 在此通道上方混合纯色，并使用漫射组中的选项。 |
| <b>色彩 ID 蒙版</b> <i>False/True</i> | 使用色彩 ID 蒙版而非灰度蒙版。 请记住，这只适用于一种颜色！<br><br>启用以下所有选项。 |
| <b>颜色</b> <i>（颜色值）</i> | 选取哪种颜色并将其转换为白色。 |
| <b>模糊</b> <i>0.01 - 1.0</i> | 您选取的颜色混合到其邻近区域的程度。 |
| <b>填充</b> <i>0.0 - 1.0</i> | 选择颜色的过渡对比度。 |
