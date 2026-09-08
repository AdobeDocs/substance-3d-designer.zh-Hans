---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: 使用3D纹理体积渲染节点从3D数据渲染体积纹理，以创建云雾效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D纹理体积渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# 3D纹理体积渲染

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**范围：** *滤镜/效果*

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**3D纹理体积渲染**&#x200B;节点使用其从&#x200B;**3D纹理**&#x200B;图像输入中相应的&#x200B;*带符号的距离字段*&#x200B;渲染&#x200B;*3D符号距离场*&#x200B;描述的形状的体积。

卷在&#x200B;*单位多维数据集*&#x200B;的范围内表示。 使用&#x200B;*定向光*&#x200B;和&#x200B;*半球天空光*&#x200B;计算光照。

>[!NOTE]
>
> 带符号的距离字段应为&#x200B;**4096x4096**&#x200B;纹理，用于描述具有256个切片的&#x200B;**16x16**&#x200B;网格的形状。\
> 您可以使用[3D纹理SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)节点为256个切片的3D纹理计算有符号距离字段。

</td>
</tr>
</table>

## 参数

### 输入

* **3D符号距离场** *灰度*\
  4096x4096图像表示形状的&#x200B;*符号距离场*&#x200B;的256个&#x200B;*切片*，以16x16网格排列。\
  您可以使用[3D纹理SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)节点为256个切片的3D纹理计算有符号距离字段。
* **密度** *灰度*\
  4096x4096图像表示形状的&#x200B;*密度*&#x200B;的256个&#x200B;*切片*，以16x16网格排列。 密度使用从0（完全透明）到1（完全不透明）的灰度值映射。\
  您可以使用[3D体积蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)或3D噪声节点（[3D Perlin噪声](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)、[3D Voronoi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md)、[3D脊状噪声分形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md)等）与[3D纹理位置](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md)节点结合作为位置输入，生成一个体积蒙版作为3D纹理，共256个切片。

### 参数

* **输出分辨率** *整数2*\
  **X**&#x200B;和&#x200B;**Y**&#x200B;中输出图像的分辨率，表示为&#x200B;*的二次方*。
* **相机位置** *Float2*\
  形状周围的相机位置。\
  选择节点后，可以使用&#x200B;**2D 视图**&#x200B;中的位置Gizmo来&#x200B;*轨道*&#x200B;相机。
* **光源位置** *Float2*\
  *定向光*&#x200B;在形状周围的位置。\
  选择节点后，可以使用&#x200B;**2D 视图**&#x200B;中的位置Gizmo来&#x200B;*绕轨*&#x200B;光源。
* **相机距离** *Float*\
  从相机到形状的距离。
* **相机FOV** *Float*\
  相机的视角&#x200B;*度*。
* **吸收** *Float*\
  调整光线通过&#x200B;*到*&#x200B;音量时吸收的光量。
* **羽化** *浮动*\
  将&#x200B;**密度**&#x200B;输入提供的值与&#x200B;*内部*&#x200B;距离字段值相乘。\
  这样可有效地将&#x200B;*渐隐渐变*&#x200B;的宽度从卷的外部限制向内调整。
* **浅色模式** *整数*\
  设置获取定向光颜色的方法：
  * *色温（开氏温度）*：颜色由光温决定，其中&#x200B;*较低*&#x200B;的值将导致&#x200B;*更暖*&#x200B;的颜色
  * *RGB颜色*：使用RGB值定义颜色
* **光温（开氏温度）***Float*\
  影响其&#x200B;*颜色*&#x200B;的定向光的温度。 *较低*&#x200B;的值会产生&#x200B;*暖色*&#x200B;色。\
  有用值：\
  1800 K — 蜡烛光\
  2800 K — 白炽灯\
  5500 K — 日光\
  6200 K — 自然白色\
  700K — 阴天\
  *注意*：仅当&#x200B;**浅色模式**&#x200B;参数设置为&#x200B;*温度（开氏度）*&#x200B;时，此参数才可用。
* **浅色** *Float3*\
  定向光的颜色。\
  *注意*：仅当&#x200B;**浅色模式**&#x200B;参数设置为&#x200B;*RGB颜色*&#x200B;时，此参数才可用。
* **光照强度** *Float*\
  定向光的强度。
* **环境色** *Float3*\
  环境天光的颜色。
* **环境强度** *Float*\
  环境天光的强度。
* **反照率** *Float3*\
  体积块的反照率。
* **背景模式** *整数*\
  基于&#x200B;**背景着色**&#x200B;的渲染场景背景颜色方法：
  * *阴影*：颜色受定向光的&#x200B;*颜色*&#x200B;和&#x200B;*强度*- *常量颜色*&#x200B;的影响：颜色统一应用&#x200B;*而不考虑定向光*
* **背景颜色** *Float4*\
  用于填充渲染场景的背景的颜色。
* **仿色** *Float*\
  调整用于平滑着色的&#x200B;*蓝色噪声仿色*&#x200B;的强度。
* **启用地面平面** *布尔值*\
  当&#x200B;*True*&#x200B;时，渲染&#x200B;*无限*&#x200B;地面平面。 包围形状的&#x200B;*单位立方体*&#x200B;位于此平面上。
* **无限平面** *布尔值*\
  将地面平面设置为&#x200B;*无限延伸*&#x200B;到地平线。\
  *注意*：仅当&#x200B;**启用地面平面**&#x200B;参数设置为&#x200B;*True*&#x200B;时，此参数才可用。
* **地面平面大小** *Float2*&#x200B;调整地面平面的大小。\
  *注意*：仅当&#x200B;**启用地面平面**&#x200B;参数设置为&#x200B;*True*&#x200B;且&#x200B;**无限平面**&#x200B;参数设置为&#x200B;*False*&#x200B;时，此参数才可用。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
