---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: 使用“裁剪”节点将材料输出裁剪到特定区域，以处理扫描材料和纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 裁剪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# 裁剪

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-10.png){width="128px"}

![](../../../../../../assets/crop-grayscale.png){width="128px"}

## 裁剪（灰度）

**在：** *材质筛选器/扫描处理*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

“裁剪”是熟悉的裁剪工具的参数化、非破坏性版本。 选择图像的一部分并返回结果，同时丢弃未选择的区域。

它在许多方面都很有用，因为对原子节点执行“裁剪”操作并不那么直接。 尤其是在变换非正方形图像时，这个节点就派上用场了。 在这种情况下，请确保正确设置输入分辨率。

要了解这一点非常重要，因为要轻松使用此节点，您必须充分利用预览与正在编辑的参数节点不同的节点的功能！\
简而言之，请&#x200B;**双击**&#x200B;用作此节点（未裁剪的原始图像）输入的节点，然后&#x200B;**单击**&#x200B;紧随其后的裁剪节点。 然后，您可以修改裁切小工具以适合要裁切的区域。

## 参数

* **输入大小**： *0 - 8192*&#x200B;输入图像的分辨率和比例。 对于非方形图像非常重要。
* **背景**： *（颜色值） /（灰度值）*未被“裁剪”覆盖的区域的背景统一值。
* **变换**： *（变换矩阵）*\
  旋转和缩放结果。 可以通过与画布直接交互来修改描摹结果。
* **偏移**： *0.0 - 1.0*\
  移动或转换结果。 可以通过与画布直接交互来修改描摹结果。
* **正常（仅适用于颜色版本）**： *False/True*&#x200B;是否应将输入视为正常映射。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
