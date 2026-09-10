---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: 使用基础材质节点创建基础材质属性，以便从头开始构建基于物理的材料。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 基础材质
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# 基础材质

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](base-material.resources/pbr-base-material.png){width="128px"}

<b>进入：</b>材质过滤器> PBR实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在[Adobe Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中创建多通道材料的最快捷、最简单的方法。 此节点根据简单的纯色设置和值返回捆绑的完整材料。 然后，这可以用作占位符或优化为复杂材料。

在对全部道具添加纹理以及混合多个材料时，此节点非常有用。 事实上，您可以从此节点启动每个材料，而无需复杂的材料库。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
|  | 可使用“用户定义的输入”中的开关切换的每个通道的可选输入。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>PBR工作流</b> <i>金属 — 粗糙度，Specular-光泽度</i> | 设置使用的PBR模型。 |
| <b>材质预设</b> <i>自定义，电介质，金，银，铝，铁，铜，钛，镍，钴，铂</i> | 快速快捷键来创造某些金属。 禁用不相关的选项。 |
| <b>基色</b> <i>（颜色值）</i> | 用于Base color的纯色。 |
| <b>金属质感</b> <i>（灰度值）</i> | 用于金属的实值。 |
| <b>Diffuse颜色</b> <i>（颜色值）</i> | 用于Diffuse的纯色。 |
| <b>Specular</b> <i>（颜色值）</i> | 用于Specular的纯色。 |
| <b>Specular预设</b> <i>塑料，木材，石头，砖块，沙子，混凝土，织物，生锈的金属，水，冰，玻璃</i> | 用于设置正确的PBRSpecular值的可选快速预设。 |
| <b>Specular范围</b> <i>0.0 - 1.0</i> | 调整Specular范围。 |
| <b>粗糙度-光泽度</b> |  |
| <b>值</b>粗糙度 <i>（灰度值）</i> | 如果通道处于活动状态，请设置全局基本粗糙度值。 |
| <b>值</b>光泽度 <i>（灰度值）</i> | 如果通道处于活动状态，则使用纯色进行光泽度。 |
| <b>污渍量</b> <i>0.0 - 1.0</i> | 可选污渍映射输入混合到光泽或粗糙度的程度。 |
| <b>拼贴</b> <i>1 - 16</i> | 按平铺可选污渍映射的范围。 |
| <b>自定义污渍输入</b> <i>False/True</i> | 启用或禁用可选的自定义污渍映射。 |
| <b>正常</b> |  |
| <b>正常的Height强度</b> <i>0.0 - 16.0</i> | （可选）将自定义Heightmap转换为正常映射，并以材料Normalmap的形式返回此值。 |
| <b>Height</b> |  |
| <b>Height位置</b> <i>0.0 - 1.0</i> | 用于Height输出的实心值。 |
| <b>Height范围</b> <i>0.0 - 1.0</i> | 设置用户定义的高度映射的影响（如果已启用）。 |
| <b>用户定义的映射</b> | 打开或关闭所有用户定义的映射，返回这些映射而不是任何实值。 |
