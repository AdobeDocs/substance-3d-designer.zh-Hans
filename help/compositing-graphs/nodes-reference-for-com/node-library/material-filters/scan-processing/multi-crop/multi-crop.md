---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: 使用“多裁剪”节点同时裁剪多个纹理通道，以便高效地处理扫描的材料。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多裁剪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# 多裁剪

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-crop.resources/multi-crop-01.png){width="128px"}

![](multi-crop.resources/multi-crop-02.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这是Crop的多通道版本。 它从图像中裁剪出一个区域，主要用于多角度照片，然后与[多角度到反照率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)或[多角度到法线](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)组合。

>[!NOTE]
>
> 有关详细信息，请参阅原始的[裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输入计数</b> <i>1 - 8</i> | 设置要并行处理的输入数。 |
| <b>输入大小</b> <i>0 - 8192</i> | 输入图像的分辨率和比例。 对于非方形图像非常重要。 |
| <b>背景</b> <i>（颜色值）/（灰度值）</i> | “裁剪”未覆盖的区域的背景统一值。 |
| <b>变换</b> <i>（转换矩阵）</i> | 旋转和缩放结果。 可以通过与画布直接交互来修改描摹结果。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移动或转换结果。 可以通过与画布直接交互来修改描摹结果。 |
| <b>正常（仅适用于颜色版本）</b> <i>False/True</i> | 是否应将输入视为正常映射。 |
