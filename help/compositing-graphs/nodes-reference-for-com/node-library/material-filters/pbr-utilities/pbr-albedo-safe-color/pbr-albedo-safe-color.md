---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: 使用“PBR反照率安全颜色”节点可确保反照率位于PBR素材物理上合理的范围内。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR反照率安全颜色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# PBR反照率安全颜色

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

## PBR反照率安全颜色

**在：** *材质滤镜/PBR实用工具*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

这是一个实用节点，如果“基色”或“漫射”值位于可接受的PBR校正范围之外，则会进行校正。 在设置为“金属”时，节点还会尝试根据“金属”强度校正“基色”值。

另请参阅[PBR BaseColor/金属验证](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md)，以获取有关哪些区域可能出错的视觉反馈。

作为一种快速校正工具，此功能非常有用，尤其是在用户仍在学习PBR时，但不打算将其用作始终应正确使用的绝对测量单位。

## 参数

* **PBR工作流程**： *基色 — 金属、扩散 — Specular*&#x200B;在两种不同的PBR工作流程之间切换。
* **容差**： *0.0 - 1.0*&#x200B;超出范围的值的容差量。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
