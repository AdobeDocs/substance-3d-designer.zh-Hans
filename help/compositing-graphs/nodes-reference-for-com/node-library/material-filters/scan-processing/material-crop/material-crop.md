---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: 使用材料裁剪节点裁剪扫描材料中的纹理区域，以隔离特定兴趣区域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材料裁剪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# 材料裁剪

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

## 材料裁剪

**位置：** *材质过滤器/扫描处理*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点是[裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)的多通道、完整材料版本。 它允许您并行对任意和所有材料声道执行裁剪操作。

>[!NOTE]
>
> [查看原始照片](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [了解更多信息。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

## 参数

### 参数

* **频道**
  * 例如，在使用Specular/光泽度映射而非金属/粗糙度时，可打开和关闭此组中的材料通道。
* **输入大小**： *0 - 8192*&#x200B;输入图像的分辨率和比例。 对于非方形图像非常重要。
* **背景**： *（颜色值） /（灰度值）*未被“裁剪”覆盖的区域的背景统一值。
* **变换**： *（转换矩阵）*\
  旋转和缩放结果。 可以通过直接与画布交互来修改结果。
* **偏移**： *0.0 - 1.0*\
  移动或平移结果。 可以通过直接与画布交互来修改结果。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
