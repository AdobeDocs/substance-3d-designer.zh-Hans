---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: 使用3D纹理表面渲染节点从3D数据渲染表面纹理，用于创建程序化的表面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D纹理表面渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# 3D纹理表面渲染

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**范围：** *滤镜/效果*

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**3D纹理表面渲染**&#x200B;节点使用来自&#x200B;**3D距离字段**&#x200B;图像输入的相应&#x200B;*距离字段*&#x200B;渲染由&#x200B;*3D纹理*&#x200B;描述的形状的表面。

曲面在&#x200B;*单位立方体*&#x200B;的范围内表示。 使用映射到无限球的&#x200B;**环境**&#x200B;输入图像计算光照。

>[!NOTE]
>
> 距离字段应为&#x200B;**4096x4096**&#x200B;纹理，用于使用256个切片的&#x200B;**16x16**&#x200B;网格描述形状。\
> 您可以使用[3D纹理SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)节点为包含256个切片的3D纹理计算距离字段。

</td>
</tr>
</table>

## 参数

### 输入

* **3D距离场** *灰度*\
  4096x4096图像表示形状的&#x200B;*距离场*&#x200B;的256个&#x200B;*切片*，以16x16网格排列。\
  您可以使用[3D纹理SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)节点为包含256个切片的3D纹理计算距离字段。
* **环境** *颜色*\
  表示&#x200B;*环境*&#x200B;的图像，该图像应映射到渲染中的无限球体，并用于计算&#x200B;*光照*。\
  当&#x200B;**“背景模式”**&#x200B;参数设置为&#x200B;*“环境”*&#x200B;或&#x200B;*“环境”*&#x200B;时，也可使用该图像渲染场景背景。

### 参数

* **输出分辨率** *整数2*\
  **X**&#x200B;和&#x200B;**Y**&#x200B;中输出图像的分辨率，表示为&#x200B;*的二次方*。
* **相机位置** *Float2*\
  形状周围的相机位置。\
  选择节点后，可以使用&#x200B;**2D 视图**&#x200B;中的位置Gizmo来&#x200B;*轨道*&#x200B;相机。
* **相机距离** *Float*\
  相机到形状的距离。
* **相机FOV** *Float*\
  相机&#x200B;*度*&#x200B;的视角。
* **反照率** *Float3*\
  形状表面的反照率。
* **背景模式** *整数*\
  呈现场景的背景表示方法：
  * *地面辐照度*：计算地面平面的辐照度
  * *环境色*： **环境**&#x200B;图像输入的环境色映射到无限球体，类似于图像的强模糊版本
  * *统一颜色*：用指定颜色统一填充背景
  * *环境*： **环境**&#x200B;图像输入映射到无限球
* **背景颜色** *Float4*\
  用于均匀填充渲染场景背景的颜色。\
  *注意*：仅当&#x200B;**背景模式**&#x200B;参数设置为&#x200B;*统一颜色*&#x200B;时，此参数才可用。
* **启用地面平面** *布尔值*\
  当&#x200B;*True*&#x200B;时，渲染地面平面。 包围形状的&#x200B;*单位立方体*&#x200B;位于此平面上。
* **无限平面** *布尔值*\
  将地面平面设置为&#x200B;*无限延伸*&#x200B;到地平线。\
  *注意*：仅当&#x200B;**启用地面平面**&#x200B;参数设置为&#x200B;*True*&#x200B;时，此参数才可用。
* **地面平面大小** *Float2*&#x200B;调整地面平面的大小。\
  *注意*：仅当&#x200B;**启用地面平面**&#x200B;参数设置为&#x200B;*True*&#x200B;且&#x200B;**无限平面**&#x200B;参数设置为&#x200B;*False*&#x200B;时，此参数才可用。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
