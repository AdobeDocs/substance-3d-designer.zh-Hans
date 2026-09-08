---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: 使用Snow覆盖节点，根据表面角度和位置，为材料添加积雪效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Snow封面
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Snow封面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

<b>进入：</b>材质过滤器>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一体式效果，可在整个材料上增加积雪。 强烈依赖于良好、高质量的高图（例如来自照片扫描的图像）。 结果旨在确保PBR正确。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭材料声道，例如，在使用Specular/光泽度映射而非金属/粗糙度时。 |
| <b>全新Snow</b> <i>0.0 - 1.0</i> | 在凸起区域设置雪量。 结果与熔化Snow参数有关。 |
| <b>融化的Snow</b> <i>0.0 - 1.0</i> | 设置降低转角处的融雪量。 |
| <b>累积</b> <i>0.0 - 1.0</i> | 主要影响Height输出，确定Height叠加效果。 |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | 设置根据积雪平滑Height细节。 |
| <b>薄片强度</b> <i>0.0 - 1.0</i> | 主要影响正常贴图、薄片细节的强度。 |
