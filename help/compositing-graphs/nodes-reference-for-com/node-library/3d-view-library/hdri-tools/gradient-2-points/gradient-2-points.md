---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-2-points.html"
breadcrumb-title: ''
description: 使用“渐变2点”节点，在HDRI环境中为天空和地色过渡创建两点渐变。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient 2 Points
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渐变2点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# 渐变2点

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-2-points.resources/gradient-2-points.png){width="250px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在两个用户选择的点之间创建2种颜色的渐变。 结果将根据球面投影进行调整。 类似于[渐变线性(HDRI)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/gradient-linear-hdri/gradient-linear-hdri.md)，但具有两个点而不是一个点。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>点1位置</b> | 用户选择的第一个点位置。 具有2D视图中的手柄。 |
| <b>点1颜色</b> <i>（颜色值）</i> | 渐变起始点颜色。 |
| <b>点1对比度</b> <i>0.0 - 1.0</i> | 第一个点蒙版的对比度。 |
| <b>点2位置</b> | 用户选定的第二个点位置。 具有2D视图中的手柄。 |
| <b>点2颜色</b> <i>（颜色值）</i> | 渐变末尾的颜色。 |
| <b>点2对比度</b> <i>0.0 - 1.0</i> | 第二个点蒙版的对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-2-points.resources/gradient-ex2.gif" />
        </td>
    </tr>
</table>
