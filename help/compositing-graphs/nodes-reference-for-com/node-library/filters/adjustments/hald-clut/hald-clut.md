---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: 使用Hald CLOT节点可应用颜色查找表，并使用Hald CLOT格式进行颜色分级和校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## Hald CLUT

**范围：** *滤镜/调整*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在输入图像上应用LUT。 LUT必须为Hald格式，分辨率为4096\*4096。 有关详细信息，请参阅<http://www.quelsolaar.com/technology/clut.html>。

### 输入

* **输入**： *颜色输入*\
  要应用LUT的图像。
* **lut**： *颜色输入* Lut输入槽。 必须为4096x4096。

## 参数

* **按Alpha排列的LUT强度**： *False/True*&#x200B;定义LUT效果是否由Alpha通道加权。

示例

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>
