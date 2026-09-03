---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/cube-3d-gbuffers.html"
breadcrumb-title: ''
description: 使用“立方3D GBuffers”节点从3D立方投影生成几何缓冲器以获得高级渲染效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Cube 3D GBuffers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 立方体3D GBuffer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---


# 立方体3D GBuffer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cube-3d-gbuffers.resources/cube-3d-gbuffers-01.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

[Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)的高级版本，它同时输出Position和法线图而不是heightmap。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>方向偏移</b> | 允许立方体进行类似3D的X和Y旋转。 也可以通过在2D预览中操作小点来完成。 |
| <b>大小</b> <i>0.0 - 1.0</i> | 允许立方体的非均匀重新缩放。 |
| <b>缩放</b> <i>0.0 - 1.0</i> | 统一重新缩放整个立方体。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用以非方形比例补偿挤压和拉伸。 |
