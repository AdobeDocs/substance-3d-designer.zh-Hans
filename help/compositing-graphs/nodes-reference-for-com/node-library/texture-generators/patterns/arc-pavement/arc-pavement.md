---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: 使用弧形路面节点生成弧形路面图案，用于创建弯曲的道路和路径纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弧形路面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# 弧形路面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成巴黎弧形路面图案。 无法使用标准[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)或[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)实现此效果，因此使用此专用节点。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>缩放</b> <i>1 - 8</i> | 设置全局缩放/拼贴。 |
| <b>图案数量</b> <i>1 - 32</i> | 设置每条弧线中使用的砖块量。 |
| <b>图案数量随机</b> <i>0.0 - 1.0</i> | 将每条弧线中的砖块量随机分布。 具有赋予砖块不同比例的附加效果。 |
| <b>图案最小数量</b> <i>1 - 10</i> | 在随机弧线时控制砖块的最小数量。 |
| <b>弧线数量</b> <i>0 - 20</i> | 设置垂直栈叠的弧线数量。 更改Height。 |
| <b>图案</b> <i>输入图像，方形，磁盘，抛物面，铃声，高斯，荆棘，金字塔，砖块，层次，波浪，半圆，脊状的圆，新月，胶囊体，锥形</i> | 选择要使用的图案形状。 |
| <b>输入图像的筛选</b> <i>双线性+ Mipmaps，双线性，最接近</i> |  |
| <b>图案缩放</b> <i>0.0 - 1.0</i> | 设置每个拼贴的缩放比例。 |
| <b>图案宽度</b> <i>0.0 - 1.0</i> | 设置每个拼贴的宽度。 |
| <b>图案Height</b> <i>0.0 - 1.0</i> | 设置每个磁贴的Height。 |
| <b>图案宽度随机</b> <i>0.0 - 1.0</i> | 随机分配拼贴宽度。 |
| <b>图案Height随机</b> <i>0.0 - 1.0</i> | 随机分布拼贴Height。 |
| <b>全局模式宽度随机</b> <i>0.0 - 1.0</i> | 随机分布拼贴宽度，而不在拼贴之间创建更大的间隙。 |
| <b>图案Height减少</b> <i>0.0 - 1.0</i> | 控制每个弧线末端的拼贴Height的挤压。 |
| <b>颜色随机</b> <i>0.0 - 1.0</i> | 随机分配拼贴颜色。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用以非方形比例补偿挤压和拉伸。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/arcpavement-ex.png" />
        </td>
    </tr>
</table>
