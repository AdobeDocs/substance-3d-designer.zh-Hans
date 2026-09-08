---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ''
description: 使用“混合”节点，使用各种混合模式将两个纹理混合在一起，以创建复合效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 9%

---


# 混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：混合](../../../../assets/comp_blend_1.png "原子节点：混合"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

使用指定的混合模式和可选蒙版组合两张图像。

它是所有原子节点中最有用的节点，几乎您在[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中构建的任何图表都将使用此节点。

</td>
</tr>
</table>

它的功能类似于在[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)或[Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html)中使两个图层相互叠加，并通过在顶部图层上设置的混合模式混合在一起。

>[!TIP]
>
> 了解[此专用页面](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md)的“混合”节点中可用的混合模式。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>不透明度</b> *浮动* | 前景图层的不透明度正在混合到背景中。 它独立于不透明度输入工作，并充当其附加乘数。 |
| <b>混合模式</b> *整数* [静态](../../../../glossary/glossary.md) | 设置要使用的混合操作。   请参阅有关混合模式的[专用页面](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md)。 |
| <b>Alpha混合</b> *整数* [静态](../../../../glossary/glossary.md) | 确定颜色输入具有Alpha通道时的混合行为：<ul data-preserve-html="true"> <li data-preserve-html="true">使用源 Alpha</li> <li data-preserve-html="true">忽略 Alpha</li> <li data-preserve-html="true">直接 Alpha 混合</li> <li data-preserve-html="true">预乘Alpha混合</li> </ul> |
| <b>裁切区域</b> *浮点4* [静态](../../../../glossary/glossary.md) | 允许设置自定义裁剪区域，其行为类似于其他不透明度蒙版。 任何裁剪区域只显示背景。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>前景</b> *灰度/颜色* | 混合操作的顶部或前景图层。 |
| <b>背景</b> *灰度/颜色*&#x200B;主要 | 混合操作的底部或背景图层。 |
| <b>不透明度</b> *灰度* | 可选Alpha蒙版输入。 |

>[!IMPORTANT]
>
> 混合节点具有动态输入，可根据您的连接在“灰度”和“颜色”之间切换。<b> 混合节点只能混合相同类型</b>的两个输入。
> 
> 将颜色和灰度输入连接到前景和背景会导致出现一条虚线红色连接线，表示存在计算错误。
> 
> 这是新用户遇到颜色连接与灰度连接问题的首要原因：请确保两个连接属于同一类型！

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

*即将推出。*
