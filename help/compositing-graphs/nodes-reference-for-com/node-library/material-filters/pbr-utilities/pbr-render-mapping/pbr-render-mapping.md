---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: 使用“PBR 渲染映射”节点将材料输出转换为不同的PBR 渲染映射格式。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 渲染映射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# PBR 渲染映射

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## PBR 渲染映射（彩色/灰度）

**在：** *材质过滤器/PBR实用工具*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

这是[PBR 渲染节点](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)的扩展节点，它允许您将一个单独的纹理映射到上一个[PBR 渲染](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)中的形状上。 其主要目标是让您将[PBR 渲染](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)中的每个单独通道重新映射到形状上，以创建复合映射通道故障，如下例所示。 您可以使用“PBR 渲染映射”节点作为组件，自由创建自己的合成方法和蒙版。

彩色和灰度版本适用于两种类型的数据：对漫射图使用颜色，对粗糙度、金属和其他灰度图使用灰度。

### 输入

* **纹理**： *彩色/灰度输入*\
  纹理以映射到形状上。
* **UV**： *颜色输入*&#x200B;来自[PBR 渲染节点的强制UV数据输入。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)

## 参数

* **背景颜色**： *（颜色值）*设置纯色值以在背景中使用。

## 示例图像

示例是将[线性渐变](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)上的[直方图选择](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md)用作蒙版的4个不同PBR 渲染映射节点的合成。

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>
