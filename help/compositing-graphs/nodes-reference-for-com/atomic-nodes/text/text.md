---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ""
description: 使用“文本”节点生成具有可自定义纹理和样式的文本字体，以创建基于文本的图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 文本
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%
---

# 文本

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![原子节点：文本](text.resources/comp_text_1.png "原子节点：文本"){width="100%"}

<b>进入：</b>个原子节点

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

“文本”节点提供了一种在图形中置入用户创建的文本的方法。 用户还可以选择字体、对齐方式和旋转等设置以自定义文本放置。

“文本”节点功能非常强大，是轻松放置文本的唯一方式。 使用时可能会有些困难，因为放置内容总是在有限的方形画布上进行，并且字体由系统定义的外部列表驱动。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="text.resources/text-tooltip.gif" alt="文本工具提示" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

仅支持Truetype (.ttf)和某些Opentype字体。 如果列表中缺少任何字体，可能是因为这个原因。 <b>字体无法作为参数公开。</b>

将使用“文本”的图形发布到sbsar时，字体将嵌入到包中，就像位图和其他资源一样，以确保在所有系统和应用程序中使用字体。



## 参数

|  |  |
| --- | --- |
| <b>颜色模式</b> *布尔值* | 在灰度图像和彩色输出图像之间切换。 |
| <b>文本</b> *字符串* | 确定文本说明。 |
| <b>字体</b> *字符串* | 用于呈现文本的字体资源。 |
| <b>字体大小</b> *Float* | 文本的字体大小（以点为单位）。 |
| <b>对齐</b> *整数* | 将文本对齐方式设置为左对齐、居中（默认）或右对齐。 |
| <b>转换</b> *Float4* | 应用于渲染文本的2x2变换矩阵。 |
| <b>位置</b> *Float2* | 文本在输出图像中的位置。 |
| <b>背景</b> *Float/Float4* | 输出图像的背景色。 |
| <b>字体颜色</b> *Float/Float4* | 文本的颜色。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>背景</b> *灰度/颜色*&#x200B;主要 | 输出图像的背景色。 |


## 示例

*即将推出。*
