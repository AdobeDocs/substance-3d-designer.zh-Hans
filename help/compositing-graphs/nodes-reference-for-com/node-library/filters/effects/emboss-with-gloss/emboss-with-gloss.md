---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: 使用“光泽浮雕”节点创建带有光泽映射的浮雕效果，为纹理添加深度和光泽。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光泽浮雕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# 光泽浮雕

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/emboss-with-gloss.png){width="128px"}

## 光泽浮雕

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

在颜色和Height输入上执行添加光泽（Specular反射）的浮雕效果。 实质上根据Height信息为图像添加仿制的烘焙光照。 对于某些需要烘焙到纹理中的光照的纹理样式很有用。

有关包含更多选项的版本，请参阅[Uber浮雕](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)。 还有更简单的原子版本的[浮雕](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)。

## 参数

### 输入

* **颜色**： *颜色输入*
* **Height**： *灰度输入*

### 参数

* **高光颜色**： *（颜色值）*Specular高光的颜色。
* **阴影颜色**： *（颜色值）*在阴影/不亮区域中使用的颜色。
* **光泽**： *0.0 - 0.5*&#x200B;光泽度高光大小。
* **强度**： *0.0 - 10.0*&#x200B;高光强度。
* **光源角度**： *0.0 - 1.0*\
  （虚假）光的入射角。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
