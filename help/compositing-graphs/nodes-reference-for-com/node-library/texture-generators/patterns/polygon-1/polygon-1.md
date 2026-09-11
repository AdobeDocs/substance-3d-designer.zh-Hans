---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: 使用“多边形1”节点生成基本多边形图案，这些图案具有可自定义的几何纹理的边和属性。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多边形1
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# 多边形1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](polygon-1.resources/polygon-1-1.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成多边形形状，其中包含许多调整选项。 有关更简单的版本，请参阅[多边形2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>边</b> <i>3 - 32</i> | 设置多边形应具有的边数。 |
| <b>爆炸</b> <i>0.0 - 1.0</i> | 将多边形“切片”分开。 |
| <b>三角形大小</b> <i>0.0 - 1.0</i> | 调整切片/三角形的大小。 任何调整都可能使形状分离，只有1,1。 完全连接！ |
| <b>缩放</b> <i>0.0 - 1.0</i> | 将整个形状作为一个整体进行缩放。 |
| <b>自动缩放</b> <i>False/True</i> | 调整比例，使用默认参数使整个多边形适应视图。 |
| <b>旋转</b> <i>0.0 - 1.0</i> | 旋转整个形状。 |
| <b>渐变</b> <i>False/True</i> | 生成渐变切片/三角形，而不是实心切片/三角形。 注意：启用此设置后，将变得与多边形2类似。 |
| <b>渐变反转</b> <i>False/True</i> | 如果启用“渐变”，则反向渐变方向。 |
| <b>拼贴</b> <i>1 - 16</i> | 设置结果应平铺的次数。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用以非方形比例补偿挤压和拉伸。 |
| <b>非方形拼贴</b> <i>False/True</i> | 启用非正方形扩展功能后，这将拼贴形状而不压缩。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="polygon-1.resources/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
