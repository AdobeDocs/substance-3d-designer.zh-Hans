---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: 使用三平面节点从三个正交平面投影纹理，以便在复杂几何上无缝映射纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三平面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# 三平面

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## 三平面（灰度）

**在：** *基于网格的生成器**/Utilities*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

该高级节点基于烘焙位置和世界空间法线数据在2D空间中执行三平面投影映射。 这意味着，它基本上可以完全将UV坐标转换为基于网格本身的无接缝贴图。

这是避免接缝的好方法，不必每次都重新烘焙（与烘焙商类似的方法是可以实现的）。 缺点是这个节点很重，所以速度不快。

请记住，您的烤盘应具有高精度：8位烤盘不会产生非常好的效果。

## 参数

### 输入

* **位置**： *颜色输入*\
  烘焙位置图。 理想情况下为16位或更高的精度。
* **正常世界空间**： *颜色输入*\
  烘焙世界空间法线图，理想为16位或更高的精度。
* **输入X**： *颜色输入（灰度输入）*输入映射，用于通过三面投影从UV重新映射到世界空间。 当“图像输入”设置为1时，适用于所有轴；如果设置为3，则适用于X轴。
* **输入Y**： *颜色输入（灰度输入）*仅当图像输入设置为3时。 输入映射，用于将UV重新映射到Y轴上的世界空间。
* **输入Z**： *颜色输入（灰度输入）*仅当图像输入设置为3时。 输入映射，用于将UV重新映射到Z轴上的世界空间。

### 参数

* **投影**：*所有轴，仅限X、仅限Y、仅限Z*&#x200B;设置要混合的轴。
* **图像输入**： *1个输入，3个输入*\
  设置是为所有轴使用一个映射，还是为每个轴使用特定映射。
* **混合模式**：*线性、高级*&#x200B;提高准确度和精度。
* **混合对比度**： *0.001 - 1.0*&#x200B;过渡对比度，在平滑或粗糙过渡之间混合。
* **规范化因子**： *0.0 - 1.0*\
  通过恢复混合区域的对比度损失来改进投影混合。
* **纹理拼贴**： *0.0 - 10.0*&#x200B;拼贴输入纹理的次数。
* **全局轮换**： *0.0 - 1.0*\
  所有轴的全局旋转。
* **修复镜像投影**： *False/True*&#x200B;设置如何处理镜像投影。
* **旋转X**： *0.0 - 1.0*&#x200B;在投影X轴上单独旋转。
* **旋转Y**： *0.0 - 1.0*&#x200B;在投影Y轴上单独旋转。
* **旋转Z**： *0.0 - 1.0*&#x200B;在投影Z轴上单独旋转。
* **偏移X**： *0.0 - 1.0*&#x200B;对投影X轴的偏移。
* **随机偏移X**： *0.0 - 1.0*\
  允许X轴偏移的随机化。
* **偏移Y**： *0.0 - 1.0*&#x200B;对投影Y轴的偏移。
* **随机偏移Y**： *0.0 - 1.0*\
  允许Y轴偏移的随机化。
* **偏移Z**： *0.0 - 1.0*&#x200B;对投影Z轴的偏移。
* **随机偏移Z**： *0.0 - 1.0*\
  允许Z轴偏移的随机化。

## 示例图像

</td>
</tr>
</table>
