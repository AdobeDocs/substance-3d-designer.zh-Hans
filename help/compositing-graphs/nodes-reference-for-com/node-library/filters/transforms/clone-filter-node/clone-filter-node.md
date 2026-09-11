---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: 使用滤镜节点复制和偏移纹理区域，以创建无缝图案和拼贴效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 克隆（筛选器节点）
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# 克隆（筛选器节点）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-4.png)

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

输入图像一次到指定位置。 可以用作原始“仿制图章”工具。

需要注意以下事项，才能获得预期效果：

* 理想情况下，输入图像将具有Alpha 通道（如贴花），因为混合只是一个直线拷贝。
* 蒙版默认为黑色，因此至少需要插入统一的白色灰度值才能看到任何结果。
* “位移”将在图像外部轻松剪切，因此请使用较小的值。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>源</b> <i>颜色输入</i> | 要仿制的图像。 重要提示：理想情况下，图像将具有Alpha 通道！ |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 默认为黑色！ |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>偏移</b> <i>-</i> | 移动或转换结果。 正片表示左和上，负片表示右和下。 使用较小的值1.0及更高版本会将其移动到图像之外！ |
| <b>模糊蒙版</b> <i>0.0 - 10.0</i> | 对蒙版应用模糊滤镜以柔化边缘。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-example.png" />
        </td>
    </tr>
</table>
