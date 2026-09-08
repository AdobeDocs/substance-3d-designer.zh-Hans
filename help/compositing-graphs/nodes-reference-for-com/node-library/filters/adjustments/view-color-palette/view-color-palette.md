---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: 使用“查看调色板”节点可以将从纹理中提取的调色板数据可视化以供分析。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 查看调色板
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# 查看调色板

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![量化颜色图标](../../../../../../assets/ViewColorPalette.png "量化颜色图标"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将调色板打包成方形或矩形，以便更轻松地在图形视图或2D视图中可视化。\
该打包旨在留出尽可能少的空位。

</td>
</tr>
</table>

调色板中的颜色顺序保持不变，颜色从左到右以及从上到下排列，类似于文本绕排。

此节点可用于可视化以下节点生成的调色板： [量化颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、[创建调色板](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)、[修改调色板](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>调色板</b> <i>颜色</i>主要 | 以像素行编码的RGB的有序列表。 调色板最多可包含256种颜色。   这是节点打包和渲染的调色板。 |
| <b>调色板颜色量</b> <i>整数</i> | 调色板中存储的颜色量。   如果该数值与“调色板”图像输入中实际颜色量不匹配，则可视化可能是不完整的，或者具有的空白槽比绝对必需的多。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>颜色</i> | 打包调色板的可视化。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![查看调色板：示例1](../../../../../../assets/view_color_palette_example_1.png "查看调色板：示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![查看调色板：示例2](../../../../../../assets/view_color_palette_example_2.png "查看调色板：示例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![查看调色板：示例3](../../../../../../assets/view_color_palette_example_3.png "查看调色板：示例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![查看调色板：示例4](../../../../../../assets/view_color_palette_example_4.png "查看调色板：示例4"){zoomable="yes"}

</td>
</tr>
</table>
