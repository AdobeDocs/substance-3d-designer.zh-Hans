---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: 使用“仿制修补”节点可以克隆和修补纹理区域，以修复扫描材料中的伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材质仿制修补
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# 仿制修补程序

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-clone-patch.resources/material-clone-patch-01.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这是[仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)的多通道、完整材料版本。 它会对材料的任意和所有通道执行仿制修补。 [有关详细信息，请参阅原始版本！](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

如果要从材料的所有通道中删除细节，这会非常有用。 输出多个通道的调试图像，以查看智能修补区域的确切外观。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭材料声道，例如，在使用Specular/光泽度映射而非金属/粗糙度时。 |
| <b>形状</b> <i>方形，磁盘</i> | 设置图章形状。 仅用作基础。 |
| <b>边缘</b> |  |
| <b>阈值（适用于多个通道）</b> <i>0.0 - 1.0</i> | 设置混合区域应达到的距离。 这种效果是分阶段生长的，沿目标区域中的形状生长，因此对于均匀背景的影响非常小。 请注意在通道之间过度更改此设置，因为这可能会导致视觉差异！ |
| <b>模糊</b> <i>0.0 - 2.0</i> | 模糊图章区域的边缘，以备需要更柔和的过渡。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 磨圆图章形状的边缘，使轮廓更加流畅。 |
| <b>网格分辨率</b> <i>1 - 11</i> | 设置混合分析的质量分辨率。 值越高，混合越准确。 |
| <b>转换</b> |  |
| <b>源矩阵</b> <i>（转换矩阵）</i> | 变换源（缩放和旋转）。 无法在画布上完成，请仅通过这些参数更改。 |
| <b>源偏移</b> <i>-0.5 - 0.5</i> | 平移源位置。 无法在画布上完成，请仅通过这些参数更改。 *此参数可能是您要更改的主要参数！* |
| <b>目标矩阵</b> <i>（转换矩阵）</i> | 变换目标位置（缩放和旋转）。 也可通过画布上的小工具完成。 |
| <b>目标偏移</b> <i>-0.5 - 0.5</i> | 平移目标位置。 也可通过画布上的小工具完成。 |
