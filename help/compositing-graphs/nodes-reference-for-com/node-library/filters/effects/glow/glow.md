---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: 使用“发光”节点为纹理添加发光效果，以创建发光和发光的材料外观。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 发光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# 发光

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](glow.resources/glow-greyscale.png){width="128px"}

![](glow.resources/glow-3.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

执行“外发光”类型的效果，如其他流行的图像编辑软件中所示。 实质上，在输入周围添加渐隐轮廓。

请记住，此功能不适用于具有Alpha通道的图像，您或许可以预料到。 即使是彩色版本，也只期望使用二进制、黑白蒙版作为输入；它只允许使用彩色发光。 如果您使用的版本处理的是具有透明度的图像，请参阅[形状发光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“发光”，对灰度输入使用“发光灰度”。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>发光量</b> <i>0.0 - 1.0</i> | 发光效果的全局不透明度。 |
| <b>清除金额</b> <i>0.0 - 1.0</i> | 暂时锁定以确认何时可关闭发光效果。 适用于半透明区域。 |
| <b>发光大小</b> <i>0.0 - 20.0</i> | 控制发光效果到达的距离。 |
| <b>发光颜色</b> <i>（颜色值）（仅限颜色版本）</i> | 设置发光效果的颜色。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="glow.resources/glow-ex.png" />
        </td>
    </tr>
</table>
