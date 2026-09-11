---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: 使用材质裁剪节点从扫描的材质中裁剪纹理区域，以隔离特定兴趣区域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 素材裁剪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 素材裁剪

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-crop.resources/crop-material.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点是[裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)的多通道、完整素材版本。 它允许您对任意和所有材质通道并行执行裁剪操作。

>[!NOTE]
>
> [查看原始照片](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [了解更多信息。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 当使用“Specular/光泽度”映射而不是“金属/粗糙度”时，可打开和关闭此组中的素材通道。 |
| <b>输入大小</b> <i>0 - 8192</i> | 输入图像的分辨率和比例。 对于非方形图像非常重要。 |
| <b>背景</b> <i>（颜色值）/（灰度值）</i> | “裁剪”未覆盖的区域的背景统一值。 |
| <b>转换</b> <i>（转换矩阵）</i> | 旋转和缩放结果。 可以通过直接与画布交互来修改结果。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移动或转换结果。 可以通过直接与画布交互来修改结果。 |
