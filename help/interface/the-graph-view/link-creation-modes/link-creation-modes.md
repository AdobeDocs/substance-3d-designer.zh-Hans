---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/link-creation-modes.html"
breadcrumb-title: ''
description: 了解图形视图中的链接创建模式，以便高效地连接节点。
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Link creation modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 链接创建模式
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---


# 链接创建模式

在[图形](../../../compositing-graphs/substance-compositing-graphs.md)中，您可以使用以下3种链接创建模式</b>之一连接节点：<b>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![链接创建模式：标准](link-creation-modes.resources/link-creation-mode-standard.gif "链接创建模式：标准"){zoomable="yes"}

*单击以放大*

<b>![](link-creation-modes.resources/image2020-10-6-19-40-25.png)标准</b> (1)

不执行任何条件。

</td>
<td style="border: 0;" valign="top">

![链接创建模式：材料](link-creation-modes.resources/link-creation-mode-material.gif "链接创建模式：材料"){zoomable="yes"}

*单击以放大*

![](link-creation-modes.resources/image2020-10-6-17-11-20.png) <b>材料</b> (2)

根据用途匹配输入和输出。

如果两个模式中只有其中一个有用法，则连接将像在标准模式中那样执行。

</td>
<td style="border: 0;" valign="top">

![链接创建模式：压缩材料](link-creation-modes.resources/link-creation-mode-compact-material.gif "链接创建模式：压缩材料"){zoomable="yes"}

*单击以放大*

![](link-creation-modes.resources/image2020-10-6-19-40-46.png) <b>压缩材料</b> (3)

与材料相同。

属于同一&#x200B;*组*&#x200B;的输入和输出被折叠。

</td>
</tr>
</table>

您可以随时在图形工具栏中通过单击![](link-creation-modes.resources/link-creation-mode.png) <b>链接创建模式</b>按钮或使用上面列出的键盘快捷键在模式之间切换。

在<b>材料</b>和<b>压缩材料</b>模式中，禁止使用&#x200B;*不匹配用法*&#x200B;的输入和输出之间的连接。

## 模式

|  | <div><img data-preserve-html="true" height="23" src="link-creation-modes.resources/image2020-10-6-19-40-25.png"/></div> 标准 | <div><img data-preserve-html="true" height="23" src="link-creation-modes.resources/image2020-10-6-17-11-20.png"/></div> 紧凑 | <div><img data-preserve-html="true" height="23" src="link-creation-modes.resources/image2020-10-6-19-40-46.png"/></div> 紧凑材质 |
| --- | --- | --- | --- |
| <b>输入</b> | 所有输入均可见 | 所有输入均可见 | 每组仅1个输入 |
| <b>输出</b> | 所有输出均可见 | 所有输出均可见 | 每组仅1个输出 |
| <b>链接</b> | 所有链接均可见 | 所有链接均可见 | 每个组仅1个链接（绿色） |
| <b>连接</b> | 逐个连接链接 | 可以根据匹配的用法将链接作为一个多链接材料组连接在一起。   如果一端存在用法，则连接为标准连接。 | 将链接作为一个单链接材质组连接在一起。 |

## 分配组

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

您应该为图形的<b>输入</b>和<b>输出</b>节点分配组，以便使用<b>材质</b>和<b>紧凑材质</b>模式。

通过在<b>组</b>属性中填充组名称，可以在节点的<b>属性</b>参数中分配组。 组可以是任何字符串值，如果链接共享的&#x200B;*完全相同*（区分大小写），则将对链接进行分组。

图形的分组输入和输出在引用该图形的节点实例上&#x200B;*封装在深色胶囊*&#x200B;中以直观方式表示。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![节点上的组胶囊](link-creation-modes.resources/link-creation-mode-group-node.png "节点上的组胶囊"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![组属性](link-creation-modes.resources/link-creation-mode-group.png "组属性"){zoomable="yes"}

*单击以放大*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## 与使用情况匹配的链接

链接分组后，需要将各个输入与输出匹配。 这是通过<b>输入</b>和<b>输出</b>节点的<b>用法</b>属性完成的。 如果输入和输出&#x200B;*之间的使用率匹配*，则将创建链接。 如果未找到匹配的用法，则不会建立链接。

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![用法属性](link-creation-modes.resources/link-creation-mode-usage.png "用法属性"){zoomable="yes"}

*单击以放大*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>
