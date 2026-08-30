---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: 使用3D纹理表面渲染节点从3D数据渲染表面纹理，以创建程序化的表面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D纹理表面渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# 3D纹理表面渲染

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>进入：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

**3D纹理表面渲染**&#x200B;节点使用来自&#x200B;**3D距离场**&#x200B;图像输入的相应&#x200B;*距离场*&#x200B;渲染由&#x200B;*3D纹理*&#x200B;描述的形状的表面。

曲面在&#x200B;*单位立方体*&#x200B;的范围内表示。 使用映射到无限球的&#x200B;**环境**&#x200B;输入图像计算光照。

>[!NOTE]
>
> 距离场应为&#x200B;**4096x4096**&#x200B;纹理，用于描述&#x200B;**16x16**&#x200B;网格（256个切片）的形状。\
> 您可以使用[3D纹理SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)节点来计算256个切片的3D纹理的距离场。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>3D距离字段</b> <i>灰度</i> | 4096x4096图像表示形状的<i>距离场</i>的256个<i>切片</i>，排列在16x16网格中。<br>您可以使用[3D纹理SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)节点来计算256个切片的3D纹理的距离字段。 |
| <b>环境</b> <i>颜色</i> | 表示<i>环境</i>的图像，该图像应映射到渲染中的无限球体，并用于计算<i>光照</i>。<br>当<b>背景模式</b>参数设置为<i>环境</i>或<i>环境</i>时，该图像还用于渲染场景背景。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输出分辨率</b> <i>整数2</i> | <b>X</b>和<b>Y</b>中输出图像的分辨率，表示为<i>的二次方</i>。 |
| <b>相机位置</b> <i>浮点2</i> | 形状周围相机的位置。<br>选择节点后，可以使用<b>2D 视图</b>中的位置Gizmo来<i>轨道</i>相机。 |
| <b>相机距离</b> <i>浮动</i> | 从相机到形状的距离。 |
| <b>相机FOV</b> <i>浮动</i> | 相机的视角<i>度</i>。 |
| <b>反照率</b> <i>浮点3</i> | 形状表面的反照率。 |
| <b>背景模式</b> <i>整数</i> | 表示渲染场景背景的方法： <br>- <i>地面辐照度</i>：计算的地面平面辐照度<br>- <i>环境</i>：映射到无限球的<b>环境</b>图像输入的环境色，类似于图像的高度模糊版本<br>- <i>统一颜色</i>：使用指定的颜色<br>- <i>环境</i>：映射到无限球的<b>环境</b>图像输入 |
| <b>背景颜色</b> <i>浮点4</i> | 用于统一填充渲染场景背景的颜色。<br><i>注意</i>：此参数仅在<b>背景模式</b>参数设置为<i>统一颜色</i>时可用。 |
| <b>启用地面平面</b> <i>布尔值</i> | 当<i>True</i>时，渲染地平面。 包围形状的<i>单位立方体</i>位于此平面上。 |
| <b>无限平面</b> <i>布尔值</i> | 将地面平面设置为<i>无限扩展</i>到水平线。<br><i>注意</i>：仅当<b>启用地面平面</b>参数设置为<i>True</i>时，此参数才可用。 |
| <b>地面的平面大小</b> <i>浮点2</i> | 调整地面平面的大小。<br><i>注意</i>：仅当<b>启用地面平面</b>参数设置为<i>True</i>且<b>无限平面</b>参数设置为<i>False</i>时，此参数才可用。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>
