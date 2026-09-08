---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# 基色/金属/粗糙度转换器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

## 基色/金属/粗糙度转换器

**在：** *材质滤镜/PBR实用工具*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点将“基色”、“金属”和“粗糙度”映射转换为不同的PBR模型输出，例如“Specular/光泽度”模型。 其中包括一些著名的渲染引擎，例如Vray、Corona、Redshift、Renderman和Arnold。

如果具有用一个PBR模型制作的图形或材质，而目标需要不同的模型，则此功能非常有用。

## 参数

* **使用SpecularLevel输入**： *False/True*&#x200B;将额外的输入槽公开为SpecularLevel输入。 在转换过程中也会考虑这一点。
* ***Target**： *PBRDiffuse/Specular/Gloss、Vray (GGX)、Corona、Corona 1.6+、Redshift 1.x、Arnold 4 (AiStandard)、Arnold 4 (AlSurface)、RenderMan (PxrSurface)**设置转换目标模型。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
