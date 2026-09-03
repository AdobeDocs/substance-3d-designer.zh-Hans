---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: 使用“矢量变形”节点通过矢量场对纹理进行变形，以创建流畅和有机扭曲效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 矢量变形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# 矢量变形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-warp.resources/vector-warp-01.png){width="128px"}

![](vector-warp.resources/vector-warp-02.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

矢量变形是一种高级扭曲效果，类似于[变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)和[定向翘曲](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)，主要区别在于它是由（彩色）矢量位图而不是灰度映射驱动的。 这意味着它比原子节点的同类产品功能更强大、用途更广泛。

矢量映射类似于范数映射，但是它不需要归一化，只使用R通道和Green通道（X通道和Y通道）。 如果需要，可将蓝色和Alpha 通道保留为黑色。 构建好的矢量图可能是使用此节点时最大的挑战；您可以[将灰度图转换为Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)，也可以通过结合通道与[RGBA合并](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)来构建该图。 或者，也可以使用[“流图”](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting)之类的项。

当您要执行具有各种方向的非常特定的扭曲时，此节点非常有用，因为标准的变形节点不会剪切它。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色输入</i> | 映射以扭曲。 |
| <b>矢量图</b> <i>颜色输入</i> | 驱动程序映射扭曲。 颜色通道使用红色和蓝色。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>0.0 - 1.0</i> | 矢量图的强度乘数。 |
| <b>矢量格式</b> <i>DirectX， OpenGL</i> | 在向上和向下解释之间交换绿色通道。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="vector-warp.resources/vector-warp-03.png" />
        </td>
    </tr>
</table>
