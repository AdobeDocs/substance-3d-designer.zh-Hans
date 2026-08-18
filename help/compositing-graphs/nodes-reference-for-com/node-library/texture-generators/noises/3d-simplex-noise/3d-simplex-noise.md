---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: 使用“3D单纯噪声”节点可生成3D单纯噪声图案，用于创建平滑、自然的体积纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D单纯噪声
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 3D单纯噪声

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## 3D单纯噪声

**在：** *纹理生成器**/杂波*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

将生成的位置映射插入输入插槽时生成程序性噪声。 它仅适用于GPU引擎。\
与[3D Perlin噪声](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)类似，但对于性能和速度很重要的情况，却更快且更简单。

此杂色可以使用[Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

## 参数

* **缩放**： *0.0 - 64.0*\
  设置效果的全局比例。
* **大小**： *0.0 - 2.0*&#x200B;分别对X、Y和Z轴执行非均匀缩放。

## 示例图像

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
