---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: 使用光照节点可根据网格光照条件生成蒙版，以创建逼真的材质变化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# 光线

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## 光线

**英寸：** *基于网格的生成器**/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版与其他生成器稍有不同：它完全执行基于世界空间正常映射的假光照，返回黑白“光图”蒙版。

## 参数

* **水平角度**： *0.0 - 1.0*&#x200B;设置假光的水平角度。
* **垂直角度**： *0.0 - 1.0*&#x200B;设置假光的垂直角度。
* **高光光泽度**： *0.0 - 0.999*&#x200B;设置高光区域的衰减分布。
* **高光级别**： *0.0 - 1.0*&#x200B;设置高光区域的亮度级别。

## 示例图像

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
