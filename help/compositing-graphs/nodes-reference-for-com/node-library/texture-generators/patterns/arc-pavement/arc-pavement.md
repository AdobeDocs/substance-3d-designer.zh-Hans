---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: 使用弧形路面节点生成弧形路面图案，用于创建弯曲的道路和路径纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弧形路面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 弧形路面

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## 弧形路面

**英寸：** *纹理生成器**/Patterns*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

生成巴黎弧形路面图案。 无法使用标准[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)或[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)实现此效果，因此使用此专用节点。

## 参数

* **缩放**： *1 - 8*&#x200B;设置全局缩放/拼贴。
* **图案数量**： *1 -* 32\
  设置每条弧线中使用的砖块量。
* **图案数量随机**： *0.0 - 1.0*\
  将每条弧线中的砖块量随机分布。 具有赋予砖块不同比例的附加效果。
* **图案最小数量**： *1 - 10*\
  在随机弧线时控制砖块的最小数量。
* **弧线数量**： *0 - 20*\
  设置垂直栈叠的弧线数量。 更改Height。
* **图案**：*输入图像，方形，磁盘，抛物面，铃声，高斯，荆棘，金字塔，砖块，层次，波浪，半圆，脊状的圆，新月，胶囊体，锥形*\
  选择要使用的图案形状。
* **输入图像**： *双线性+Mipmaps，双线性，最接近*
* **图案缩放**： *0.0 - 1.0*&#x200B;设置每个拼贴的缩放。
* **图案宽度**： *0.0 - 1.0*\
  设置每个拼贴的宽度。
* **图案Height**： *0.0 - 1.0*\
  设置每个磁贴的Height。
* **图案宽度随机**： *0.0 - 1.0*\
  随机分配拼贴宽度。
* **图案Height随机**： *0.0 - 1.0*\
  随机分布拼贴Height。
* **全局图案宽度随机**： *0.0 - 1.0*&#x200B;随机分布拼贴宽度，而不在拼贴之间产生更大的间隙。
* **图案Height减少**： *0.0 - 1.0*&#x200B;控制每个弧线末端的拼贴Height的挤压。
* **颜色随机**： *0.0 - 1.0*\
  随机分配拼贴颜色。
* **非正方形扩展**： *False/True*\
  启用压缩补偿并使用非正方形比例拉伸。

## 示例图像

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
