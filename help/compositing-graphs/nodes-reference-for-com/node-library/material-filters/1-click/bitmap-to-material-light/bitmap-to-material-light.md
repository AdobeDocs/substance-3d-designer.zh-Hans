---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: 使用“位图转换为材质光照”节点可以将位图图像快速转换为具有优化光照的材质，从而实现快速工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 将位图转换为材质光照
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# 将位图转换为材质光照

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

<b>在</b>个材质过滤器中>一键式

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点将单个漫射/基色输入转换为完整素材。 作为[Allegorithmic完全成熟的Bitmap2素材的简单“浅色”版本（可单独购买）](https://www.allegorithmic.com/products/bitmap2material)，它为您提供了完整版本的些许体验。 对于较简单的情形，它可以很好地工作。

虽然无法保证生成完美的PBR校正素材，但如果您只有一个图像并且需要完整的素材，这是一种好且快速入门的方法。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 |
| <b>全局</b> |  |
| <b>深度平衡</b> <i>-1.0 - 1.0</i> | 为Heightmap设置偏移。 |
| <b>扩散</b> |  |
| <b>锐化</b> <i>0.0 - 1.0</i> | 向扩散结果添加锐化。 |
| <b>色相</b> <i>0.0 - 1.0</i> | 色调因用户选择的色相偏移而扩散。 |
| <b>饱和度</b> <i>0.0 - 1.0</i> | 修改Diffuse结果的饱和度。 |
| <b>亮度</b> <i>0.0 - 1.0</i> | 调整Diffuse结果亮度。 |
| <b>对比度</b> <i>-1.0 - 1.0</i> | 调整结果的对比度。 |
| <b>浮雕</b> | 浮雕组同时控制正常输出和Height输出。 |
| <b>输出普通格式</b> <i>DirectX， OpenGL</i> | 在正常格式之间切换（翻转绿色）。 |
| <b>反转生成的浮雕</b> <i>False/True</i> | 反转Height的解释。 |
| <b>普通强度</b> <i>0.0 - 20.0</i> | 设置生成的正常映射的强度。 |
| <b>浮雕均衡器</b> <i>0.0 - 1.0</i> | 设置不同明细比率的折换余额。 |
| <b>挤压强度</b> <i>0.0 - 1.0</i> | 使正常过渡更锐利。 在转换为正常图像之前，可以先有效地添加锐化滤镜，使边缘更加明显。 |
| <b>正常锐化</b> <i>0.0 - 1.0</i> | 在转换后锐化正常映射，以显示细节。 |
| <b>正常柔化</b> <i>0.0 - 1.0</i> | 在转换后柔化正常映射，隐藏细节。 |
| <b>Specular</b> |  |
| <b>Diffuse影响</b> <i>0.0 - 1.0</i> | 设置扩散对Specular的影响。 还影响光泽度和粗糙度输出。 |
| <b>Specular饱和度</b> <i>0.0 - 1.0</i> | 更改Specular输出的饱和度。 |
| <b>Specular锐化</b> <i>0.0 - 1.0</i> | 锐化Specular输出。 |
| </b>中的<b>Specular level <i>0.0 - 1.0</i> | 设置用于Specular解释的输入级别。 |
| <b>Specular level输出</b> <i>0.0 - 1.0</i> | 修改Specular的输出级别。 |
| <b>金属的Specular影响</b> <i>0.0 - 1.0</i> | 确定可选金属输入对Specular映射的影响。 |
| <b>光泽度</b> |  |
| <b>在</b>中的光泽度级别 <i>0.0 - 1.0</i> | 设置用于光泽度解释的输入级别。 |
| <b>超出光泽度级别</b> <i>0.0 - 1.0</i> | 修改光泽度输出级别。 |
| <b>金属的光泽度影响</b> <i>0.0 - 1.0</i> | 确定可选金属输入对光泽度映射的影响。 |
| <b>粗糙度</b> |  |
| <b>在</b>中的粗糙度级别 <i>0.0 - 1.0</i> | 设置用于粗糙度解释的输入级别。 |
| <b>超出粗糙度级别</b> <i>0.0 - 1.0</i> | 修改粗糙度输出级别。 |
| <b>金属粗糙度影响</b> <i>0.0 - 1.0</i> | 确定可选金属输入对光泽度映射的影响。 |
| <b>Ambient occlusion</b> |  |
| <b>Diffuse中的Ambient occlusion</b> <i>0.0 - 1.0</i> | 将生成的AO中的混合转换为Diffuse输出。 |
| <b>Ambient occlusion跨页</b> <i>0.0 - 1.0</i> | 设置AO跨页的生成距离。 |
| <b>Ambient occlusion光距离</b> <i>0.0 - 1.0</i> | 设置AO“深度”解释。 当跨距较大时，影响较小。 |
| <b>Ambient occlusion的光角度</b> <i>0.0 - 1.0</i> | 设置假光照AO强制转换角度。 如果设置为相反的角度，可用于补偿Diffuse中已有的任何方向AO。 |
| <b>Ambient occlusion级别</b> <i>0.0 - 1.0</i> | 修改AO输出级别。 |
