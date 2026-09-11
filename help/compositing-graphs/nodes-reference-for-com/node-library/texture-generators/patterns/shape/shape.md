---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: 使用“形状”节点可生成用于在Substance 3D Designer中创建图案和纹理的基本几何形状。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# 形状

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成各种程序化形状，其中包含修改基础形状的选项。 形状始终具有完美插值和高精度。

尽管简单明了，但这是一个非常有用的节点：它是大多数程序化的高度图生成的构建块！ 通过将基本形状与变换节点相结合，可以创建比任何位图都更精确的完全程序化的高位图形状。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>拼贴</b> <i>1 - 16</i> | 设置结果应平铺的次数。 |
| <b>图案</b> <i>方形，磁盘，抛物面，铃声，高斯，荆棘，金字塔，砖块，层次，波浪，半圆，脊状的圆，新月，胶囊体，锥形，半球</i> | 选择要使用的图案形状。 |
| <b>特定图案</b> <i>0.0 - 1.0</i> | 可以更改选定图案的形状。 该效果取决于所选图案。 |
| <b>缩放</b> <i>0.0 - 1.0</i> | 缩放整个形状。 |
| <b>大小</b> <i>0.0 - 1.0</i> | 允许在X或Y轴上进行非均匀缩放。 |
| <b>角度</b> <i>0.0 - 1.0</i> | 旋转整个形状。 |
| <b>旋转45°</b> <i>False/True</i> | 以预设45度旋转。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用以非方形比例补偿挤压和拉伸。 |
| <b>非方形拼贴</b> <i>False/True</i> | 启用非正方形扩展功能后，这将拼贴形状而不压缩。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shape-ex.gif" />
        </td>
    </tr>
</table>
