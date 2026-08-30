---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: 使用“形状投影”节点向形状添加投影效果，以便在纹理中创建深度和维度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# 形状投影

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-drop-shadow.resources/shape-dropshadow-grayscale.png){width="128px"}

![](shape-drop-shadow.resources/shape-dropshadow.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在输入黑白图像（适用于灰度版本）或具有透明度的图像（适用于白色蒙版版本）上，执行来自其他2D图像处理软件的众所周知的“投影”效果。

它不同于[阴影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md)效果，因为它返回应用了完全透明度的图像，从而使效果更完整，类似于您在其他软件中期望的效果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>角度</b> <i>0.0 - 1.0</i> | （假）光的入射角。 |
| <b>距离</b> <i>-0.5 - 0.5</i> | 阴影下拉到形状的距离/与形状之间的距离。 |
| <b>大小</b> <i>0.0 - 1.0</i> | 控制阴影的模糊化/模糊化。 |
| <b>跨页</b> <i>0.0 - 1.0</i> | 模糊效果的切断/阈值使阴影进一步扩散。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 混合阴影效果的不透明度。 |
| <b>（阴影）颜色</b> <i>（颜色值）</i> | 应用于阴影的色调。 |
| <b>蒙版颜色</b> <i>（颜色值）（仅限灰度版本）</i> | 用于透明度映射输出的纯色。 |
| <b>输入已预乘</b> <i>False/True（仅限颜色版本）</i> | 是否应假设输入为预乘。 |
| <b>预乘输出</b> <i>False/True</i> | 是否应预乘输出。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-drop-shadow.resources/dropshadowex.png" />
        </td>
    </tr>
</table>
