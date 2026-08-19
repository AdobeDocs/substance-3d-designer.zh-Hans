---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: 使用材质仿制修补节点可仿制和修补纹理区域，以修复扫描材质中的伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质仿制修补
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# 材质仿制修补

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## 材质仿制修补

**在：** *材质筛选器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

这是[克隆修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)的多通道、完整材质版本。 它会对素材的任何和所有通道执行仿制修补。 [有关详细信息，请参阅原始版本！](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

如果要从材质的所有通道中删除细节，这将非常有用。 输出多个通道的调试图像，以查看智能修补区域的确切外观。

## 参数

### 输入

* **蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。

### 参数

* **频道**
  * 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **形状**： *正方形，磁盘*&#x200B;设置图章形状。 仅用作基础。
* **边缘**
  * **阈值（适用于多个通道）**： *0.0 - 1.0*&#x200B;设置混合区域应达到的距离。 这沿着目标区域中的形状逐步增长，因此它对均匀背景的影响非常小*。*注意在通道之间过多地更改此项，因为这可能会导致视觉差异！
  * **模糊**： *0.0 - 2.0*&#x200B;模糊图章区域的边缘，以备需要更柔和的过渡。
  * **Smoothness**： *0.0 - 2.0*&#x200B;磨圆图章形状的边缘，使轮廓更加流畅。
  * **网格分辨率**： *1 - 11*&#x200B;设置混合分析的质量分辨率。 值越高，混合越准确。
* **转换**
  * **源矩阵**： *（变换矩阵）*变换源（缩放和旋转）。 无法在画布上完成，请仅通过这些参数更改。
  * **源偏移**： *-0.5 - 0.5*&#x200B;转换源位置。 无法在画布上完成，请仅通过这些参数更改。 *此参数可能是您要更改的主要参数！*
  * **目标矩阵**： *（变换矩阵）*变换目标位置（缩放和旋转）。 也可通过画布上的小工具完成。
  * **目标偏移**： *-0.5 - 0.5*&#x200B;翻译目标位置。 也可通过画布上的小工具完成。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
