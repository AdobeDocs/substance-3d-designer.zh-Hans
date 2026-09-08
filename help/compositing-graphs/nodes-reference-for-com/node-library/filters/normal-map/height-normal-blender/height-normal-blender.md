---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: 使用“Height法线混合器”节点混合Height和法线图，以组合表面详细信息。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height标准混合器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Height标准混合器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Height标准混合器

**范围：** *筛选器/法线图*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

将灰度高图混合到正常映射上的快捷节点。 Height输入在内部转换为正常映射，然后与正常输入正确混合。

与手动对单独节点执行此操作相比，这是混合细节的一种更快的方式，但您可能会发现它缺乏对某些需求的控制和优化。

## 参数

### 输入

* **Height**： *灰度输入*\
  要混合的灰度高度图。
* **正常**： *颜色输入*\
  要混合到的基本正常映射。

### 参数

* **正常强度**： *0.0 - 16.0* Height输入的正常转换强度。
* **普通格式**： *DirectX，OpenGL*\
  在不同正常映射格式之间切换（反转绿色通道）。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
