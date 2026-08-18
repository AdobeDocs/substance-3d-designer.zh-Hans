---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: 了解如何在FXMaps中使用迭代变量和数字变量来创建循环模式和过程变化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 迭代和数字变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# 迭代和$number变量

![](../../../../assets/iterate-1.jpg)

“迭代”节点将按照“迭代”值所指定的时间量渲染连接到右侧的节点。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1次迭代：高斯图案渲染一次 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10次迭代：高斯图案将在同一位置渲染10次 |

使用“迭代”节点时，可以使用$number变量获取当前迭代值。 $number是浮点值，从0开始。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

在“图案偏移”参数中设置此函数，将执行10次，每个图案执行一次。

第一个图案具有等于0的$number值，然后在(0， 0)坐标下呈现。 第二个图案具有等于1的$number值，然后以(0.1， 0)坐标(1 x 0.1 = 0.1)呈现，依此类推，用于下一个图案。

下载示例： [迭代\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
