---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: 使用“位图转换为材质光照”节点可以将位图图像快速转换为具有优化光照的材质，从而实现快速工作流程。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 将位图转换为材质光照
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# 将位图转换为材质光照

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## 将位图转换为材质光照

**位置：** *材质滤镜/1键单击*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点将单个漫射/基色输入转换为完整素材。 作为[Allegorithmic完全成熟的Bitmap2素材的简单“浅色”版本（可单独购买）](https://www.allegorithmic.com/products/bitmap2material)，它为您提供了完整版本的些许体验。 对于较简单的情形，它可以很好地工作。

虽然无法保证生成完美的PBR校正素材，但如果您只有一个图像并且需要完整的素材，这是一种好且快速入门的方法。

## 参数

* **频道**
  * 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。
* **全局**
  * **深度平衡**： *-1.0 - 1.0*&#x200B;设置Heightmap的偏差/偏移。
* **扩散**
  * **锐化**： *0.0 - 1.0*&#x200B;将锐化添加到扩散结果。
  * **色相**： *0.0 - 1.0*&#x200B;色调扩散，用户选择色相偏移。
  * **饱和度**： *0.0 - 1.0*&#x200B;修改扩散结果的饱和度。
  * **亮度**： *0.0 - 1.0*&#x200B;调整扩散结果亮度。
  * **对比度**： *-1.0 - 1.0*\
    调整结果的对比度。
* **浮雕**\
  浮雕组同时控制正常输出和Height输出。
  * **输出普通格式**：*DirectX，OpenGL*&#x200B;在正常格式之间切换（翻转绿色）。
  * **反转生成的浮雕**： *False/True*&#x200B;反转Height的解释。
  * **正常强度**： *0.0 - 20.0*&#x200B;设置生成的正常映射的强度。
  * **浮雕均衡器**： *0.0 - 1.0*&#x200B;为不同的细节比例设置转换余额。
  * **挤压强度**： *0.0 - 1.0*&#x200B;使正常过渡更清晰。 在转换为正常图像之前，可以先有效地添加锐化滤镜，使边缘更加明显。
  * **正常锐化**： *0.0 - 1.0*&#x200B;转换后锐化正常映射，以显示细节。
  * **正常柔化**： *0.0 - 1.0*&#x200B;转换后柔化正常映射，隐藏细节。
* **Specular**
  * **Specular扩散影响**： *0.0 - 1.0*&#x200B;设置扩散对Specular的影响。 还影响“光泽度”和“粗糙度”输出。
  * **Specular饱和度**： *0.0 - 1.0*&#x200B;更改Specular输出的饱和度。
  * **Specular锐化**： *0.0 - 1.0*&#x200B;锐化Specular输出。
  * **在**&#x200B;中的Specular level： *0.0 - 1.0*&#x200B;设置用于Specular解释的输入级别。
  * **Specular level输出**： *0.0 - 1.0*&#x200B;修改Specular的输出级别。
  * **金属Specular影响**： *0.0 - 1.0*&#x200B;确定可选金属输入对Specular映射的影响。
* **光泽度**
  * **1}中的光泽度级别： *0.0 - 1.0*设置光泽度解释的输入级别。**
  * **光泽度色阶输出**： *0.0 - 1.0*&#x200B;修改光泽度输出色阶。
  * **金属光泽度影响**： *0.0 - 1.0*&#x200B;确定可选金属输入对光泽度图的影响。
* **粗糙度**
  * **粗糙度级别**： *0.0 - 1.0*&#x200B;设置粗糙度解释的输入级别。
  * **粗糙度色阶输出**： *0.0 - 1.0*&#x200B;修改粗糙度输出色阶。
  * **金属粗糙度影响**： *0.0 - 1.0*&#x200B;确定可选金属输入对光泽度图的影响。
* **环境遮蔽**
  * **漫射中的环境遮蔽**： *0.0 - 1.0*&#x200B;将生成的AO中的混合输出到漫射输出中。
  * **环境遮蔽跨页**： *0.0 - 1.0*&#x200B;设置生成AO跨页的距离。
  * **环境遮蔽光距离**： *0.0 - 1.0*&#x200B;设置AO“深度”解释。 当跨距较大时，影响较小。
  * **环境遮蔽光角度**： *0.0 - 1.0*&#x200B;设置假光照AO投射角度。 如果设置为相反角度，可用于补偿漫射中已有的任何方向AO。
  * **环境遮蔽色阶**： *0.0 - 1.0*&#x200B;修改AO输出色阶。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
