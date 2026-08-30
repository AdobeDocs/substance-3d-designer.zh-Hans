---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/plasma.html"
breadcrumb-title: ''
description: 使用“等离子体”节点生成类似等离子体的噪声图案，用于创建有机和流体纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Plasma
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 等离子体
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 7%

---


# 等离子体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](plasma.resources/plasma.png){width="128px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这将生成稍有不同的[高斯杂色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)变体，其中较长的暗条纹作为凹谷。 它具有类似的比例距离控件，可以保持拼贴。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>缩放</b> <i>1 - 128</i> | 设置效果的全局比例。 |
| <b>无序</b> <i>0.0 - 1.0</i> | 对噪声进行相移以引入较小的变化。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用以非方形比例补偿挤压和拉伸。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="plasma.resources/plasma-ex.gif" />
        </td>
    </tr>
</table>
