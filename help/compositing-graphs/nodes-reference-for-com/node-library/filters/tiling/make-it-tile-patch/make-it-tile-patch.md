---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: 使用Make It Tile Patch节点可从输入图像修补并创建无缝拼贴纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使其拼贴贴贴面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# 使其拼贴贴贴面

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## 使其平铺图案（灰度）

**范围：** *筛选器/拼贴*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点是基于网格的半随机拼贴。 它接受输入修补程序并四处盖印，尝试根据您的设置将它转换为拼贴图像，而不会重复过多。

当您有一小块纹理并希望从中创建更大尺寸的拼贴纹理时，非常有用

请记住，这不同于[Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)，后者主要修复边缘。

要对整个材料执行此操作，请参阅[智能自动磁贴](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)。

## 参数

* **蒙版大小**： *0.0 - 1.0*&#x200B;盖印修补程序时使用的圆形蒙版大小。
* **蒙版精度**： *0.0 - 1.0*&#x200B;蒙版的衰减/Smoothness精度。
* **蒙版变形**： *-100.0 - 100.0*&#x200B;在蒙版边缘引入变形。 适合避免曲面片之间平滑、未定义的过渡。
* **图案大小宽度**： *0.0 - 1000.0*&#x200B;将修补的宽度更改得不均匀。
* **图案大小Height**： *0.0 - 1000.0*&#x200B;将修补程序的Height更改为非一致的。
* **无序**： *0.0 - 1.0*\
  引入了平移随机性，略微移动斑块。
* **大小变化**： *0.0 - 100.0*&#x200B;引入蒙版的大小变化。
* **八度音阶**： *0 - 6*&#x200B;这是确定整体大小的主控件。
* **旋转**： *-360.0 - 360.0*&#x200B;预旋转修补程序。
* **旋转变化**： *0.0 - 360.0*&#x200B;为每个修补图章引入随机旋转。
* **背景颜色**： *（颜色值）*设置没有显示修补程序的区域的背景颜色。
* **颜色变化**： *0.0 - 1.0（仅限颜色版本）*引入每个修补的颜色变化。
* **明度变化** *（仅限灰度版本）*引入每个修补的明度变化。

## 示例图像

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>
