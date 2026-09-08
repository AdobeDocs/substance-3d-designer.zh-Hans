---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 使用3D纹理SDF节点从3D数据生成有符号距离场纹理，以创建平滑的形状和效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D纹理SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# 3D纹理SDF

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**范围：** *滤镜/效果*

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**3D纹理SDF**&#x200B;节点从&#x200B;**输入**&#x200B;的&#x200B;*3D纹理*&#x200B;蒙版生成形状的&#x200B;*有符号距离场*，该蒙版表示形状&#x200B;*体积*&#x200B;的切片。

</td>
</tr>
</table>

## 参数

### 输入

* **蒙版输入** *灰度*\
  表示形状&#x200B;*体积*&#x200B;切片的&#x200B;*3D纹理*&#x200B;蒙版。

### 参数

* **阈值** *浮动*\
  当形状体积由&#x200B;*渐隐渐变*&#x200B;描述时，设置渐变值，在该渐变值处，形状的&#x200B;*表面*&#x200B;被&#x200B;*检测到*。
* **输出** *整数*\
  应输出的距离字段的类型：
  * *距离字段*：输出描述形状&#x200B;*外部*&#x200B;距离的距离字段。
  * *符号距离场*：输出一个距离字段，描述形状的&#x200B;*外部*（正）和&#x200B;*内部*（负）的距离。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
