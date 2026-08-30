---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 使用弯曲Sobel节点通过Sobel运算符检测弯曲边缘，以创建基于边缘的蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel弯曲
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Sobel弯曲

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-sobel.resources/curvature-sobel.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对输入[标准映射](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)执行简单而苛刻的单程弯曲转换。 生成的贴图具有凸形区域的白色色调和凹形区域的黑色色调。 弯曲将始终产生较粗的线条和尖锐的过渡。

此节点对于快速突出显示或调暗某些边缘非常有用。 它与[弯曲](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)略有不同，因为它可以产生更好的质量结果，但仍然清晰且严苛。

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
            <img src="curvature-sobel.resources/curv-sobel-ex.png" />
        </td>
    </tr>
</table>
