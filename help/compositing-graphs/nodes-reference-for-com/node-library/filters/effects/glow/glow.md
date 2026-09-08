---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: 使用“发光”节点为纹理添加发光效果，以创建发光和emissive的材料外观。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 发光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 发光

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## 发光

**范围：** *滤镜/效果*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

执行“外发光”类型的效果，如其他流行的图像编辑软件中所示。 实质上，在输入周围添加渐隐轮廓。

请记住，此功能并非旨在用于具有Alpha 通道的图像，您可能会预料到这一点。 即使是彩色版本，也只要求输入二进制、黑色和白色蒙版；它只允许使用彩色发光。 如果您使用的版本处理的是具有透明度的图像，请参阅[形状发光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“发光”，对灰度输入使用“发光灰度”。

## 参数

* **发光量**： *0.0 - 1.0*&#x200B;发光效果的全局不透明度。
* **清除量**： *0.0 - 1.0*&#x200B;何时关闭发光效果。 适用于半透明区域。
* **发光大小**： *0.0 - 20.0*&#x200B;控制发光效果到达的距离。
* **发光颜色**： *（颜色值）（仅限颜色版本）*设置发光效果的颜色。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
