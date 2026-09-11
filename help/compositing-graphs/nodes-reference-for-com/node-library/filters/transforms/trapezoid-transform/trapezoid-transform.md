---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: 使用“梯形变换”节点将梯形扭曲应用于纹理，以创建透视校正效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 梯形变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# 梯形变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapeze-transform.png){width="128px"}

![](trapezoid-transform.resources/trapeze-transform-grayscale.png){width="128px"}

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

以透视/梯形变形方式修改输入的特殊变换节点。 具有对顶部和底部拉伸的控制。 价值可以超越极限，产生更强烈的效果。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>顶拉伸</b> <i>0.0 - 1.0</i> | 在顶部设置拉伸或挤压量。 |
| <b>底部拉伸</b> <i>0.0 - 1.0</i> | 设置瓶子上的拉伸或挤压量。 |
| <b>背景颜色</b> <i>（灰度/颜色值）</i> | 设置纯背景色，以防拼贴关闭。 |
| <b>取样</b> <i>双线性，最接近</i> | 设置取样品质。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapeze-example.gif" />
        </td>
    </tr>
</table>
