---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: 使用马赛克节点通过将纹理分为像素化的块和图案来创建马赛克拼贴效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 马赛克
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# 马赛克

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/mosaic-1.png){width="128px"}

![](../../../../../../assets/mosaic-grayscale.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

通过执行多程[变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)效果来“刻画”现有、平滑、倾斜的渐变映射。 当对两个输入使用同一地图时，它实际上会增长并突出最亮的区域。

这对于为灰度图（如Heightmap）添加更多定义非常有用，因为它可以增加形状的定义。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>颜色</b> <i>彩色/灰度输入</i> |  |
| <b>马赛克地图</b> <i>灰度输入</i> | 变形驱动程序映射。 可以与第一个输入项相同。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>示例</b> <i>0 - 16</i> | 确定多样本品质。 |
| <b>强度</b> <i>0.0 - 1.0</i> | 效果的强度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/mosaci-ex.png" />
        </td>
    </tr>
</table>
