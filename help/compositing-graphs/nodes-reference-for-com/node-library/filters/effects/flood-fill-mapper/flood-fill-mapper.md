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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---


# Flood Fill映射器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

## Flood Fill映射器（灰度）

**范围：** *滤镜/效果*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

Flood Fill映射器允许将现有图案或Flood Fill重新映射到[纹理](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的每个单元格上。 它与[随机灰度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)或[渐变](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)等其他Flood Fill转换不同，因为它不生成纯色或纯值，但允许您使用自己的输入映射。 它可以看作是[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)和[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)或[形状映射器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md)的某种组合，因为它提供了许多类似的控件和界面。

颜色版本具有处理法线映射的其他控件，它可以[补偿切线空间法线映射旋转](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md)。

## 参数

### 输入

* **Flood FillBbox**： *颜色输入*&#x200B;标准Flood Fill输入，必填。
* **图案输入1-8**： *灰度/彩色输入*\
  自定图案图像输入。
* **图案分布图**： *灰度输入* ID映射，用于确定哪个图案将发送到哪个单元格。 可以来自其他Flood Fill映射，例如“Flood Fill到索引”。
* **比例图**： *灰度输入*&#x200B;用于确定每个单元格比例的地图。
* **旋转贴图**： *灰度输入*&#x200B;映射，用于确定每个单元旋转。
* **明亮度偏移映射**： *灰度输入*&#x200B;映射，用于设置每个单元格的明亮度

### 参数

* **拼贴模式**： *无拼贴，H+V*&#x200B;设置是否使用拼贴。 仅当“大小”或“缩放”设置为小于1时可见。
* **图案**
  * **模式输入编号**： *1 - 8*&#x200B;设置要使用的自定义模式输入量。
  * **模式分布模式**： *随机，形状大小，分布图输入*&#x200B;设置方法以确定单元格中显示的模式。
  * **图案分布抖动**： *0.0 - 1.0*&#x200B;允许图案分布有轻微变化或偏移，而不通过随机种子更改所有内容。
* **大小**
  * **大小模式**： *相对于纹理、相对于形状、相对于最大形状、相对于最小形状、适合形状*&#x200B;设置如何确定每个单元格中的图案大小。
  * **大小**： *0.0 - 1.0*&#x200B;允许图案非均匀缩放。
  * **缩放**： *0.0 - 1.0*\
    设置效果的全局（统一）比例。
  * **缩放映射多路复用器**： *0.0 - 1.0*&#x200B;设置可选缩放映射的影响。
  * **随机缩放**： *-1.0 - 1.0*&#x200B;设置图案缩放范围内的随机变化量。
* **旋转**
  * **旋转**： *0.0 - 1.0*&#x200B;为每个单元格设置全局、统一的旋转。
  * **旋转贴图多倍数**： *0.0 - 1.0*&#x200B;设置可选旋转贴图的影响。
  * **旋转随机**： *0.0 - 1.0*&#x200B;设置每个单元格的随机旋转量。
  * **旋转自动缩放**： *False/True*&#x200B;设置图案在旋转时是否应该调整其缩放以适应单元格。
* **位置**
  * **位置偏移**： *0.0 - 1.0*&#x200B;设置每个单元格的全局位置偏移。
  * **位置偏移对齐**：*纹理，图案*&#x200B;设置为将偏移0点与图案单元格或纹理对齐。
  * **位置偏移随机**： *0.0 - 1.0*&#x200B;设置每单元格位置偏移随机化的数量。
* **颜色**（仅适用于灰度版本）
  * **明亮度范围**： *0.0 - 1.0*&#x200B;设置纹理上的全局对比度，其中0变为中度灰色。
  * **明亮度范围随机**： *0.0 - 1.0*&#x200B;设置明亮度范围的随机化量。
  * **明亮度偏移**： *-1.0 - 1.0*&#x200B;设置明亮度的偏移，作为亮度控件。
  * **明亮度偏移随机**： *0.0 - 1.0*&#x200B;设置明亮度偏移的随机化量。
  * **明亮度偏移映射多路复用器**： *0.0 - 1.0*&#x200B;设置可选明亮度偏移映射的影响。
  * **背景色**： *（灰度值）*设置混合纹理的背景色。
* **颜色**（仅适用于颜色版本）
  * **是正常映射**： *False/True*&#x200B;设置为将图案输入解释为正常映射。 将补偿并修复法线切线空间旋转。
  * **普通格式**： *DirectX，OpenGL*\
    在不同的法线贴图格式之间切换（反转绿色通道）。 仅当正常映射为True时激活。
  * **HSL调整**： *-1.0 - 1.0*&#x200B;全局调整HSL。
  * **HSL随机**： *-1.0 - 1.0*&#x200B;设置每个单元格的HSL随机化。
  * **Alpha调整**： *-1.0 - 1.0*&#x200B;设置全局Alpha调整会降低Alpha对比度。
  * **Alpha随机**： *-1.0 - 1.0*&#x200B;设置每个单元格的Alpha调整随机化。
  * **背景颜色**： *（颜色值）*设置混合纹理的背景颜色。

.

## 示例图像

![](../../../../../../assets/floodfill-mapper-ex01.png)

![](../../../../../../assets/floodfill-mapper-ex02.jpg)

</td>
</tr>
</table>
