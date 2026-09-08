---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: 使用Ambient occlusionHBAO滤镜节点可以使用基于水平线的算法生成ambient occlusion图，以实现逼真的着色。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ambient occlusion(HBAO)(滤镜节点)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# ambient occlusion(HBAO)(滤镜节点)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## ambient occlusion(HBAO)

**范围：** *滤镜/效果*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

将Heightmap作为输入并从中生成Ambient occlusion映射。 它使用了基于水平的Ambient occlusion，一种最初用于屏幕空间实时AO生成的算法。 对于从程序化高度图创建程序化AO映射非常有用。

有关替代的、更高但较慢的AO版本，请参阅[Ambient occlusion(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## 参数

* **使用世界单位**： *False/True*&#x200B;切换使用世界或场景单位。 启用允许更精确控制的额外参数。
* **深度**： *0.0 - 1.0*&#x200B;仅在World Units设置为False时使用。 控制全局缩放程度。
* **表面大小**： **0.0 - 1000.0**&#x200B;仅在World Units设置为True时使用。 控制全局缩放程度。
* **Height比例(cm)**： *0.0 - 1000.0*&#x200B;仅在World Units设置为True时使用。 控制全局缩放程度。
* **半径**： *0.0 - 1.0*&#x200B;控制AO的传播。
* **质量**： *4个示例，8个示例，16个示例*\
  通过确定用于计算的样本量来设置质量级别。
* **GPU优化**： *False/True*&#x200B;启用内部GPU优化，加快处理速度。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
