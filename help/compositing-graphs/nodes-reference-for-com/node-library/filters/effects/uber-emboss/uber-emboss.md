---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: 使用Uber浮雕节点通过可自定义的深度、角度和光照控制创建高级浮雕效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber浮雕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# Uber浮雕

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## Uber浮雕

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

[浮雕](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)的高级、功能丰富版本。 基于Heightmap执行复杂的2D伪光照效果。

在需要大量控制的情况下，为某些纹理样式创建烘焙光照时非常有用。

## 参数

### 输入

* **颜色**： *颜色输入*\
  要修改的基本图像。
* **Height**： *灰度输入*\
  将Heightmap用作效果的驱动程序。

### 参数

* **环境色**： *（颜色值）*阴影区域中使用的颜色。
* **Diffuse颜色**： *（颜色值）*光照区域中使用的颜色。
* **Specular颜色**： *（颜色值）*用于Specular反射的颜色
* **光照强度**： *0.0 - 1.0*\
  （虚假）光线的强度。
* **光源角度**： *0.0 - 1.0*\
  （虚假）光的入射角
* **Specular强度**： *0.0 - 1.0* Specular反射强度。
* **光泽度**： *0.0 - 1.0* Specular高光的大小。
* **粗糙度**： *0.0 - 1.0*&#x200B;用于计算漫射光照的粗糙度。
* **阴影不透明度**： *0.0 - 1.0*&#x200B;混合阴影区域的不透明度。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
