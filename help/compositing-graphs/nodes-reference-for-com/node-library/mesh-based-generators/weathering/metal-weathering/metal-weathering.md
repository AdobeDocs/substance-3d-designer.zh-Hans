---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: 使用金属风化节点，可根据网格几何形状为金属材料添加逼真的铁锈和腐蚀效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金属风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# 金属风化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-weathering.resources/metal-weathering.png){width="128px"}

<b>在</b>中基于网格的生成器>风化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>正常WS</b> <i>颜色输入</i> | 用于内部效果和蒙版的烘焙世界空间正常映射。 |
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 |
| <b>高级</b> |  |
| <b>正常格式</b> <i>Direct X， Open GL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>蒙版</b> <i>False/True</i> | 启用或禁用蒙版图。 |
| <b>效果</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>污迹</b> <i>0.0 - 1.0</i> |  |
| <b>边缘磨损</b> <i>0.0 - 1.0</i> |  |
| <b>绘画剥落</b> <i>0.0 - 1.0</i> |  |
| <b>铁锈</b> <i>0.0 - 1.0</i> |  |
| <b>铁锈剥落</b> <i>0.0 - 1.0</i> |  |
| <b>铁锈Verdigris</b> <i>铁锈，Verdigris</i> |  |
| <b>裂缝缩放</b> <i>1.0 - 16.0</i> |  |
| <b>裂缝变形强度</b> <i>0.0 - 1.0</i> |  |
| <b>锐边Scratches缩放</b> <i>1.0 - 32.0</i> |  |
| <b>锐边Scratches变形强度</b> <i>0.0 - 1.0</i> |  |
| <b>原始金属颜色</b> <i>（颜色值）</i> |  |
| <b>原始金属Specular颜色</b> <i>（颜色值）</i> |  |
| <b>原始金属光泽度值</b> <i>（灰度值）</i> |  |
| <b>原始金属粗糙度值</b> <i>（灰度值）</i> |  |
| <b>混合</b> |  |
| <b>Diffuse强度</b> <i>0.0 - 1.0</i> | 扩散的混合强度。 |
| <b>Base color强度</b> <i>0.0 - 1.0</i> | 混合基色的强度。 |
| <b>正常强度</b> <i>0.0 - 64.0</i> | 混合“正常”的强度。 |
| <b>Specular强度</b> <i>0.0 - 1.0</i> | 混合Specular的强度。 |
| <b>光泽度强度</b> <i>0.0 - 1.0</i> | 混合光泽度的强度。 |
| <b>粗糙度强度</b> <i>0.0 - 1.0</i> | 混合粗糙度的强度。 |
| <b>金属强度</b> <i>0.0 - 1.0</i> | 混合金属强度。 |
| <b>Ambient occlusion强度</b> <i>0.0 - 1.0</i> | 混合环境遮蔽的强度。 |
| <b>Height强度</b> <i>0.0 - 1.0</i> | 混合Height的强度。 |
