---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# 素材裁剪

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

## 素材裁剪

**在：** *材质筛选器/扫描处理*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点是[裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)的多通道、完整素材版本。 它允许您对任意和所有材质通道并行执行裁剪操作。

>[!NOTE]
>
> [查看原始照片](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [了解更多信息。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

## 参数

### 参数

* **频道**
  * 当使用“Specular/光泽度”映射而不是“金属/粗糙度”时，可打开和关闭此组中的素材通道。
* **输入大小**： *0 - 8192*&#x200B;输入图像的分辨率和比例。 对于非方形图像非常重要。
* **背景**： *（颜色值） /（灰度值）*未被“裁剪”覆盖的区域的背景统一值。
* **变换**： *（变换矩阵）*\
  旋转和缩放结果。 可以通过直接与画布交互来修改结果。
* **偏移**： *0.0 - 1.0*\
  移动或转换结果。 可以通过直接与画布交互来修改结果。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
