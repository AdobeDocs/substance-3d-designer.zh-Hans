---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: 使用3D体积蒙版节点创建基于3D位置的体积蒙版以获得高级材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D体积蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 3D体积蒙版

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3dvolumemask.png){width="256px"}

<b>进入：</b>生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

**3D体积蒙版**&#x200B;节点基于&#x200B;**位置**&#x200B;输入图生成&#x200B;*基本形状*&#x200B;的表示形式。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>位置</b> <i>颜色</i> | 描述基元的&#x200B;*3D空间坐标*&#x200B;的映射表示为。<br><br>X/Y/Z **坐标分别映射到** R/G/B **通道。** |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>形状</b> <i>整数</i> | 应表示的基本形状： <br><br>- *立方体*<br>- *圆柱体*<br>- *球体* |
| <b>缩放</b> <i>浮动</i> | 定义基元的&#x200B;*全局*&#x200B;缩放，在所有轴上统一应用&#x200B;**。 |
| <b>大小</b> <i>浮点3</i> | 定义每个轴上的形状大小。 |
| <b>位置输入</b> <i>整数</i> | *通过&#x200B;**位置**&#x200B;输入表示空间*&#x200B;的方法： <br><br>- *UV位置*：使用&#x200B;*UV映射*。 X/Y(U/V)坐标分别映射到R/G通道。 Z轴被假定为&#x200B;*正交向前*&#x200B;矢量。<br>- *世界空间位置*：使用&#x200B;*位置映射*&#x200B;在3D空间中映射基元。 X/Y/Z坐标分别映射到R/G/B通道。 |
| <b>位置UV</b> <i>浮点2</i> | 基元在UV空间中的位置。<br><br>*注意*：仅当&#x200B;**位置输入**&#x200B;参数设置为&#x200B;*UV位置*&#x200B;时，此参数才可用。 |
| <b>位置</b> <i>浮点3</i> | 基元在世界空间中的位置。<br><br>*注意*：仅当&#x200B;**位置输入**&#x200B;参数设置为&#x200B;*世界空间位置*&#x200B;时，此参数才可用。 |
| <b>旋转</b> <i>浮点3</i> | 定义形状在世界空间中的旋转。 |
| <b>羽化宽度</b> <i>浮动</i> | 从基元表面向内调整&#x200B;*淡化渐变*&#x200B;的宽度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant4.jpg" />
        </td>
    </tr>
</table>
