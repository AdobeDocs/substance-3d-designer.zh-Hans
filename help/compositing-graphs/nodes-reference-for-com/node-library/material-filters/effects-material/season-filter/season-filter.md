---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: 使用“季节过滤器”节点将季节性效果应用于创建春季、夏季、秋季和冬季变体的素材。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 季节过滤器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# 季节过滤器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## 季节过滤器

**范围：** *材质过滤器/效果*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点添加效果，如动画水位、雪、冰和/或苔藓。

请记住，这是旧版滤镜，并不旨在完全符合PBR要求。 保留它主要是出于旧版/兼容性原因，尽管它在某些情况下仍然很有用。 在[Snow封面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)和[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)中可以找到更新的PBR校正版本。

节点需要一组适当的材料输入，主要使用非常详细的Heightmap或Normalmap。

## 参数

### 输入

* **蒙版** ：*灰度输入*\
  用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。

### 参数

* **频道**
  * 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **高级**
  * **普通格式**： *DirectX，OpenGL*\
    在不同正常映射格式之间切换（反转绿色通道）。
  * **蒙版**： *False/True*\
    启用或禁用蒙版图。
  * **光照强度**： *0.0 - 1.0*\
    （虚假）光线的强度。
  * **光源角度**： *0.0 - 1.0*\
    （虚假）光的入射角
* **效果**
  * **来自Height或普通的效果**： *Height，普通*&#x200B;选择驱动效果的输入图。
  * **水位**： *0.0 - 1.0*&#x200B;根据Height/正常信息升高或降低水位。
  * **水细节**： *0.0 - 1.0*&#x200B;设置水中的细节量。
  * **折射**： *0.0 - 1.0*&#x200B;设置效果中的假折射量。
  * **反射**： *0.0 - 1.0*&#x200B;设置效果中的虚假反射量。
  * **反射距离**： *0.0 - 1.0*&#x200B;控制反射视觉效果。
  * **反射角度**： *0.0 - 1.0*&#x200B;控制反射视觉效果。
  * **流动方向**： *0.0 - 1.0*&#x200B;控制动画流动（使用Substance Player进行可视化）。
  * **冰**： *0.0 - 1.0*&#x200B;设置水的冻结程度。
  * **冰细节**： *0.0 - 1.0*&#x200B;设置冰的细节量。
  * **Snow**： *0.0 - 1.0*&#x200B;设置雪覆盖量。
  * **苔藓**： *0.0 - 1.0*&#x200B;设置苔藓覆盖的量。
  * **苔藓规模**： *1 - 4*&#x200B;设置所生成苔藓的纹理规模。
  * **苔藓颜色**： *（颜色值）*设置苔藓的颜色。
  * **水彩**： *（颜色值）*设置水彩，包括Alpha/不透明度。
* **混合**
  * **扩散强度**： *0.0 - 1.0*\
    扩散的混合强度。
  * **基色强度**： *0.0 - 1.0*\
    混合基色的强度。
  * **正常强度**： *0.0 - 1.0*\
    混合“正常”的强度。
  * **Specular强度**： *0.0 - 1.0*\
    混合Specular的强度。
  * **光泽度强度**： *0.0 - 1.0*\
    混合光泽度的强度。
  * **粗糙度强度**： *0.0 - 1.0*\
    混合粗糙度的强度。
  * **环境遮蔽强度**： *0.0 - 1.0*\
    混合环境遮蔽的强度。
  * **Height强度**： *0.0 - 1.0*\
    混合Height的强度。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
