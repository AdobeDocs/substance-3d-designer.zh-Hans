---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: 使用基础材质节点创建基础材质属性，以便从头开始构建基于物理的材质。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 基础材质
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# 基础材质

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## 基础材质

**在：** *材质滤镜/PBR实用工具*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在[Adobe Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中创建多通道素材的最快捷、最简单的方法。 此节点根据简单、纯色设置和值返回捆绑的“完整”材质。 然后，这可以用作占位符或细化为复杂素材。

为全部道具添加纹理和混合多种材质时，此节点非常有用。 事实上，您可以从这个节点开始使用每种材料，而无需复杂的材料基础。

## 参数

### 输入

* 可使用“用户定义的输入”中的开关切换的每个通道的可选输入。

### 参数

* **PBR工作流**： *金属 — 粗糙度，Specular — 光泽度*&#x200B;设置使用的PBR模型。
* **材质预设**：*自定义、电介质、金、银、铝、铁、铜、钛、镍、钴、铂*&#x200B;创建某些金属的快速快捷键。 禁用不相关的选项。
* **基色**： *（颜色值）*用于基色的纯色。
* **金属质感**： *（灰度值）*用于金属质感的实心值。
* **漫射颜色**： *（颜色值）*用于漫射的纯色。
* **Specular**： *（颜色值）*纯色用于Specular。
* **Specular预设**：*塑料、木材、石材、砖、沙子、混凝土、织物、生锈金属、水、冰、玻璃*&#x200B;用于设置PBR正确Specular值的可选快速预设。
* **Specular范围**： *0.0 - 1.0*&#x200B;调整Specular范围。
* **粗糙度 — 光泽度**
  * **粗糙度值**： *（灰度值）*设置全局基本粗糙度值（如果通道处于活动状态）。
  * **光泽度值**： *（灰度值）*用于光泽度的纯色（如果通道处于活动状态）。
  * **污渍量**： *0.0 - 1.0*&#x200B;可选污渍映射输入混合到光泽或粗糙度的范围。
  * **污渍拼贴**： *1 - 16*&#x200B;范围按拼贴可选污渍映射。
  * **自定义污渍输入**： *False/True*&#x200B;启用或禁用可选的自定义污渍映射。
* **正常**
  * 从Height强度&#x200B;**为**&#x200B;正常： *0.0 - 16.0*&#x200B;可以选择将自定义Heightmap转换为正常，并将此作为材质正常映射返回。
* **Height**
  * **Height位置**： *0.0 - 1.0*&#x200B;用于Height输出的实心值。
  * **Height范围**： *0.0 - 1.0*&#x200B;设置用户定义的海图的影响（如果已启用）。
* **用户定义的映射**
  * 打开或关闭所有用户定义的映射，返回这些映射而不是任何实值。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
