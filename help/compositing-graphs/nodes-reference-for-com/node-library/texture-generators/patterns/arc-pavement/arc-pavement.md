---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: 使用“弧形路面”节点生成弧形路面图案，用于创建弯曲的道路和路径纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弧形路面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
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

* **比例**： *1 - 8*&#x200B;设置全局比例/拼贴。
* **图案数量**： *1 -* 32\
  设置每条弧线中使用的砖块数量。
* **图案数量随机**： *0.0 - 1.0*\
  随机选择每条弧线中的砖块数量。 具有赋予砖块不同比例的附加效果。
* **图案最小数量**： *1 - 10*\
  在随机弧线时控制砖块的最小数量。
* **弧线数量**： *0 - 20*\
  设置垂直栈叠的弧线数量。 更改程序块Height。
* **图案**：*输入图像，方形，圆盘，抛物面，贝尔，高斯，刺，金字塔，砖，渐变，波形，半铃，脊状贝尔，新月，胶囊，锥形体*\
  选择要使用的图案形状。
* **输入图像过滤**： *双线性+多角映射，双线性，最接近*
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
  启用以非方形比例补偿挤压和拉伸。

## 示例图像

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
