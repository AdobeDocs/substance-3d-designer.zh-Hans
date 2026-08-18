---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi-fractal.html"
breadcrumb-title: ''
description: 使用Voronoi分形节点生成分形Voronoi图案，用于创建有机细胞纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi分形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Voronoi分形

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal.png){width="200px"}

**位置：** *纹理生成器* */杂色*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**Voronoi分形**&#x200B;节点使用&#x200B;*Z向下正交投影*&#x200B;生成&#x200B;*分形*&#x200B;映射到2D图像的3D Voronoi噪声。

此节点可以使用[Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

>[!WARNING]
>
> 此噪声仅适用于&#x200B;*GPU引擎*（即&#x200B;**Direct**&#x200B;或&#x200B;**OpenGL**）。 转到&#x200B;**工具>切换引擎……**&#x200B;或按&#x200B;**F9**&#x200B;键以选择所需的引擎。

</td>
</tr>
</table>

## 参数

* **反转** *布尔值*\
  反转输出图像。
* **缩放** *浮动*\
  控制分形Voronoi噪声的缩放程度。\
  *注意*：在&#x200B;*任意轴*&#x200B;上启用&#x200B;**拼贴**&#x200B;时，缩放调整为&#x200B;*步进*。 这是预期的。
* **大小** *浮点3*\
  控制&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中的分形Voronoi噪声的大小。 非均匀值导致&#x200B;*拉伸或挤压*&#x200B;效果。\
  *注意*：在&#x200B;*任意轴*&#x200B;上启用&#x200B;**拼贴**&#x200B;时，大小调整为&#x200B;*步进*。 这是预期的。
* **偏移** *浮点3*\
  将偏移应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中的分形Voronoi噪声的&#x200B;*位置*。
* **无序** *浮动3*\
  应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中每个噪声点的&#x200B;*随机偏移*&#x200B;的强度。
* **扭曲强度** *浮动*\
  控制应用于分形Voronoi噪声的&#x200B;*变形效果*&#x200B;的强度。
* **扭曲缩放乘数** *浮点*\
  控制变形效果中使用的&#x200B;*变形图案*&#x200B;的比例，该比例由&#x200B;**扭曲强度**&#x200B;控制。
* **最小级别** *整数*\
  分形图案中使用的最小&#x200B;*重复级别*。 更宽的最小值/最大值范围会生成&#x200B;*更丰富的图案*，并且随更多频率范围而变化。
* **最大级别** *整数*\
  分形图案中使用的最大重复级别&#x200B;*为*。 更宽的最小值/最大值范围会生成&#x200B;*更丰富的图案*，并且随更多频率范围而变化。
* **粗糙度** *浮动*\
  控制分形图案中&#x200B;*低重复级别与高重复级别*&#x200B;之间的平衡&#x200B;**。\
  *注意*： **0**&#x200B;的值导致输出为&#x200B;*不在行*&#x200B;中，并在行之后出现其他低值。 这是预期的。\
  *注意2*：仅当&#x200B;**混合模式**&#x200B;参数设置为&#x200B;*添加*&#x200B;时，此参数才可用。
* **隙度** *浮动*\
  控制应用的分形图案&#x200B;*填充空间*&#x200B;的方式。 *较高的*&#x200B;值会使图案中的间隙减少&#x200B;*，从而产生*&#x200B;更密&#x200B;*的杂色。*
* **全局不透明度** *浮动*\
  从0控制分形Perlin杂色值的&#x200B;*范围*。
* **圆角曲线** *浮动*\
  围绕杂色的每个点对&#x200B;*斜率*&#x200B;进行圆化，使其变为&#x200B;*凸形*。\
  *注意*：当&#x200B;**Style**&#x200B;参数设置为&#x200B;*Edge*&#x200B;时，此参数不可用。
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
* **混合模式** *整数*\
  设置空间中&#x200B;*重叠单元格*&#x200B;的值混合在一起的方法：
  * *添加*：添加值
  * *最大*：保留&#x200B;*最大*&#x200B;值
  * *分钟*：保留&#x200B;*最低*&#x200B;值
* **样式***整数*&#x200B;设置分形Voronoi噪声的数据渲染方法&#x200B;**，考虑噪声基于空间中的一组点：
  * *F1*：到空间中&#x200B;*最近点*&#x200B;的距离
  * *F2*：到空间中&#x200B;*秒近点*&#x200B;的距离
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;边缘&#x200B;*：空间中每个单元之间的*&#x200B;边缘*
  * *随机颜色*：为空间中的噪声的每个单元格分配&#x200B;*随机平面颜色*
* **边缘Thickness***浮点*&#x200B;调整分形Voronoi噪声细胞之间检测到的边缘Thickness。 在X、Y和Z轴检测边缘，因此某些厚度可能比其他厚度增加得更快，这取决于单元的&#x200B;*深度*。\
  *注意*：仅当&#x200B;**Style**&#x200B;参数设置为&#x200B;*Edge*&#x200B;时，此参数才可用。
* **随机颜色种子模式** *整数*\
  设置&#x200B;*获取*&#x200B;每个单元格颜色选择的随机种子的方法：
  * *全局随机植入*：使用节点继承的植入&#x200B;**
  * *手动种子*：使用&#x200B;*离散*&#x200B;种子\
    *注意*：仅当&#x200B;**Style**&#x200B;参数设置为&#x200B;*随机颜色*&#x200B;时，此参数才可用。
* **随机颜色种子** *整数*\
  应该用于每个单元格的颜色选择的离散随机种子。\
  *注意*：仅当&#x200B;**Style**&#x200B;参数设置为&#x200B;*随机颜色*&#x200B;并且&#x200B;**随机颜色种子模式**&#x200B;参数设置为&#x200B;*手动种子*&#x200B;时，此参数才可用。
* **启用拼贴** *布尔值*\
  调整分形Voronoi噪声，使其生成的图案&#x200B;*在X、Y和Z轴上重复*。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-sea.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-scifi-panel.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant4.jpg){width="256px"}

</td>
</tr>
</table>
