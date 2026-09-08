---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# 克隆修补程序

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

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

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>正常（仅适用于颜色）</b> <i>False/True</i> | 设置输入是否为正常映射，以及是否应该将混合视为正常映射。 |
| <b>形状</b> <i>方形，磁盘</i> | 设置图章形状。 仅用作基础。 |
| <b>边缘</b> |  |
| <b>阈值</b> <i>0.0 - 1.0</i> | 设置混合区域应达到的距离。 这沿着目标区域中的形状逐步增长，对于均匀的背景<i>几乎没有影响。</i> |
| <b>模糊</b> <i>0.0 - 2.0</i> | 模糊图章区域的边缘，以备需要更柔和的过渡。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 磨圆图章形状的边缘，使轮廓更加流畅。 |
| <b>网格分辨率</b> <i>1 - 11</i> | 设置混合分析的质量分辨率。 值越高，混合越准确。 |
| <b>转换</b> |  |
| <b>源矩阵</b> <i>（转换矩阵）</i> | 变换源（缩放和旋转）。 无法在画布上完成，请仅通过这些参数更改。 |
| <b>源偏移</b> <i>-0.5 - 0.5</i> | 平移源位置。 无法在画布上完成，请仅通过这些参数更改。 <i>此参数可能是您要更改的主要参数！</i> |
| <b>目标矩阵</b> <i>（转换矩阵）</i> | 变换目标位置（缩放和旋转）。 也可通过画布上的小工具完成。 |
| <b>目标偏移</b> <i>-0.5 - 0.5</i> | 平移目标位置。 也可通过画布上的小工具完成。 |
