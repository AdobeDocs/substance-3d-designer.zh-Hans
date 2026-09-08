---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: 使用“智能自动拼贴”节点，可通过智能模式检测，自动从扫描的材料创建无缝拼贴。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 智能自动平铺
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# 智能自动平铺

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点根据对输入的智能分析，将一组非拼贴的Basecolor、Normal和Heightmap转换为拼贴版本。 它类似于[使其平铺照片](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)，但更高级，因为它使用来自所有通道的信息以最智能的方式将内容混合在一起（类似于[仿制修补](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)的功能）。 它还具有内部[裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)函数，用于确定在拼贴时要使用的区域 — 请确保[阅读有关裁剪节点的更多信息](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)，以正确了解此函数。

要使用此节点，请先定义裁剪区域，然后使用“边缘”设置来确定拼贴边缘混合到中心的方式。 Treshold参数对此至关重要！ 请记住，大的统一区域对这种效果并不太有效；其中的细节和形状越多，就越需要处理。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“使用蒙版”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>裁剪</b> |  |
| <b>输入大小</b> <i>0 - 8192</i> | 输入图像的分辨率和比例。 对于非方形图像非常重要。 |
| <b>转换</b> <i>（转换矩阵）</i> | 旋转和缩放结果。 可以通过与画布直接交互来修改描摹结果。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移动或转换结果。 可以通过与画布直接交互来修改描摹结果。 |
| <b>边缘</b> |  |
| <b>检测边缘</b> <i>False/True</i> | 打开或关闭检测到的特殊边缘混合。 |
| <b>使用每个通道的阈值</b> <i>False/True</i> | 在全局阈值或每个通道一个阈值之间切换。 |
| <b>阈值</b> <i>0.0 - 1.0</i> |  |
| <b>阈值Base color</b> <i>0.0 - 1.0</i> |  |
| <b>阈值正常</b> <i>0.0 - 1.0</i> |  |
| <b>阈值Height</b> <i>0.0 - 1.0</i> |  |
| <b>切割偏移</b> <i>0.0 - 0.5</i> | 用于移动切割的主控制器，X和Y轴都被分离。 |
| <b>模糊</b> <i>0.0 - 2.0</i> | 模糊混合过渡。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 控制边缘分析结果的跳度。 |
| <b>网格分辨率</b> <i>1 - 11</i> | 边缘分析的质量分辨率。 |
| <b>使用Base color</b> <i>False/True</i> | 切换Base color处理（入点和出点）。 |
| <b>使用普通</b> <i>False/True</i> | 切换正常处理（入点和出点）。 |
| <b>使用Height</b> <i>False/True</i> | 切换正常处理（入点和出点）。 |
| <b>使用蒙版</b> <i>False/True</i> | 为自定图章蒙版形状切换蒙版映射的使用开关。 |
