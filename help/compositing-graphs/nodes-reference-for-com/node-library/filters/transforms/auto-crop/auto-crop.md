---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: 使用“自动裁剪”节点自动裁剪纹理，以移除空边框并优化纹理尺寸。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自动裁剪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# 自动裁剪

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**英寸：**&#x200B;筛选器*/变换*

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**自动裁剪**&#x200B;节点调整&#x200B;**输入**，以便其内容可以放在图像的&#x200B;*中心*&#x200B;而不调整大小，或调整到图像的&#x200B;*范围*。

图像的内容由符合&#x200B;**X**&#x200B;和&#x200B;**Y**&#x200B;的&#x200B;*第一个和最后一个像素*&#x200B;的框定义，这些像素的值是&#x200B;*大于0*（即非黑色）。 **颜色**&#x200B;版本允许您从用于定义该框的RGB和Alpha 通道中进行选择。

</td>
</tr>
</table>

## 参数

* **模式** *整数*&#x200B;设置应应用的裁切方法：
  * *裁剪方形*：裁剪图像以便形状位于可以完全包含它的最小的&#x200B;*方形*&#x200B;图像的中心
  * *自动裁剪*：裁剪图像以便形状位于可以完全包含的最小的&#x200B;*正方形或非正方形*&#x200B;图像的中心
  * *适合（保持比例）*：在保持图像的&#x200B;*比例*（即宽长比）的同时，将图像大小调整为图像的&#x200B;*全宽*
  * *填充(拉伸)*：将图像大小调整为图像的&#x200B;*全宽*
* **使用alpha** *布尔值*&#x200B;使用&#x200B;**输入**&#x200B;的Alpha 通道来确定图像内容的&#x200B;*边界*&#x200B;以进行裁剪。 设置为&#x200B;*False*&#x200B;时，将改用黑色像素。\
  *注意*：此参数仅在节点的&#x200B;**颜色**&#x200B;版本中可用。
* **筛选模式** *整数*&#x200B;定义在像素之间&#x200B;*插值*&#x200B;时如何处理取样结果：
  * *最接近的*：将对&#x200B;*相同的*&#x200B;值取样（较快）
  * *双线性*：将对&#x200B;*更平滑*&#x200B;外观的结果应用双线性的滤镜
  * *自动*：根据为裁剪选择的&#x200B;**模式**，使用上述两种模式中最合适的模式

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>
