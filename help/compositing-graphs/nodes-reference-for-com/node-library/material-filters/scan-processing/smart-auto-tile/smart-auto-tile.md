---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: 使用智能自动拼贴节点，可通过智能图案检测，自动从扫描的素材创建无缝拼贴。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 智能自动平铺
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# 智能自动平铺

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## 智能自动平铺

**在：** *材质筛选器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点根据对输入的智能分析，将一组非拼贴的Basecolor、Normal和Heightmap转换为拼贴版本。 它类似于[使其平铺照片](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)，但更高级，因为它使用来自所有通道的信息以最智能的方式将内容混合在一起（类似于[仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)的功能）。 它还具有内部[裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)功能，用于确定拼贴时要使用的区域 — 请确保[详细阅读裁剪节点](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)，以正确了解此功能。

要使用此节点，请先定义裁剪区域，然后使用“边缘”设置来确定拼贴边缘混合到中心的方式。 Treshold参数对此至关重要！ 请记住，大的统一区域对这种效果并不太有效；其中的细节和形状越多，就越需要处理。

## 参数

### 输入

* **蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。 可以使用“使用蒙版”参数切换。

### 参数

* **裁剪**
  * **输入大小**： *0 - 8192*&#x200B;输入图像的分辨率和比例。 对于非方形图像非常重要。
  * **变换**： *（变换矩阵）*\
    旋转和缩放结果。 可以通过与画布直接交互来修改描摹结果。
  * **偏移**： *0.0 - 1.0*\
    移动或转换结果。 可以通过与画布直接交互来修改描摹结果。
* **边缘**
  * **检测边缘**： *False/True*&#x200B;打开或关闭检测到的特殊边缘混合。
  * **使用每个通道的阈值**： *False/True*&#x200B;在全局阈值之间切换，或为每个通道切换一个阈值。
  * **阈值**： *0.0 - 1.0*
  * **阈值基色**： *0.0 - 1.0*
  * **阈值正常**： *0.0 - 1.0*
  * **阈值Height**： *0.0 - 1.0*
  * **切削偏移**： *0.0 - 0.5*&#x200B;移动切削的主控件，X轴和Y轴分开。
  * **模糊**： *0.0 - 2.0*&#x200B;模糊混合过渡。
  * **Smoothness**： *0.0 - 2.0*&#x200B;控制边缘分析结果的跳跃程度。
  * **网格分辨率**： *1 - 11*&#x200B;边缘分析的质量分辨率。
  * **使用基色**： *False/True*&#x200B;切换基色处理（入点和出点）。
  * **使用普通**： *False/True*&#x200B;切换正常处理（入点和出点）。
  * **使用Height**： *False/True*&#x200B;切换正常处理（入点和出点）。
  * **使用蒙版**： *False/True*\
    为自定图章蒙版形状切换蒙版映射的使用开关。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
