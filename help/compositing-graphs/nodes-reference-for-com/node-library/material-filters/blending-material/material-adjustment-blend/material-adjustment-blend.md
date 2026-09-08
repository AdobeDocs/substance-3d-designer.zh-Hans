---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# 素材调整混合

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## 素材调整混合

**范围：** *材质过滤器/混合*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点允许基于蒙版调整完整材料的任意和所有通道。 它旨在使完整的材料工作流程更轻松、更快速。

当您要基于同一蒙版调整材料的几个声道（例如，使扩散更亮、粗糙度更暗）时，此效果非常有用。

## 参数

### 输入

* **色彩 ID 蒙版**： *颜色输入*\
  用于遮盖节点效果的遮罩槽。
* **灰度蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **频道**\
  在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。\
  这还可以启用和禁用通道相关组的外观。
* **扩散**\
  在蒙版定义的区域中，对Diffuse通道执行调整操作。
* **基色**\
  在蒙版定义的区域中，对Base color通道执行调整操作。
* **正常**
  * **强度**： *0.0 - 1.0*&#x200B;按正常强度调低
* **Specular**\
  在蒙版定义的区域中，对Specular通道执行调整操作。
* **具发射性**\
  在蒙版定义的区域中，对发射通道执行调整操作。
* **光泽度**\
  在蒙版定义的区域中，对光泽度通道执行调整操作。
* **粗糙度**\
  在蒙版定义的区域中，对粗糙度通道执行调整操作。
* **金属**\
  在蒙版定义的区域中，对金属通道执行调整操作。
* **Specular level**\
  在蒙版定义的区域中，对Specular level通道执行调整操作。
* **Ambient occlusion**\
  在蒙版定义的区域中，对Ambient occlusion通道执行调整操作。
* **Height**\
  在蒙版定义的区域中，对Height通道执行调整操作。
* **不透明度**\
  在不透明度通道上，在蒙版定义的区域中执行调整操作。
* **色彩 ID 蒙版**： *False/True*&#x200B;设置为使用色彩 ID 蒙版而非灰度蒙版。
* **模糊**： *0.01 - 1.0*&#x200B;如果启用了“色彩 ID 蒙版”，这将确定“颜色ID”选区颜色的扩散。
* **颜色**： *（颜色值）*设置要从颜色Id 图和蒙版中选择的颜色。
* **填充**： *0.0 - 1.0*&#x200B;确定颜色ID蒙版的混合对比度/过渡。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
