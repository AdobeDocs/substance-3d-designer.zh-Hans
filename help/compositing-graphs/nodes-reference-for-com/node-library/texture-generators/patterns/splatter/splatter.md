---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: 使用“飞溅”节点跨散点形状，以创建随机图案和有机纹理细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 飞溅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# 飞溅

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## 飞溅（颜色）

**英寸：** *纹理生成器**/Patterns*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

Scplatter是一种图案生成器，用于随机放置地图输入。 它具有许多用于几何图案化放置的控制，并且比[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)使用起来更简单。 后者可以获得类似的结果，但复杂得多。

“飞溅”适用于快速压印某些形状，而无需过多调整。

请记住，默认的Splatter参数看起来完全不是随机的：您需要调整其中几个参数以获得随机性（主要是无序参数）。 另外请记住，“飞溅”需要地图输入才能生效。

## 参数

* **图案大小宽度**： *0.0 - 1000.0*&#x200B;在X轴上使用的图案数。
* **图案大小Height**： *0.0 - 1000.0*&#x200B;在Y轴上使用的图案数。
* **旋转**： *-360.0 - 360.0*&#x200B;按设置量旋转每个图案。
* **旋转变化**： *0.0 - 360.0*&#x200B;为每个单独的形状引入随机旋转。
* **缩放**： *100.0 - 10000.0*&#x200B;放大最终结果。 请记住，这会打破拼贴！
* **增益**： *0.0 - 10.0*&#x200B;调整每个模式的混合增益。 使它们更加突出。
* **平移X**： *-100.0 - 100.0*&#x200B;平移X轴的整个结果。
* **平移Y**： *-100.0 - 100.0*&#x200B;平移Y轴的整个结果。
* **无序**： *0.0 - 100.0*\
  随机移动形状。
* **网格号**： *0 - 8*&#x200B;跳转不同的网格大小以调整结果缩放。 保持拼贴。
* **无序角度**： *0.0 - 360.0*&#x200B;控制无序移动的角度。
* **无序随机**： *False/True*&#x200B;随机化无序角度，从而增加更多的混乱。
* **图案大小**： *5 - 12*
* **大小变化**： *0.0 - 100.0*&#x200B;为每个形状引入随机缩放。
* **图像输入筛选（仅限引擎> v4）**：*双线性+Mipmaps、双线性、最接近*&#x200B;要应用于输入图像的筛选。
* **输出电平最小值**： *0.0 - 1.0*&#x200B;输出最小电平调整。
* **输出电平最大值**： *0.0 - 1.0*&#x200B;输出最大电平调整。
* **背景颜色**： *（灰度值）*设置纯背景颜色。
* **明亮度变化**： *0.0 - 1.0（仅限灰度版本）*引入明亮度变化。
* **颜色变化**： *0.0 - 1.0（仅限颜色版本）*引入颜色变化。

## 示例图像

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
