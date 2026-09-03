---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: 使用“环境遮蔽”(RTAO)节点，从Height地图生成实时的环境遮蔽地图，以实现逼真的着色。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境遮蔽(RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# 环境遮蔽(RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RTAO节点图标](ambient-occlusion-rtao.resources/ambient-occlusion-rtao-01.png "RTAO节点图标")

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

基于遮蔽映射输入生成环境Height映射。

与HBAO相比，该滤波器计算结果更精确，但由于计算时间的原因，不能与CPU (SSE)引擎结合使用。

请参阅[环境遮蔽(HBAO)（滤镜节点）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md)以获取更快、更简单的替代方案。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>使用物理尺寸</b> <i>布尔值</i> | 切换以使用物理尺寸设置来确定Height比例。 |
| <b>物理尺寸</b> <i>浮点3</i> <i>（当<b>使用物理尺寸</b>设置为<i>True</i>时可用）</i> | 根据表面的真实物理尺寸调整Height比例 |
| <b>示例</b> <i>整数</i> | 用于计算ambient occlusion的光线数。<br>值越高，结果越平滑精确，但会降低性能。 |
| <b>Height比例</b> <i>浮动</i> <i>（当<b>使用物理尺寸</b>设置为<i>False</i>时可用）</i> | Height映射输入强度的乘数。 |
| <b>分发</b> <i>整数</i> | 设置分布方法。 影响阴影区域的衰减， |
| <b>最大距离</b> <i>浮动</i> | 设置光线可传播以被遮挡的最大距离。 |
| <b>扩散角度</b> <i>浮动</i> | 设置要拍摄的光线的扩散角度。 值1表示整个半球。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/ambient-occlusion-rtao-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/ambient-occlusion-rtao-03.png" />
        </td>
    </tr>
</table>
