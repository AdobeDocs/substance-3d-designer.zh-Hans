---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: 使用“飞溅”节点跨散点形状，以创建随机图案和有机纹理细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 飞溅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# 飞溅

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter.resources/splatter.png)

![](splatter.resources/splatter-color.png)

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

Scplatter是一种图案生成器，用于随机放置地图输入。 它具有许多用于几何图案化放置的控制，并且比[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)使用起来更简单。 后者可以获得类似的结果，但复杂得多。

“飞溅”适用于快速压印某些形状，而无需过多调整。

请记住，默认的Splatter参数看起来完全不是随机的：您需要调整其中几个参数以获得随机性（主要是无序参数）。 另外请记住，“飞溅”需要地图输入才能生效。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>图案大小宽度</b> <i>0.0 - 1000.0</i> | 在X轴上使用的图案数。 |
| <b>图案大小Height</b> <i>0.0 - 1000.0</i> | 在Y轴上使用的图案数。 |
| <b>旋转</b> <i>-360.0 - 360.0</i> | 按设置的量旋转每个图案。 |
| <b>旋转变化</b> <i>0.0 - 360.0</i> | 为每个单独的形状引入随机旋转。 |
| <b>缩放</b> <i>100.0 - 10000.0</i> | 放大最终结果。 请记住，这会打破拼贴！ |
| <b>增益</b> <i>0.0 - 10.0</i> | 调整每种模式的混合增益。 使它们更加突出。 |
| <b>平移X</b> <i>-100.0 - 100.0</i> | 对X轴平移整个结果。 |
| <b>平移Y</b> <i>-100.0 - 100.0</i> | 在Y轴上平移整个结果。 |
| <b>无序</b> <i>0.0 - 100.0</i> | 随机移动形状。 |
| <b>网格编号</b> <i>0 - 8</i> | 跳转不同的网格大小以调整结果刻度。 保持拼贴。 |
| <b>无序角度</b> <i>0.0 - 360.0</i> | 控制无序移动的角度。 |
| <b>无序随机</b> <i>False/True</i> | 随机调整无序角度，从而增加更多的混乱。 |
| <b>图案大小</b> <i>5 - 12</i> |  |
| <b>大小变化</b> <i>0.0 - 100.0</i> | 为每个形状引入随机缩放。 |
| <b>图像输入筛选（仅限引擎> v4）</b> <i>双线性+ Mipmaps，双线性，最接近</i> | 要应用于输入图像的筛选。 |
| <b>输出级别最小值</b> <i>0.0 - 1.0</i> | 输出最小电平调整。 |
| <b>输出级别最大值</b> <i>0.0 - 1.0</i> | 输出最大电平调整。 |
| <b>背景颜色</b> <i>（灰度值）</i> | 设置纯背景色。 |
| <b>明亮度变化</b> <i>0.0 - 1.0（仅限灰度版本）</i> | 引入明亮度变化。 |
| <b>颜色变化</b> <i>0.0 - 1.0（仅限颜色版本）</i> | 引入颜色变化。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter.resources/splatter-ex.gif" />
        </td>
    </tr>
</table>
