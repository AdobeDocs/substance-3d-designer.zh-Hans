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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
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

在[Adobe Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)中创建多通道材料的最快捷、最简单的方法。 此节点根据简单的纯色设置和值返回捆绑的完整材料。 然后，这可以用作占位符或优化为复杂材料。

在对全部道具添加纹理以及混合多个材料时，此节点非常有用。 事实上，您可以从此节点启动每个材料，而无需复杂的材料库。

## 参数

### 输入

* 可使用“用户定义的输入”中的开关切换的每个通道的可选输入。

### 参数

* **PBR工作流**： *Metal -粗糙度，Specular-光泽度*&#x200B;设置使用的PBR模型。
* **材质预设**：*自定义、电介质、金、银、铝、铁、铜、钛、镍、钴、铂*&#x200B;快速快捷键以生成某些金属。 禁用不相关的选项。
* **Base color**： *（颜色值）*用于Base color的纯色。
* **金属**： *（灰度值）*用于金属的实心值。
* **Diffuse**： *（颜色值）*用于Diffuse的纯色。
* **Specular**： *（颜色值）*纯色用于Specular。
* **Specular预设**：*塑料、木材、石材、砖块、沙子、混凝土、织物、生锈金属、水、冰、玻璃*&#x200B;用于设置PBR正确Specular值的可选快速预设。
* **Specular范围**： *0.0 - 1.0*&#x200B;调整Specular范围。
* **粗糙度-光泽度**
  * **粗糙度值**： *（灰度值）*设置全局基本粗糙度值（如果通道处于活动状态）。
  * **光泽度值**： *（灰度值）*如果通道处于活动状态，则使用纯色进行光泽度。
  * **污渍量**： *0.0 - 1.0*&#x200B;可选污渍映射输入混合到光泽或粗糙度的程度。
  * **拼贴**： *1 - 16*&#x200B;范围以按平铺可选污渍映射。
  * **自定义污渍输入**： *False/True*&#x200B;启用或禁用可选的自定义污渍映射。
* **正常**
  * 从Height强度&#x200B;**为**&#x200B;正常： *0.0 - 16.0*&#x200B;可以选择将自定义Heightmap转换为正常，并以材料Normalmap的形式返回此值。
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
