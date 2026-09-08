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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Snow封面

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Snow封面

**范围：** *材质过滤器/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

一体式效果，可在整个材料上增加积雪。 强烈依赖于良好、高质量的高图（例如来自照片扫描的图像）。 结果旨在确保PBR正确。

## 参数

### 输入

* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **频道**\
  在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **新鲜Snow**： *0.0 - 1.0*&#x200B;在凸起区域设置雪量。 结果与熔化Snow参数有关。
* **融化的Snow**： *0.0 - 1.0*&#x200B;设置低角处融化的雪量。
* **累积**： *0.0 - 1.0*&#x200B;主要影响Height输出，确定Height累加效果。
* **Smoothness**： *0.0 - 1.0*&#x200B;设置雪花栈积对Height细节的平滑处理。
* **薄片强度**： *0.0 - 1.0*&#x200B;主要影响正常贴图，即薄片细节的强度。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
