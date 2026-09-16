---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ""
description: 使用“浮雕”节点在纹理上创建浮雕效果，为表面细节添加深度和浮雕。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 浮雕效果
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 9%
---

# 浮雕效果

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![原子节点：浮雕](emboss.resources/comp_emboss_1.png "原子节点：浮雕")

</td>
<td style="border: 0;" valign="top">

根据指定的光源方向照亮图像中形状的侧面，以此应用浮雕效果。

即，该节点基于两个输入执行简单的二维着色，模拟光落在具有Height和深度变化的表面上。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="emboss.resources/emboss-tooltip.gif" alt="浮雕工具提示" /></div>

此节点不常用于类似PBR的项目，但在纹理中需要简单烘焙的光照时，它可以发挥作用。 或者，[光泽浮雕](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md)和[Uber浮雕](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)提供类似但更广泛的功能。



## 参数

|  |  |
| --- | --- |
| <b>强度</b> *浮动* | 调整照明效果的全局强度。   设置“Height”映射的强度，从而设置光照效果的强度 |
| <b>光线角度</b> *浮动* | 设置模拟光线的角度。   定义浮雕图像高光的照明角度 |
| <b>突出显示颜色</b> *浮动/浮动4* | 设置面向光源角度的区域颜色。   如果输入图像是彩色，则设置高亮显示的颜色。 |
| <b>阴影颜色</b> *浮动/浮动4* | 设置背向光源角度的区域的颜色。   设置浮雕图像的阴影区域的颜色。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色*&#x200B;主要 | 提供基础的未着色颜色。 将其视为一种漫射或基色纹理。 |
| <b>强度输入</b> *灰度* | 表示用于计算表面光线的高度图。 黑是低，白色是高。 |


## 示例

*即将推出。*
