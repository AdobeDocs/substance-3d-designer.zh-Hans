---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: 使用“多克隆修补”节点来克隆和修补多个纹理通道，以修复扫描的素材伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多克隆修补程序
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# 多克隆修补程序

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## 多克隆修补（灰度）

**在：** *材质筛选器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点是[克隆修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)的多输入版本。 它最多可将八个输入链接在一起，并在所有输入上执行完全相同的克隆修补程序操作。 它主要用于多角度照片，然后与[多角度至反照率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)或[多角度至法线](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)组合。

>[!NOTE]
>
> 请参阅[仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)以了解更多信息，请参阅[材质仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)以了解材质版本。

## 参数

### 参数

* **输入计数**： *1 - 8*&#x200B;设置将接收相同Patch操作的输入量。
* **正常（仅适用于颜色）**： **False/True**&#x200B;设置输入是否为正常映射，以及是否应将混合视为正常映射。
* **形状**： **正方形，磁盘**&#x200B;设置图章形状。 仅用作基础。
* **边缘**
  * **阈值**： *0.0 - 1.0*&#x200B;设置混合区域应达到的距离。 这沿着目标区域中的形状阶梯式增长；对于均匀的背景效果非常小*。*
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
