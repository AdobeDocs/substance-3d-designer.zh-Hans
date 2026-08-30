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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# 多克隆修补程序

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/clone-patch-multi.png){width="128px"}

![](multi-clone-patch.resources/clone-patch-multi-grayscale.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点是[克隆修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)的多输入版本。 它最多可将八个输入链接在一起，并在所有输入上执行完全相同的克隆修补程序操作。 它主要用于多角度照片，然后与[多角度至反照率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)或[多角度至法线](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)组合。

>[!NOTE]
>
> 请参阅[仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)以了解更多信息，请参阅[材质仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)以了解材质版本。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输入计数</b> <i>1 - 8</i> | 设置将接收相同修补程序操作的输入量。 |
| <b>正常（仅适用于颜色）</b> <i>False/True</i> | 设置输入是否为正常映射，以及是否应该将混合视为正常映射。 |
| <b>形状</b> <i>方形，磁盘</i> | 设置图章形状。 仅用作基础。 |
| <b>边缘</b> |  |
| <b>阈值</b> <i>0.0 - 1.0</i> | 设置混合区域应达到的距离。 这沿着目标区域中的形状阶梯式增长；对于均匀的背景效果非常小。 |
| <b>模糊</b> <i>0.0 - 2.0</i> | 模糊图章区域的边缘，以备需要更柔和的过渡。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 磨圆图章形状的边缘，使轮廓更加流畅。 |
| <b>网格分辨率</b> <i>1 - 11</i> | 设置混合分析的质量分辨率。 值越高，混合越准确。 |
| <b>转换</b> |  |
| <b>源矩阵</b> <i>（转换矩阵）</i> | 变换源（缩放和旋转）。 无法在画布上完成，请仅通过这些参数更改。 |
| <b>源偏移</b> <i>-0.5 - 0.5</i> | 平移源位置。 无法在画布上完成，请仅通过这些参数更改。 *此参数可能是您要更改的主要参数！* |
| <b>目标矩阵</b> <i>（转换矩阵）</i> | 变换目标位置（缩放和旋转）。 也可通过画布上的小工具完成。 |
| <b>目标偏移</b> <i>-0.5 - 0.5</i> | 平移目标位置。 也可通过画布上的小工具完成。 |
