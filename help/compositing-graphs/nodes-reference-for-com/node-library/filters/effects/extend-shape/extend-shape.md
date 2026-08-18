---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: 使用Extend Shape节点将形状扩展至其边界之外，以创建扩展的蒙版和图案效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**英寸：**&#x200B;滤镜*/效果*

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**Extend Shape**&#x200B;节点将&#x200B;**输入**&#x200B;的&#x200B;*节*&#x200B;延伸至设定的方向和距离。

使用&#x200B;**Show helper**&#x200B;参数可以可视化扩展部分和扩展方向。

</td>
</tr>
</table>

## 参数

* **模式** *整数*&#x200B;定义用于应用扩展的&#x200B;*参数*：
  * *双向*：由&#x200B;**扩展位置**&#x200B;和&#x200B;**扩展角度**&#x200B;指定的&#x200B;**输入**&#x200B;部分在&#x200B;*相反方向*&#x200B;上扩展到&#x200B;**扩展距离**&#x200B;上
  * *单向*：由&#x200B;**扩展位置**&#x200B;和&#x200B;**扩展角度**&#x200B;指定的&#x200B;**输入**&#x200B;部分在&#x200B;*单向*&#x200B;中扩展到&#x200B;**扩展距离**&#x200B;上
  * *开始/结束位置*：扩展&#x200B;*矢量*&#x200B;由&#x200B;**开始位置**&#x200B;和&#x200B;**结束位置**&#x200B;定义。 **开始位置**&#x200B;处&#x200B;**输入**&#x200B;的&#x200B;*垂直*&#x200B;部分在&#x200B;*上在此矢量*&#x200B;上扩展到&#x200B;**结束位置**
* **延伸距离** *浮动*&#x200B;应延伸由&#x200B;**延伸位置**&#x200B;和&#x200B;**延伸角度**&#x200B;所指定的截面的距离。 距离以图像范围的&#x200B;*比例*&#x200B;表示。
* **扩展位置** *浮点*&#x200B;应扩展的分区图像中的位置。 该值表示为距中心&#x200B;*的*&#x200B;偏移。
* **扩展角度** *浮点*&#x200B;考虑到起始点为&#x200B;*垂直截面*，应扩展的截面的角度。
* **开始位置** *浮点2* *扩展矢量*&#x200B;的开始位置。
* **结束位置** *浮点2* *扩展矢量*&#x200B;的结束位置。
* **开始明亮度偏移** *浮动*&#x200B;将明亮度偏移应用于&#x200B;*位于*&#x200B;扩展部分之前的图像区域。 此明亮度偏移是沿截面&#x200B;*向截面之后的图像区域的明亮度插入的*。\
  *注意*：此参数仅在节点的&#x200B;**灰度**&#x200B;版本中可用。
* **结束明亮度偏移** *浮动*&#x200B;将明亮度偏移应用于&#x200B;*跟随扩展部分*&#x200B;的图像区域。 此明亮度偏移是沿截面&#x200B;*向截面前图像区域的明亮度插入的*。\
  *注意*：此参数仅在节点的&#x200B;**灰度**&#x200B;版本中可用。
* **亮度。 “偏移”忽略黑色像素** *布尔值*&#x200B;当设置为&#x200B;*True*&#x200B;时，*两者* **开始明亮度偏移**&#x200B;和&#x200B;**结束明亮度偏移**&#x200B;中指定的明亮度偏移仅应用于&#x200B;*非黑色*&#x200B;像素，即值大于0的像素。\
  *注意*：此参数仅在节点的&#x200B;**灰度**&#x200B;版本中可用。
* **筛选模式** *整数*&#x200B;定义在像素之间&#x200B;*插值*&#x200B;时如何处理取样结果：
  * *最接近的*：将对&#x200B;*相同的*&#x200B;值取样（较快）
  * *双线性*：将在结果上应用双线性滤镜，以实现&#x200B;*更平滑*&#x200B;的外观
* **显示帮助程序** *布尔值*&#x200B;将&#x200B;*扩展部分*&#x200B;显示为叠加，箭头显示扩展的&#x200B;*方向*。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
