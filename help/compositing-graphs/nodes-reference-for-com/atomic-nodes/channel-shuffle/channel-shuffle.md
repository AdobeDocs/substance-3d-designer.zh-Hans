---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: 使用“通道随机排布”节点重新排列纹理中的颜色通道，以创建颜色效果和通道交换。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通道随机混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# 通道随机混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：通道随机排布](../../../../assets/comp_shuffle.png "原子节点：通道随机排布"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

将一个或两个输入图像的颜色通道重新排列到输出图像中。

即，获取两个输入并允许您返回输出，其中红色、绿色、蓝色和Alpha声道中的任何一个被交换或设置为来自输入的任何声道。

实际上，它允许您以任何可能的方式打包和交换RGB通道。 灰度输入将被视为是彩色输入：红色、绿色、蓝色和Alpha都返回相同的值。

</td>
</tr>
</table>

“声道随机排布”具有基本选项，但在大多数声道打包或去除和设置Alpha声道的情况下，使用[RGBA合并](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)、[RGBA拆分](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md)、[Alpha合并](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md)和[Alpha拆分](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)更快。 这些模板设置为执行默认操作，不需要更改多个参数并在之后转换为灰度。 如果您使用的是包含更多混合选项的更高级版本，请查看[通道混合器](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md)。

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

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>红色通道</b> *整数* | 选择要插入到输出图像的红色通道中的源通道。 |
| <b>绿色通道</b> *整数* | 选择要插入到输出图像的绿色通道中的源通道。 |
| <b>蓝色通道</b> *整数* | 选择要插入到输出图像的蓝色通道的源通道。 |
| <b>Alpha频道</b> *整数* | 选择要插入到输出图像的Alpha声道的源声道。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入1</b> *彩色/灰度*&#x200B;主要 | 主输入图像。 |
| <b>输入2</b> *彩色/灰度* | 次输入映像。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

*即将推出。*
