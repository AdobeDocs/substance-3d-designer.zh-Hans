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
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hald-clut.resources/hald-clut.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在输入图像上应用LUT。 LUT必须为Hald格式，分辨率为4096\*4096。 有关详细信息，请参阅<http://www.quelsolaar.com/technology/clut.html>。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色输入</i> | 要应用LUT的图像。 |
| <b>lut</b> <i>颜色输入</i> | Lut输入插槽。 必须为4096x4096。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>按Alpha排列的LUT强度</b> <i>False/True</i> | 定义LUT效果是否由Alpha 通道加权。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="hald-clut.resources/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
