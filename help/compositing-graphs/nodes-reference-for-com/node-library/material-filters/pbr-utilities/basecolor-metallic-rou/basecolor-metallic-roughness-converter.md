---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: 使用“BaseColor金属粗糙度转换器”节点可在不同的PBR材质格式和工作流程之间进行转换。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 基色金属粗糙度转换器
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# 基色/金属/粗糙度转换器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

<b>进入：</b>材质过滤器> PBR实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点将“基色”、“金属”和“粗糙度”映射转换为不同的PBR模型输出，例如“Specular/光泽度”模型。 其中包括一些著名的渲染引擎，例如Vray、Corona、Redshift、Renderman和Arnold。

如果具有用一个PBR模型制作的图形或材质，而目标需要不同的模型，则此功能非常有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>使用SpecularLevel输入</b> <i>False/True</i> | 将额外的输入槽公开为SpecularLevel输入。 在转换过程中也会考虑这一点。 |
| <b>目标</b> <i>PBRDiffuse/Specular/光泽、Vray (GGX)、Corona、Corona 1.6+、Redshift 1.x、Arnold 4 (AiStandard)、Arnold 4 (AlSurface)、RenderMan (PxrSurface)</i> | 设置转换目标模型。 |
