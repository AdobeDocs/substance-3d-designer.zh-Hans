---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ""
description: ""
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 输出
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%
---

# 输出

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![原子节点：输出](output.resources/comp_output_1.png "原子节点：输出"){width="100%"}

<b>进入：</b>个原子节点

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Output节点指定图形的<b>结果</b>，如果其中存在多个Output节点，则指定其结果之一。

连接到图形的输出节点的图像或值由表示此图形的任何[实例化](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)输出，并且可以[导出为图形输出](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="output.resources/output-tooltip.gif" alt="输出工具提示" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

同样，当[发布的Sbsar 文件](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)包含此图形时，该文件可以在使用该文件的任何集成或增效工具中输出该图像。

它具有类型无关的单个输入插槽，这意味着它会在连接到它的数据类型之后键入自己。

它没有参数，而是一些对正确标示输出并将其用于预期用途非常重要的属性。

每个图形都必须具有&#x200B;*至少一个*&#x200B;输出节点。 如果不存在输出，则图形无法返回实际结果，并会引发[警告](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md)。

## 属性

|                             |                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>标识符</b> *字符串* | 输出的唯一标识符。 此属性不能留空，也不能包含特殊字符或空格。   由于标识符的标签为“Label”属性，因此该属性留空。 它还可用于命名[导出的纹理](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)。 |
| <b>描述</b> *字符串* | 用作输出的工具提示的可选说明是图形。 |
| <b>标签</b> *字符串* | 这用作输出节点的标签，及其在[实例化](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)中表示此图形的相应连接器。 标签可以包含空格和特殊字符。 |
| <b>用户数据</b> *字符串* | 可用于特定筛选操作的可选元数据。 [Substance 3D Painter](https://www.adobe.com/products/substance3d/apps/painter.html)使用此数据来[驱动某些功能](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/content/creating-custom-effects/user-data)。 |
| <b>组</b> *字符串* | 用于为Designer的[链接创建模式](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)将输出分组的特性。   在“紧凑材料”链接创建模式下，具有相同“组”属性的输出显示为单个连接。 |

## 集成属性

这些属性旨在由使用[已发布Sbsar 文件](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)中的图形的集成/插件使用。

因此，它们不会影响[位图导出](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)的格式。 此外，Designer中仅使用<b>Usage</b>属性，有关详细信息，请参阅下文。

+++ 使用情况

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>组件</b> *字符串* | 用于将某些纹理通道映射到AxF工作流程中的适当SVBRDF着色器输入。 |
| <b>用法</b> *字符串* | 定义输出节点的类型和用法。 此属性在驱动时非常重要：<ul data-preserve-html="true"> <li data-preserve-html="true">使用某些[链接创建模式](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)时连接图形中的节点 </li> <li data-preserve-html="true">纹理与3D 视图中着色器的连接（请参阅下文：“[关于3D 视图中使用者的作用](#about-the-role-of-usages-in-the-3d-view)”）</li> <li data-preserve-html="true">纹理与集成/增效工具中材料的连接</li> </ul> |
| <b>色彩空间</b> *字符串* | 设置解释此输出的色彩空间。 由其他应用程序中的某些集成使用，在Designer中没有影响。 |

+++

### 关于使用在3D 视图中的作用

由于图形输出通常旨在作为特定纹理声道的最终结果，因此输出可以自动发送到3D 视图中使用的着色器的相应采样器。

实际上，<b>用法</b>属性&#x200B;*与3D 视图中的取样器用法*&#x200B;匹配的输出将连接到该取样器。 例如，使用情况为`basecolor`的输出将连接到着色器的`basecolor`取样器。 （了解详情： [以3D视图查看数据](../../../../interface/3d-view/3d-view.md#view-data-in-3d-view)）

单击[图形视图](../../../../interface/the-graph-view/the-graph-view.md)的空白区域上的人民币，然后在上下文菜单中选择<b>在3D视图中查看输出</b>选项，以将所有输出连接到具有&#x200B;*匹配用法*&#x200B;的3D 视图取样器。

>[!IMPORTANT]
>
> 例如，如果按顺序设置了多个使用实例，以将使用实例分配给打包纹理中的频道，则只有&#x200B;*第一个使用实例*&#x200B;将连接到3D 视图。 这是一个已知限制。

## 默认输出

当图形有多个输出时，可以将其中一个输出设置为该图形的默认输出。 这指定应将哪些输出用于：

* 表示该图形的任何实例化的缩略图
* 在2D 视图中查看这些实例化
* 该图形在库中的缩览图（了解如何在[此处](../../../../interface/preferences-window/project-settings/project-settings.md)添加自己的资源）

利用此功能，您可以按任意顺序排列图形输出，而不管如何将图形可视化为节点。

要将“输出”节点设置为图形的默认输出，请执行以下操作：

* 右键单击输出节点，然后在上下文菜单中选择“设置为默认输出”操作。
* 在输出节点的属性中，使用“属性”部分标题中的“设置为默认值”按钮。

以下是设置默认输出之前和之后的实例化示例：

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="output.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>之前</i>
    </td>
    <td style="border: 0">
      <img src="output.resources/defaultouput1.png" alt="defaultouput1">
      <br><i>之后</i>
    </td>
  </tr>
</table>
