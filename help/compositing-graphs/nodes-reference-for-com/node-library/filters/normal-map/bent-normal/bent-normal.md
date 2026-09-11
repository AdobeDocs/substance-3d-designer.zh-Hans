---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: 使用“弯曲法线”节点生成考虑环境遮蔽和间接光照的弯曲法线图。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 弯曲法线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# 弯曲法线

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![弯曲正常节点图标](bent-normal.resources/rt-bent-normal.png "弯曲正常节点图标")

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据Height映射输入生成弯曲法线映射。 弯曲法线映射是[法线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)和[环境遮蔽(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)的特殊版本，生成带有嵌入环境遮蔽的法线映射。\
这可用于实时引擎，以将环境遮蔽烘焙到正常映射中，例如，用于更精确的金属遮蔽反射。

由于计算时间的原因，不应将此节点与CPU (SSE)引擎结合使用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>使用物理尺寸</b> <i>布尔值</i> | 切换以使用物理尺寸设置来确定Height比例。 |
| <b>物理尺寸</b> <i>浮点3</i> | （<b>使用物理尺寸</b>设置为<i>True</i>时可用）根据表面的实际物理尺寸调整Height比例。 |
| <b>示例</b> <i>整数</i> | 用于计算弯曲法线的光线数。<br>光线数越高，得到的结果越平滑，精度越高，但会降低性能。 |
| <b>Height比例</b> <i>浮动</i> | （使用物理尺寸设置为False时可用）高度图输入强度的乘数。 |
| <b>分发</b> <i>整数</i> | 设置分布方法。 影响向阴影区域的衰减。 |
| <b>最大距离</b> <i>浮动</i> | 设置光线可传播以被遮挡的最大距离。 |
| <b>扩散角度</b> <i>浮动</i> | 设置要拍摄的光线的扩散角度。 值1表示整个半球。 |
| <b>正常格式</b> <i>整数</i> | 反转输出的绿色通道。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bent-normal.resources/bent-normal-ex-1.jpg" />
        </td>
    </tr>
</table>
