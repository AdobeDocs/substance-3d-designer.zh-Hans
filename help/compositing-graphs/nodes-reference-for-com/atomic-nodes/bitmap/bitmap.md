---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: 使用“位图”节点可导入位图图像，并将其用作Substance合成图表中的纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 位图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 989234054615406114d2f7664ebee6f8c86f4bf2
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# 位图

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：位图](bitmap.resources/comp_bitmap.png "原子节点：位图"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

将[位图资源](../../../../resources/bitmap-resource/bitmap-resource.md)加载到图形中。

此节点用于将[位图](../../../../glossary/glossary.md)导入到图形中，或用于创建一个新位图以用于[位图绘画工具](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)。

创建此节点有几种方法，所有这些方法都需要您了解[链接和导入资源之间的区别。](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

您可以从头开始创建节点，也可以将受支持格式的[位图](../../../../glossary/glossary.md)拖放到“图形”视图中。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 可以使用[2D视图](../../../../interface/2d-view/2d-view.md)停放区中的[位图绘制工具](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)来绘制生成的或导入的8位位位图。

>[!IMPORTANT]
>
> 此节点依赖于外部资源，因此在使用它们时需要注意以下几点：
> 
> * 位图节点可以返回彩色或灰度，但即使资源是灰度位图，也默认为彩色。 这可能会影响图形性能和复杂性，因此请始终确保根据需要切换到“灰度”[颜色模式](#parameters)。
> * 删除位图节点不会删除[包](../../../../glossary/glossary.md)中的[位图资源](../../../../resources/bitmap-resource/bitmap-resource.md)，您必须在[资源管理器](../../../../interface/the-explorer-window/the-explorer-window.md)中手动执行此操作。
> * 另一方面，在资源管理器中删除[位图资源](../../../../resources/bitmap-resource/bitmap-resource.md)时要小心：由于它保留在缓存中，因此它仍可在该会话的图形中工作，但在您下次加载[包](../../../../glossary/glossary.md)时，该资源将被标记为缺失。
> * 当Substance图形为[熟悉](../../../../glossary/glossary.md)时，位图分辨率将固定为图形内的分辨率，而不是基于其原始大小。 建议确保Bitmap节点的“Output size”[基参数](../../../../glossary/glossary.md)使用“Absolute”[继承方法](../../../../glossary/glossary.md)，并且节点后跟设置为“相对于父项”的[Transform 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)节点（即主机图形的分辨率）。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 参数

</td>
<td style="border: 0;" valign="top">

### 位图绘画工具

</td>
<td style="border: 0;" valign="top">

### 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>颜色模式</b> *布尔值* | 确定节点的输出类型，以返回彩色或灰度。 |
| <b>PKG资源路径</b> *字符串* | 节点引用的[位图资源](../../../../resources/bitmap-resource/bitmap-resource.md)的路径。   建议不要手动键入，而是从资源管理器中复制资源并将其粘贴到参数文本字段中，或者将位图资源直接从[资源管理器](../../../../interface/the-explorer-window/the-explorer-window.md)拖放到图形中的位图节点上。 |
| <b>调整方法大小</b> *整数* | 在放大或缩小位图时要使用的重新采样方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>平滑拉伸：</i>应用[双线性筛选](../../../../glossary/glossary.md)以插值于拉伸图像的源像素。</li> <li data-preserve-html="true"><i>最接近拉伸：</i>拉伸图像并使用最接近的源像素的颜色。</li> </ul> |

## 位图绘画工具

位图可以在Designer中进行编辑。 了解有关[此部分](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)中编辑工具的更多信息。

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

*即将推出。*
