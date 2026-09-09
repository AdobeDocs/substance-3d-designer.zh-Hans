---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: 使用“创建调色板”节点从纹理中提取16色调色板以获得风格化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建调色板(16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# 创建调色板(16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![量化颜色图标](create-color-palette-16.resources/CreateColorPalette16.png "量化颜色图标"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

创建颜色的有序列表，并将它输出为最多具有16种颜色的调色板。

节点可以使用“调色板”输入集将新颜色附加到现有调色板中。

此节点可以与以下节点结合使用： [量化颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、[应用调色板](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md)、[修改调色板](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)、[查看调色板](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>调色板</b> <i>颜色</i>主要 | 以像素行编码的RGB的有序列表。 调色板最多可包含256种颜色。   此输入是可选的。 如果使用，则节点设置的颜色将附加到此调色板中。   可以使用[查看调色板](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)节点来可视化调色板。 |
| <b>调色板颜色量</b> <i>整数</i> | 调色板中存储的颜色量。   如果该数值与“调色板”图像输入中实际颜色量不匹配，则可视化可能是不完整的，或者具有的空白槽比绝对必需的多。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>调色板</b> <i>颜色</i> | 追加了指定颜色的更新调色板。 |
| <b>调色板颜色量</b> <i>整数</i> | 组件面板中存储的颜色的更新量，以及添加到组件面板中的指定颜色量。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>颜色量</b> *整数* | 应添加到调色板的颜色量。 |
| <b>颜色#</b> *浮点3* *可用参数数量与“颜色量”值相同* | 应添加到调色板中的颜色。   颜色会按照此编号列表的顺序附加到调色板。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![创建调色板：示例1](create-color-palette-16.resources/create_color_palette_example_1.png "创建调色板：示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![创建调色板：示例2](create-color-palette-16.resources/create_color_palette_example_2.png "创建调色板：示例2"){zoomable="yes"}

</td>
</tr>
</table>

![创建调色板：示例3](create-color-palette-16.resources/create_color_palette_example_3.png "创建调色板：示例3"){zoomable="yes"}
