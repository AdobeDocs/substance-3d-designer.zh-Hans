---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: 使用Flood Fill映射器节点，使用用于纹理处理的泛洪填充算法跨连接的区域映射值。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill映射器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Flood Fill映射器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/floodfill-mapper-gray.png)![](flood-fill-mapper.resources/floodfill-mapper-color.png)

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

Flood Fill映射器允许将现有图案或Flood Fill重新映射到[纹理](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的每个单元格上。 它与[随机灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)或[渐变](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)等其他Flood Fill转换不同，因为它不生成纯色或纯值，但允许您使用自己的输入映射。 它可以看作是[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)和[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)或[形状映射器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md)的某种组合，因为它提供了许多类似的控件和界面。

颜色版本具有处理法线映射的其他控件，它可以[补偿切线空间法线映射旋转](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Flood Fill的Bbox</b> <i>颜色输入</i> | 标准Flood Fill输入，必填。 |
| <b>模式输入1-8</b> <i>灰度/彩色输入</i> | 自定图案图像输入。 |
| <b>模式分布图</b> <i>灰度输入</i> | id 图以确定将哪个图案发送到哪个单元格。 可以来自其他Flood Fill映射，例如“Flood Fill到索引”。 |
| <b>比例图</b> <i>灰度输入</i> | 映射以确定每个单元格的比例。 |
| <b>旋转贴图</b> <i>灰度输入</i> | 映射以确定每个单元格的旋转。 |
| <b>明亮度偏移量映射</b> <i>灰度输入</i> | 映射以设置每个单元格的明亮度 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>拼贴模式</b> <i>无拼贴，H+V</i> | 设置是否使用拼贴。 仅当“大小”或“缩放”设置为小于1时可见。 |
| <b>图案</b> |  |
| <b>模式输入编号</b> <i>1 - 8</i> | 设置要使用的自定义模式输入量。 |
| <b>模式分发模式</b> <i>随机，形状大小，分布图输入</i> | 设置方法以确定单元格中显示的图案。 |
| <b>图案分布抖动</b> <i>0.0 - 1.0</i> | 允许在图案分布中稍作变化或偏移，而不通过随机植入更改所有内容。 |
| <b>大小</b> |  |
| <b>大小模式</b> <i>相对于纹理，相对于形状BSphere，相对于最大形状，相对于最小形状，适合形状BBox</i> | 设置如何确定每个单元格中的图案大小。 |
| <b>大小</b> <i>0.0 - 1.0</i> | 允许图案非均匀缩放。 |
| <b>缩放</b> <i>0.0 - 1.0</i> | 设置效果的全局（统一）比例。 |
| <b>缩放地图乘数</b> <i>0.0 - 1.0</i> | 设置可选的“比例图”的影响。 |
| <b>随机缩放</b> <i>-1.0 - 1.0</i> | 设置图案缩放范围内的随机变化量。 |
| <b>旋转</b> |  |
| <b>旋转</b> <i>0.0 - 1.0</i> | 为每个单元格设置全局一致旋转。 |
| <b>旋转贴图乘数</b> <i>0.0 - 1.0</i> | 设置可选旋转贴图的影响。 |
| <b>旋转随机</b> <i>0.0 - 1.0</i> | 设置每个单元格的随机旋转量。 |
| <b>旋转自动缩放</b> <i>False/True</i> | 设置图案在旋转时是否应该调整其比例以适合单元格。 |
| <b>位置</b> |  |
| <b>位置偏移</b> <i>0.0 - 1.0</i> | 设置每个单元格的全局位置偏移。 |
| <b>位置偏移对齐</b> <i>纹理，图案</i> | 设置为将偏移量0点与“图案”单元格或纹理对齐。 |
| <b>位置偏移随机</b> <i>0.0 - 1.0</i> | 设置每单元格“位置偏移”随机化的数量。 |
| <b>颜色（仅适用于灰度版本）</b> |  |
| <b>明亮度范围</b> <i>0.0 - 1.0</i> | 设置纹理上的全局对比度，其中0变为中度灰色。 |
| <b>明亮度范围随机</b> <i>0.0 - 1.0</i> | 设置明亮度范围的随机数量。 |
| <b>明亮度偏移</b> <i>-1.0 - 1.0</i> | 设置明亮度的偏移，作为亮度控件。 |
| <b>明亮度偏移随机</b> <i>0.0 - 1.0</i> | 设置明亮度偏移的随机数量。 |
| <b>明亮度偏移映射多路复用器</b> <i>0.0 - 1.0</i> | 设置可选明亮度偏移映射的影响。 |
| <b>背景颜色</b> <i>（灰度值）</i> | 设置混合纹理的背景色。 |
| <b>颜色（仅适用于颜色版本）</b> |  |
| <b>法线图</b> <i>False/True</i> | 设置为将图案输入解释为法线图。 将补偿并修复法线切线空间旋转。 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同的法线贴图格式之间切换（反转绿色通道）。 仅当正常映射为True时激活。 |
| <b>HSL调整</b> <i>-1.0 - 1.0</i> | 全局调整HSL。 |
| <b>HSL Random</b> <i>-1.0 - 1.0</i> | 设置每个单元格的HSL随机化。 |
| <b>Alpha调整</b> <i>-1.0 - 1.0</i> | 设置全局Alpha调整，降低Alpha对比度。 |
| <b>Alpha随机</b> <i>-1.0 - 1.0</i> | 设置每个单元格的Alpha调整随机化。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 设置混合纹理的背景色。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/floodfill-mapper-ex01.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/floodfill-mapper-ex02.jpg" />
        </td>
    </tr>
</table>
