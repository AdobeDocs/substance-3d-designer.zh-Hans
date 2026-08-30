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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# 3D纹理SDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3dtexturesdf.png){width="200px"}

<b>进入：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

**3D纹理SDF**&#x200B;节点从&#x200B;**输入**&#x200B;的&#x200B;*3D纹理*&#x200B;蒙版生成形状的&#x200B;*有符号距离场*，该蒙版表示形状&#x200B;*体积*&#x200B;的切片。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版输入</b> <i>灰度</i> | 表示形状<i>体积</i>切片的<i>3D纹理</i>蒙版。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>阈值</b> <i>浮动</i> | 当形状体积由<i>渐隐渐变</i>描述时，设置渐变值，在该渐变值处，形状的<i>表面</i>被<i>检测到</i>。 |
| <b>输出</b> <i>整数</i> | 应输出的距离字段的类型： <br>- <i>距离字段</i>：输出描述形状<i>外部</i>距离的距离字段。<br>- <i>符号距离场</i>：输出描述形状的<i>外部</i>（正）和<i>内部</i>（负）距离的距离字段。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>
