---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: 使用“形状光”节点将自定形状的光源添加到HDRI环境，以实现创意光照效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状光照
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# 形状光照

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-light.resources/panorama-shape.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成球面投影的矩形形状。 形状变换由变换小工具驱动。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>背景图像输入</b> <i>颜色输入</i> | 合成所生成光的可选背景。 |
| <b>形状图像输入</b> <i>颜色输入</i> | 要映射到球面光的可选图像。 仅在“形状颜色模式”设置为“图像输入”时使用。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>形状矩阵</b> |  |
| <b>矩阵</b> <i>（转换矩阵）</i> | 结果的变换控件。 可以通过直接与画布交互来修改结果。 |
| <b>偏移</b> <i>-2.0 - 2.0</i> | 移动或平移结果。 可以通过直接与画布交互来修改结果。 |
| <b>形状</b> <i>矩形，磁盘</i> | 选择要置入的形状。 |
| <b>形状颜色模式</b> <i>RGB、温度（开氏温度）、图像输入</i> | 选择用来设置形状颜色的方法。 “Image Input（图像输入）”允许使用第二个输入插槽。 |
| <b>颜色</b> <i>（颜色值）</i> | 仅当“形状颜色模式”设置为“RGB”时。 为形状选取颜色。 |
| <b>形状温度</b> <i>800.0 - 20000.0</i> | 仅在“形状颜色模式”设置为“色温”时。 设置形状颜色的开氏值。 |
| <b>形状图像输入灰度系数</b> <i>sRGB，线性</i> | 仅当“形状颜色模式”设置为“图像输入”时。 确定如何解释形状图像输入。 |
| <b>形状曝光(EV)</b> <i>0.0 - 10.0</i> | 为生成的形状设置曝光值，使其与背景图像曝光值完美匹配。 |
| <b>形状硬度</b> <i>0.0 - 1.0</i> | 设置形状边缘的硬度。 |
| <b>热点曝光(EV)</b> <i>0.0 - 10.0</i> | 设置中心热点的曝光度。 请注意，这在RGB模式下不是很可见。 |
| <b>热点大小</b> <i>0.0 - 1.0</i> | 中心热点的大小。 |
| <b>热点衰减</b> <i>0.0 - 1.0</i> | 中心热点的衰减。 |
| <b>热点位置</b> <i>0.0 - 1.0</i> | 中心热点的X和Y位置。 |
| <b>启用后台输入</b> <i>False/True</i> | 切换可选背景图像的使用。 复合图像在背景之上生成了光照。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 如果未使用背景输入，请在此处设置纯色背景值。 |
| <b>背景灰度系数</b> <i>sRGB，线性</i> | 如果使用“背景输入”，请设置如何解释背景输入。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-light.resources/shape-light-ex.gif" />
        </td>
    </tr>
</table>
