---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
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
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Uber浮雕

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

[浮雕](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)的高级、功能丰富版本。 基于Heightmap执行复杂的2D伪光照效果。

在需要大量控制的情况下，为某些纹理样式创建烘焙光照时非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>颜色</b> <i>颜色输入</i> | 要修改的基本图像。 |
| <b>Height</b> <i>灰度输入</i> | 将Heightmap用作效果的驱动程序。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>环境色</b> <i>（颜色值）</i> | 阴影区域中使用的颜色。 |
| <b>Diffuse颜色</b> <i>（颜色值）</i> | 在亮区中使用的颜色。 |
| <b>Specular颜色</b> <i>（颜色值）</i> | 用于Specular反射的颜色 |
| <b>光照强度</b> <i>0.0 - 1.0</i> | （虚假）光线的强度。 |
| <b>光线角度</b> <i>0.0 - 1.0</i> | （虚假）光的入射角 |
| <b>Specular强度</b> <i>0.0 - 1.0</i> | Specular反射的强度。 |
| <b>光泽度</b> <i>0.0 - 1.0</i> | Specular高光的大小。 |
| <b>粗糙度</b> <i>0.0 - 1.0</i> | 用于计算漫射光照的粗糙度。 |
| <b>阴影不透明度</b> <i>0.0 - 1.0</i> | 混合阴影区域的不透明度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/uberemboss-ex.png" />
        </td>
    </tr>
</table>
