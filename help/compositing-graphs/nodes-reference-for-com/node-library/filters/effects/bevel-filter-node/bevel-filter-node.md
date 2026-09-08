---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: 使用“斜面”滤镜节点在形状和图案上创建斜边以添加深度和维度。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜面(滤镜节点)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# 斜面(滤镜节点)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在输入灰度高图上执行边缘斜切效果。 基于该Heightmap返回斜面的Heightmap和Normalmap。

在理想二进制（高收缩黑白）的基本Heightmap上，这是应用精确曲线配置文件的一个有用的节点。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>灰度输入</i> | 要转换的高度映射。 |
| <b>自定义曲线</b> <i>灰度输入</i> | 确定确切曲线/斜率的渐变。 理想情况下为渐变线性节点，您可以在其中执行任何类型的调整，如[色阶](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)或[曲线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)。 仅当“使用自定义曲线”为True时处于活动状态。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>距离</b> <i>-1.0 - 1.0</i> | 斜角效果应达到的距离。 |
| <b>角类型</b> <i>圆，Angular</i> | 斜面轮廓是圆形还是直线。 |
| <b>平滑</b> <i>0.0 - 5.0</i> | 在斜角后还需要执行多少其他平滑（模糊）操作。 |
| <b>使用非均匀模糊</b> <i>False/True</i> | 是否应该以非一致的方式进行平滑。 |
| <b>使用自定义曲线</b> <i>False/True</i> | 切换使用您自己的自定义Height曲线。 有关更多信息，请参阅上文。 |
| <b>正常强度</b> <i>0.0 - 50.0</i> | 生成的正常映射的强度。 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/bevel-example.png" />
        </td>
    </tr>
</table>
