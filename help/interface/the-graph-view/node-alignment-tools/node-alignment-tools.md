---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/the-graph-view/node-alignment-tools.html"
breadcrumb-title: ''
description: 使用节点对齐工具组织和对齐图形视图中的节点，可获得更清晰、可读性更高的图形。
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node alignment tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 节点对齐工具
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---


# 节点对齐工具

![节点对齐工具栏](../../../assets/node-alignment-toolbar.png "节点对齐工具栏"){zoomable="yes"}

节点对齐工具允许您在图中排列节点，以提高节点的可读性和创作体验。 它们提供了对齐节点、均匀分布节点和对齐网格的操作。

它们只对当前选定的<b>节点</b>起作用。

>[!NOTE]
>
> 键盘快捷键
> 
> 某些操作具有快速访问的键盘快捷键：H、V和S。它们显示在下面操作列表的括号之间。
> 
> 请注意，它们将覆盖分配给节点的任何[键盘快捷键](../../../interface/preferences-window/preferences-window.md)。

## 对齐

节点可以水平和垂直对齐，每个轴有三种模式：

### 水平对齐

<b>![](../../../assets/node-alignment-h-left.png)左侧：</b>将所选节点的左侧与最左侧节点的左侧对齐。

<b>![](../../../assets/node-alignment-h-center.png)居中(H)：</b>将所选节点的水平中心与围绕它们的定界框的水平中心对齐。

<b>![](../../../assets/node-alignment-h-right.png)右侧：</b>将所选节点的右侧与最右侧节点对齐。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点对齐工具：左](../../../assets/node-alignment-left.gif "节点对齐工具：左"){zoomable="yes"}

*左*

</td>
<td style="border: 0;" valign="top">

![节点对齐工具：居中](../../../assets/node-alignment-center.gif "节点对齐工具：居中"){zoomable="yes"}

*居中*

</td>
<td style="border: 0;" valign="top">

![节点对齐工具：右](../../../assets/node-alignment-right.gif "节点对齐工具：右"){zoomable="yes"}

*右*

</td>
</tr>
</table>

### 垂直对齐

<b>![](../../../assets/node-alignment-v-top.png)顶部：</b>将所选节点的顶部与最上面的节点的顶部对齐。

<b>![](../../../assets/node-alignment-v-middle.png)中间(V)：</b>将所选节点的垂直中心与围绕它们的定界框的垂直中心对齐。

<b>![](../../../assets/node-alignment-v-bottom.png)底部：</b>将所选节点的底边与最低节点的底边对齐。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点对齐工具：上](../../../assets/node-alignment-top.gif "节点对齐工具：上"){zoomable="yes"}

*顶*

</td>
<td style="border: 0;" valign="top">

![节点对齐工具： middle](../../../assets/node-alignment-middle.gif "节点对齐工具： middle"){zoomable="yes"}

*中间*

</td>
<td style="border: 0;" valign="top">

![节点对齐工具：底部](../../../assets/node-alignment-bottom.gif "节点对齐工具：底部"){zoomable="yes"}

*下*

</td>
</tr>
</table>

### 堆叠

使用对齐时，<b>栈叠</b>选项![](../../../assets/node-alignment-stack.png)允许您<b>避免任何重叠</b>。 默认情况下，此选项处于启用状态。

启用后，节点将尽可能移动到参考位置，直到它们与所选节点中的另一个节点发生冲突为止。 这有效地将它们栈叠在所选轴上，每个节点之间有一个中间网格单元的边界。

![节点对齐工具：栈叠](../../../assets/node-alignment-stacking.gif "节点对齐工具：栈叠"){zoomable="yes"}

## 分配

节点可以在所期望轴上当前选择的每个极端上均匀地分布到节点之间。

<b>![](../../../assets/node-alignment-distribute-h.png)水平：</b>节点均匀分布在选区中最左边和最右边的节点之间。

<b>![](../../../assets/node-alignment-distribute-v.png)垂直：</b>节点均匀分布在选择项中最顶层和最底层的节点之间。

分布的目标是节点之间的<b>均匀间距</b>，而不管节点的大小如何。

当多个节点的中心完全对齐到选定轴上时，它们会保留下来，并且在分布中<b>被视为1</b>。 对齐节点中的&#x200B;*最大*&#x200B;用于计算偶数间距。

请注意，当选定节点的总大小大于选定轴上的可用空间时，可能会发生重叠。

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

![节点对齐工具：水平分布](../../../assets/node-alignment-distribute-h.gif "节点对齐工具：水平分布"){zoomable="yes"}

*水平*

</td>
<td width="100.00%" style="border: 0;" valign="top">

![节点对齐工具：垂直分布](../../../assets/node-alignment-distribute-v.gif "节点对齐工具：垂直分布"){zoomable="yes"}

*垂直*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

## 网格对齐

<b>对齐(S) ![](../../../assets/node-alignment-snap.png)</b>操作可移动每个选定节点，以便其左上角位于媒体网格上最近的点。

</td>
<td width="100.00%" style="border: 0;" valign="top">

![节点对齐工具：网格对齐](../../../assets/node-alignment-snapping.gif "节点对齐工具：网格对齐"){zoomable="yes"}

</td>
</tr>
</table>
