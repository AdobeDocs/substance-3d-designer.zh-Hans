---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: 使用阴影滤镜节点通过输入纹理生成阴影效果，从而为材料增加深度和真实感。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 阴影(滤镜节点)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# 阴影(滤镜节点)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shadows-filter-node.resources/shadows-1.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

[形状投影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md)节点的原始纯灰度版本。 它仅将黑白二值形状作为输入并仅返回阴影。

如果您刚好位于阴影之后，不想处理更完整的节点（例如，构建自己的材料或烘焙的光照），则此功能将非常有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>阴影距离</b> <i>0.0 - 1.0</i> | 控制阴影应落至多远。 |
| <b>光线角度</b> <i>0.0 - 1.0</i> | 控制光线的入射角。 |
| <b>边缘柔和度</b> <i>0.0 - 1.0</i> | 确定阴影边缘的硬度或柔和程度。 |
| <b>示例</b> <i>1 - 16</i> | 设置“边缘柔和度”设置的品质。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shadows-filter-node.resources/shadow-ex.png" />
        </td>
    </tr>
</table>
