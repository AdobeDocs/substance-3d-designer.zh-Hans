---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Height标准混合器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-normal-blender.resources/height-normal-blender-01.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将灰度海图图混合到正常映射上的快捷键节点。 Height输入在内部转换为正常映射，然后与正常输入正确混合。

与手动对单独节点执行此操作相比，这是混合细节的一种更快的方式，但您可能会发现它缺乏对某些需求的控制和优化。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Height</b> <i>灰度输入</i> | 要混合的灰度高度图。 |
| <b>正常</b> <i>颜色输入</i> | 要混合到的基本正常映射。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>正常强度</b> <i>0.0 - 16.0</i> | Height输入的正常转换的强度。 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
