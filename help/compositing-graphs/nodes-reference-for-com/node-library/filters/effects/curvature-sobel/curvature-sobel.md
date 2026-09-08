---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 使用Sobel运算符通过曲率Sobel节点检测曲率边缘，以创建基于边缘的蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弯曲Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# 弯曲Sobel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对输入[正常映射](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)执行简单、苛刻的单程曲率转换。 生成的贴图具有凸形区域的白色色调和凹形区域的黑色色调。 曲率将始终产生较粗的线条和尖锐的过渡。

此节点对于快速突出显示或调暗某些边缘非常有用。 它与[曲率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)略有不同，因为它可产生更好的质量结果，但仍然清晰且生硬。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>0.0 - 1.0</i> | 效果的强度，调整对比度。 |
| <b>正常类型</b> <i>DirectX， OpenGL</i> |  |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/curv-sobel-ex.png" />
        </td>
    </tr>
</table>
