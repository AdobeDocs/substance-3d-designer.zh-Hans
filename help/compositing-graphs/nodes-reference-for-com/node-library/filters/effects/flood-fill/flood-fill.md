---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: 使用Flood Fill节点可填充颜色相近的连接区域，以创建蒙版和纹理处理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

Flood Fill是高级效果集的一部分，该效果允许您将更多的变化添加到基本的二进制拼贴纹理中。 它本不该单独使用：相反，它更像其他Flood Fill效果的起点。 这种拆分的独立数据可实现更动态、更优化和更少的破坏性的工作流程。

其他Flood Fill效果包括[Flood Fill到渐变](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)、[Flood Fill到彩色/灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md)、[Flood Fill到随机灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)、[Flood Fill到随机颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md)、[Flood Fill到边框大小](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md)、[Flood Fill到位置](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md)、[Flood Fill映射器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md)和[Flood Fill到索引](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> 输入图需要适合Flood Fill才能工作。 理想情况下，它是二进制映射（仅黑白，无灰度），其中每个拼贴与其他行隔开一条边界，该边界对于每个像素都是全黑色(0,0，0)。 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)就是一个非常理想的候选对象。
> 
> 如果拼贴未用全黑像素分隔，通常在使用灰度值时会出现问题。 可以通过结果中整体缺少红色值以及可能具有奇怪的人为线条来识别这一点。 在这种情况下，请调整输入图的对比度或切出输入图。 确保更改“安全/速度”的平衡设置，看看是否会有改善。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>安全/速度取舍</b> <i>形状简单或小，形状复杂或大，无失败模式。</i> | 设置最适合输入形状的计算模式。 如果选择正确的模式，则允许获得更准确的结果。 |
| <b>高级选项</b> <i>显示高级参数和输出/隐藏高级参数和输出</i> |  |
| <b>覆盖安全/速度权衡</b> <i>-1 - 100</i> | 仅在打开“高级选项”时可见。 允许覆盖内部功能。 非常高级，可用于创建自己的效果或调试。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/flood-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/flood-ex1.png" />
        </td>
    </tr>
</table>

Flood Fill结果的好例子和坏示例。
