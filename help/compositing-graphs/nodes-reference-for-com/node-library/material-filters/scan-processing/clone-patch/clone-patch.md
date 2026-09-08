---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: 使用“仿制修补”节点可以克隆和修补扫描材料中的区域，以移除伪影和瑕疵。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 克隆修补程序
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# 克隆修补程序

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## 仿制修补/仿制修补灰度

**在：** *材质筛选器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

“仿制修补”是一个程序化的参数化“仿制图章”节点。 它会将输入的一个区域克隆到另一个区域，从而隐藏可能不需要的细节。 虽然这种方法不像使用基于画笔的应用程序中熟悉的工具那样快速和轻松，但它具有非破坏性和在基于节点的工作流程中工作的主要优势。 此外，该节点对目标区域和源区域执行智能分析，并尝试基于对比度、值和形状尽可能好地混合对象。

这主要适用于您想要手动修复特定区域的罕见时刻，以防某个位置出现不需要的细节。

请记住，这不同于标准的简单“图章”画笔。 混合区域的形状基于您正在处理的区域的形状和值，这意味着这是一个相当大的节点，需要耐心，但可以带来出色的效果。

同样重要的是要了解的是，您可以使用小工具移动目标区域，但需要通过更改“源矩阵”参数来设置源区域。

>[!NOTE]
>
> 如果您希望将其用于完整材料（通常如此），请参阅[材料仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)。
> 
> 如果要同时对多个输入执行此操作（不作为材料），请参阅[多仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)。

## 参数

* **正常（仅适用于颜色）**： *False/True*\
  设置输入是否为正常映射，以及是否应该将混合视为正常映射。
* **形状**： *正方形，磁盘*&#x200B;设置图章形状。 仅用作基础。
* **边缘**
  * **阈值**： *0.0 - 1.0*&#x200B;设置混合区域应达到的距离。 这沿着目标区域中的形状逐步增长，对于均匀的背景几乎没有影响*。*
  * **模糊**： *0.0 - 2.0*&#x200B;模糊图章区域的边缘，以备需要更柔和的过渡。
  * **Smoothness**： *0.0 - 2.0*&#x200B;磨圆图章形状的边缘，使轮廓更加流畅。
  * **网格分辨率**： *1 - 11*&#x200B;设置混合分析的质量分辨率。 值越高，混合越准确。
* **转换**
  * **源矩阵**： *（变换矩阵）*变换源（缩放和旋转）。 无法在画布上完成，请仅通过这些参数更改。
  * **源偏移**： *-0.5 - 0.5*&#x200B;平移源位置。 无法在画布上完成，请仅通过这些参数更改。 *此参数可能是您要更改的主要参数！*
  * **目标矩阵**： *（变换矩阵）*变换目标位置（缩放和旋转）。 也可通过画布上的小工具完成。
  * **目标偏移**： *-0.5 - 0.5*&#x200B;平移目标位置。 也可通过画布上的小工具完成。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
