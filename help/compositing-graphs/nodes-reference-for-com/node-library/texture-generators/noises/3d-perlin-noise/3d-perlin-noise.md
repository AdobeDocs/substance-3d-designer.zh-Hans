---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: 使用3D Perlin噪声节点在3D空间中生成平滑的Perlin噪声图案，用于创建自然外观的体积纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin噪声
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 3D Perlin噪声

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**在：** *纹理生成器**/噪声*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**3D Perlin噪声**&#x200B;节点基于&#x200B;**位置映射**&#x200B;输入在3D空间中生成Perlin噪声。

此节点可以使用[Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

>[!WARNING]
>
> 此噪声仅适用于&#x200B;*GPU引擎*（即&#x200B;**Direct3D**&#x200B;或&#x200B;**OpenGL**）。 转到&#x200B;**工具>切换引擎...**&#x200B;或按&#x200B;**F9**&#x200B;键以选择所需的引擎。

</td>
</tr>
</table>

## 参数

* **反转** *布尔值*\
  反转输出图像。
* **缩放** *Float*\
  控制3D Perlin噪声的比例。
* **大小** *Float3*\
  控制&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中的3D Perlin噪声的大小。 值不一致会产生&#x200B;*拉伸或挤压*&#x200B;效果。
* **偏移** *Float3*\
  将偏移应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中的3D Perlin噪声的&#x200B;*位置*。
* **扭曲强度** *Float*\
  控制应用于3D Perlin噪声的&#x200B;*变形效果*&#x200B;的强度。
* **扭曲比例乘数** *Float*\
  控制变形效果中使用的&#x200B;*变形图案*&#x200B;的比例，该比例由&#x200B;**扭曲强度**&#x200B;控制。
* **基线** *Float*\
  将&#x200B;*偏移*&#x200B;应用于3D Perlin噪声值分布的基线&#x200B;*明亮度*&#x200B;值。
* **对比度** *Float*\
  调整3D Perlin噪声的对比度。
* **绝对** *布尔值*\
  使用3D Perlin噪声中的绝对值。 这实际上&#x200B;*反转*&#x200B;低于0.5 *的值*&#x200B;的值分布。
* **启用拼贴** *布尔值*\
  调整3D Perlin噪声，使其生成的图案&#x200B;*在X、Y和Z轴中重复*。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>
