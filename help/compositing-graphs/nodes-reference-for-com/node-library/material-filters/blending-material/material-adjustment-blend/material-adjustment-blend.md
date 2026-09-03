---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: 使用材料调整混合节点可在材料之间混合材料调整，以微调复合效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 素材调整混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# 素材调整混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend-01.png){width="128px"}

<b>进入：</b>材质过滤器>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点允许基于蒙版调整完整材料的任意和所有通道。 它旨在使完整的材料工作流程更轻松、更快速。

当您要基于同一蒙版调整材料的几个声道（例如，使扩散更亮、粗糙度更暗）时，此效果非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>色彩 ID 蒙版</b> <i>颜色输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>灰度蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭材料通道，例如，使用Specular/光泽度映射而非金属/粗糙度时。<br><br>这也会启用和禁用通道相关组的外观。 |
| <b>扩散</b> | 在蒙版定义的区域中，对Diffuse通道执行调整操作。 |
| <b>基色</b> | 在蒙版定义的区域中，对Base color通道执行调整操作。 |
| <b>正常</b> |  |
| <b>强度</b> <i>0.0 - 1.0</i> | 调暗正常强度 |
| <b>Specular</b> | 在蒙版定义的区域中，对Specular通道执行调整操作。 |
| <b>具发射性</b> | 在蒙版定义的区域中，对发射通道执行调整操作。 |
| <b>光泽度</b> | 在蒙版定义的区域中，对光泽度通道执行调整操作。 |
| <b>粗糙度</b> | 在蒙版定义的区域中，对粗糙度通道执行调整操作。 |
| <b>金属</b> | 在蒙版定义的区域中，对金属通道执行调整操作。 |
| <b>Specular level</b> | 在蒙版定义的区域中，对Specular level通道执行调整操作。 |
| <b>Ambient occlusion</b> | 在蒙版定义的区域中，对Ambient occlusion通道执行调整操作。 |
| <b>Height</b> | 在蒙版定义的区域中，对Height通道执行调整操作。 |
| <b>不透明度</b> | 在不透明度通道上，在蒙版定义的区域中执行调整操作。 |
| <b>色彩 ID 蒙版</b> <i>False/True</i> | 设置为使用色彩 ID 蒙版而非灰度蒙版。 |
| <b>模糊</b> <i>0.01 - 1.0</i> | 如果启用了“色彩 ID 蒙版”，则会确定Color ID选择颜色的跨页。 |
| <b>颜色</b> <i>（颜色值）</i> | 设置要从颜色Id 图和蒙版中选择的颜色。 |
| <b>填充</b> <i>0.0 - 1.0</i> | 确定颜色ID蒙版的混合对比度/过渡。 |
