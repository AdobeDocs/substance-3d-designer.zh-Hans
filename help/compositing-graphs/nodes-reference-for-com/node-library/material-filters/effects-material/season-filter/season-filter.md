---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: 使用季节滤镜节点对材料应用季节性效果，打造春季、夏季、秋季和冬季变体。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 季节过滤器
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# 季节过滤器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>进入：</b>材质过滤器>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点添加效果，如动画水位、雪、冰和/或苔藓。

请记住，这是旧版滤镜，并不旨在完全符合PBR要求。 保留它主要是出于旧版/兼容性原因，尽管它在某些情况下仍然很有用。 在[Snow封面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)和[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)中可以找到更新的PBR校正版本。

节点需要一组适当的材料输入，主要带有非常详细的Heightmap或Normalmap。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭材料声道，例如，在使用Specular/光泽度映射而非金属/粗糙度时。 |
| <b>高级</b> |  |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>蒙版</b> <i>False/True</i> | 启用或禁用蒙版图。 |
| <b>光照强度</b> <i>0.0 - 1.0</i> | （虚假）光线的强度。 |
| <b>光线角度</b> <i>0.0 - 1.0</i> | （虚假）光的入射角 |
| <b>效果</b> |  |
| <b>来自Height或普通的效果</b> <i>Height，正常</i> | 选择驱动效果的输入图。 |
| <b>水位</b> <i>0.0 - 1.0</i> | 根据Height/正常信息升高或降低水位。 |
| <b>水细节</b> <i>0.0 - 1.0</i> | 设置水中的细节量。 |
| <b>折射</b> <i>0.0 - 1.0</i> | 设置效果中的伪折射量。 |
| <b>反射</b> <i>0.0 - 1.0</i> | 设置效果中的虚假反射量。 |
| <b>反射距离</b> <i>0.0 - 1.0</i> | 控制反射视觉效果。 |
| <b>反射角度</b> <i>0.0 - 1.0</i> | 控制反射视觉效果。 |
| <b>流动方向</b> <i>0.0 - 1.0</i> | 控制动画流（使用Substance Player进行可视化）。 |
| <b>冰</b> <i>0.0 - 1.0</i> | 设置水的冻结程度。 |
| <b>冰详细信息</b> <i>0.0 - 1.0</i> | 设置冰的细节量。 |
| <b>Snow</b> <i>0.0 - 1.0</i> | 设置雪覆盖量。 |
| <b>苔藓</b> <i>0.0 - 1.0</i> | 设置苔藓覆盖范围的数量。 |
| <b>苔藓缩放</b> <i>1 - 4</i> | 设置所生成苔藓纹理的比例。 |
| <b>苔藓颜色</b> <i>（颜色值）</i> | 设置苔藓的颜色。 |
| <b>水彩</b> <i>（颜色值）</i> | 设置水的颜色，包括Alpha/不透明度。 |
| <b>混合</b> |  |
| <b>Diffuse强度</b> <i>0.0 - 1.0</i> | 扩散的混合强度。 |
| <b>Base color强度</b> <i>0.0 - 1.0</i> | 混合基色的强度。 |
| <b>正常强度</b> <i>0.0 - 1.0</i> | 混合“正常”的强度。 |
| <b>Specular强度</b> <i>0.0 - 1.0</i> | 混合Specular的强度。 |
| <b>光泽度强度</b> <i>0.0 - 1.0</i> | 混合光泽度的强度。 |
| <b>粗糙度强度</b> <i>0.0 - 1.0</i> | 混合粗糙度的强度。 |
| <b>Ambient occlusion强度</b> <i>0.0 - 1.0</i> | 混合环境遮蔽的强度。 |
| <b>Height强度</b> <i>0.0 - 1.0</i> | 混合强度。 |
