---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: 使用“非正方形变换”节点，可以将变换应用于具有独立X和Y缩放的非正方形纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非方形变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# 非方形变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

[变换2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的非方形安全版本。 自动检测非方形比例，并可以将正方形变换到非方形画布上。

确保您完全理解[图形参数](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)以充分利用此节点，因为您需要正确设置一些设置：

* 您的&#x200B;**图形**&#x200B;大小应为非方形，否则不需要此节点。
* 将非正方形变换&#x200B;**节点的**&#x200B;输出大小设置为“*相对于父代*”。
* 如果只想将输入变换到单个位置，请将&#x200B;**节点的**&#x200B;拼贴模式设置为“*无拼贴*”。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>平铺模式</b> <i>自动，手动</i> | 是否启用自动非方形补偿。 |
| <b>平铺</b> <i>1 - 16</i> | 只有在“平铺模式”设置为“手动”时才能访问。 允许您以拼贴安全的方式更改比例。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移动或转换结果。 双击滑块以输入负值。 |
| <b>旋转</b> <i>0.0 - 1.0</i> | 旋转输入图像。 |
| <b>安全旋转（仅限正方形）</b> <i>False/True</i> | 捕捉到安全值以保持像素的锐度。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 用于填充图像的背景色。 仅当Base Parameters中的[拼贴模式设置为“*无拼贴*”](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)时可见。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonsquare-ex.png" />
        </td>
    </tr>
</table>
