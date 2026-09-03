---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: 使用Ambient occlusionHBAO滤镜节点可以使用基于水平线的算法生成ambient occlusion图，以实现逼真的着色。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境遮蔽(HBAO)（滤镜节点）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# 环境遮蔽(HBAO)（滤镜节点）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-01.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将Heightmap作为输入并从中生成Ambient occlusion映射。 它使用了基于水平的Ambient occlusion，一种最初用于屏幕空间实时AO生成的算法。 对于从程序化高度图创建程序化AO映射非常有用。

有关替代的、更高但较慢的AO版本，请参阅[Ambient occlusion(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>使用世界单位</b> <i>False/True</i> | 切换使用世界或场景单位。 启用允许更精确控制的额外参数。 |
| <b>深度</b> <i>0.0 - 1.0</i> | 仅在“世界单位”设置为False时使用。 控制全局缩放程度。 |
| <b>表面大小</b> <i>0.0 - 1000.0</i> | 仅在“世界单位”设置为True时使用。 控制全局缩放程度。 |
| <b>Height比例（厘米）</b> <i>0.0 - 1000.0</i> | 仅在“世界单位”设置为True时使用。 控制全局缩放程度。 |
| <b>半径</b> <i>0.0 - 1.0</i> | 控制AO的传播。 |
| <b>质量</b> <i>4个样本，8个样本，16个样本</i> | 通过确定用于计算的样本量来设置质量级别。 |
| <b>GPU优化</b> <i>False/True</i> | 启用内部GPU优化，加快处理速度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-03.png" />
        </td>
    </tr>
</table>
