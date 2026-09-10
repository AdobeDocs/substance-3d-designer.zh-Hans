---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/creased.html"
breadcrumb-title: ''
description: 使用“折痕”节点生成折痕图案，用于创建折叠织物和褶皱表面纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Creased
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 折痕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 93824555c1b2d3de289eaf470e6f929ebf90dd71
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 8%

---


# 折痕

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](creased.resources/creased.png){width="128px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点生成类似布的噪声。 可以将其解释为Heightmap

当需要具有大比例变化的半方向噪声时，“折痕”非常有用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>缩放</b> <i>1 - 8</i> | 设置效果的全局比例。 |
| <b>变形强度</b> <i>0.0 - 128.0</i> | 设置弯曲/变形效果的强度。 |
| <b>无序</b> <i>0.0 - 100.0</i> | 使用于生成噪声的图层略微偏移，以引入变化。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用压缩补偿并使用非正方形比例拉伸。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="creased.resources/creased-ex.gif" />
        </td>
    </tr>
</table>
