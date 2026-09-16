---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ""
description: 使用“通道随机混合”节点重新排列纹理中的颜色通道，以创建颜色效果和通道交换。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通道随机混合
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 7%
---

# 通道随机混合

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![原子节点：通道随机混合](channel-shuffle.resources/comp_shuffle.png "原子节点：通道随机混合"){width="100%"}

<b>进入：</b>个原子节点

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

将一个或两个输入图像的颜色通道重新排列到输出图像中。

即，获取两个输入并允许您返回输出，其中红色、绿色、蓝色和Alpha 通道中的任何一个被交换或设置为来自输入的任意声道。

实际上，它允许您以任何可能的方式打包和交换RGB通道。 灰度输入将被视为是彩色输入：红色、绿色、蓝色和Alpha都返回相同的值。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="channel-shuffle.resources/channels-shuffle-tooltip.gif" alt="“通道随机排布”工具提示" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

“通道随机排布”具有基本选项，但在大多数通道打包或去除和设置Alpha 通道的情况下，使用[RGBA合并](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)、[RGBA拆分](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md)、[Alpha合并](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md)和[Alpha拆分](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)会更快。 这些模板设置为执行默认操作，不需要更改多个参数并在之后转换为灰度。 如果您使用的是包含更多混合选项的更高级版本，请查看[通道混合器](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md)。



## 参数

|  |  |
| --- | --- |
| <b>红色通道</b> *整数* | 选择要插入到输出图像的红色通道的源通道。 |
| <b>绿色通道</b> *整数* | 选择要插入到输出图像的绿色通道的源通道。 |
| <b>蓝色通道</b> *整数* | 选择要插入到输出图像的蓝色通道的源通道。 |
| <b>Alpha 通道</b> *整数* | 选择要插入到输出图像Alpha 通道的源通道。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入1</b> *彩色/灰度*&#x200B;主要 | 主要输入图像。 |
| <b>输入2</b> *彩色/灰度* | 辅助输入图像。 |


## 示例

*即将推出。*
