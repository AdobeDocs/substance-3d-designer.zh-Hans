---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: 利用3D Voronoi节点生成基于3D世界位置的Voronoi图案，用于生成体细胞纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi.png){width="200px"}

**位置：** *纹理生成器* */杂色*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**3D Voronoi**&#x200B;节点基于&#x200B;**位置映射**&#x200B;输入在3D空间中生成Voronoi噪声。

此节点可以使用[Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

>[!WARNING]
>
> 此噪声仅适用于&#x200B;*GPU引擎*（即&#x200B;**Direct3D**&#x200B;或&#x200B;**OpenGL**）。 转到&#x200B;**工具>切换引擎……**&#x200B;或按&#x200B;**F9**&#x200B;键以选择所需的引擎。

</td>
</tr>
</table>

## 参数

* **反转** *布尔值*\
  反转输出图像。
* **缩放** *浮动*\
  控制3D Voronoi噪声的大小。\
  *注意*：在&#x200B;*任意轴*&#x200B;上启用&#x200B;**拼贴**&#x200B;时，缩放调整为&#x200B;*步进*。 这是预期的。
* **大小** *浮点3*\
  控制&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中的3D Voronoi噪声的大小。 非均匀值导致&#x200B;*拉伸或挤压*&#x200B;效果。\
  *注意*：在&#x200B;*任意轴*&#x200B;上启用&#x200B;**拼贴**&#x200B;时，大小调整为&#x200B;*步进*。 这是预期的。
* **偏移** *浮点3*\
  将偏移应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中3D Voronoi噪声的&#x200B;*位置*。
* **无序** *浮动3*\
  应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中每个噪声点的&#x200B;*随机偏移*&#x200B;的强度。
* **扭曲强度** *浮动*\
  控制应用于3D Voronoi噪声的&#x200B;*变形效果*&#x200B;的强度。
* **扭曲缩放乘数** *浮点*\
  控制变形效果中使用的&#x200B;*变形图案*&#x200B;的比例，该比例由&#x200B;**扭曲强度**&#x200B;控制。
* **圆角曲线** *浮动*\
  围绕杂色的每个点对&#x200B;*斜率*&#x200B;进行圆化，使其变为&#x200B;*凸形*。\
  *注意* ：当&#x200B;**Style**&#x200B;参数设置为&#x200B;*Edge*&#x200B;时，此参数不可用。
* **距离刻度** *浮动*\
  调整渐变&#x200B;*在每个噪声点周围的*&#x200B;距离。
* **距离模式** *整数*\
  将方法设置为&#x200B;*计算噪声每个点周围的距离渐变*：
  * *欧几里德*
  * *曼哈顿*
  * *切比雪夫*
  * *Minkowski*
* **闵可夫斯基数值** *浮动*\
  Minkowski距离的顺序&#x200B;*p*。 如果将距离渐变划分为几个象限，则此数值将对这些象限产生如下影响：
  * p是&#x200B;*刚好* 1：直线
  * p比1：凹形小&#x200B;**
  * p是&#x200B;*大于*&#x200B;的1：凸的\
    有趣的值：\
    *- 1.0*：曼哈顿距离\
    *- 2.0*：欧氏距离\
    *— 无限*：切比雪夫距离\
    *注意*：仅当&#x200B;**Distance Mode**&#x200B;参数设置为&#x200B;*Minkowski*&#x200B;时，此参数才可用。
* **样式** *整数*&#x200B;设置3D Voronoi噪声的数据渲染&#x200B;*方法，考虑噪声基于3D空间中的一组点：*
  * *F1*：到3D空间中&#x200B;*最近点*&#x200B;的距离
  * *F2*：到3D空间中&#x200B;*第二个最接近点*&#x200B;的距离
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;边缘&#x200B;*：3D空间中每个单元之间的*&#x200B;边缘*
  * *随机颜色*：为3D空间中的每个噪点单元分配&#x200B;*随机平面颜色*
* **边缘Thickness***浮动*&#x200B;调整3D Voronoi噪声的单元格之间检测到的边缘的Thickness。 在X、Y和Z轴检测边缘，因此某些厚度可能比其他厚度增加得更快，这取决于单元的&#x200B;*深度*。\
  *注意*：仅当&#x200B;**Style**&#x200B;参数设置为&#x200B;*Edge*&#x200B;时，此参数才可用。
* **启用拼贴** *布尔值*\
  调整3D Voronoi噪声，使其生成的图案在X、Y和Z轴上&#x200B;*重复*。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
