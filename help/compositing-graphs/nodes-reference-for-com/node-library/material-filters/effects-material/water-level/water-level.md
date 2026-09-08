---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: 使用“水位”节点可根据水位Height混合材料，以创建逼真的水面效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水位
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# 水位

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## 水位

**范围：** *材质过滤器/效果*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

将水位添加到完整材料输入的一体式效果。 输入材料必须拥有优质、高质量的Heightmap效果才能发挥作用。 结果是PBR正确的。

## 参数

### 输入

* **蒙版**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **频道**\
  在此组中打开和关闭材料声道，例如，在使用Specular/光泽度映射而非金属/粗糙度时。
* **水位**： *0.0 - 1.0*&#x200B;用于升高或降低水位的主控件。
* **水黑度**： *0.0 - 1.0*&#x200B;设置水的常规“透明度”。
* **边缘湿度**： *0.0 - 1.0*&#x200B;确定水边缘应该具有多少湿外观。
* **边缘湿度距离**： *0.0 - 1.0*&#x200B;设置湿边缘可达到的距离。
* **深度模糊量**： *0.0 - 1.0*&#x200B;根据水面以下深度设置模糊量。 修改模糊半径。
* **深度模糊不透明度**： *0.0 - 1.0*&#x200B;确定混合了多少深度模糊，可用于降低模糊效果。
* **污泥颜色**： *（颜色值）*设置污泥效果的颜色。
* **污泥深度**： *0.0 - 1.0*&#x200B;设置污泥开始出现的深度（相对于水位）。
* **污泥不透明度**： *0.0 - 1.0*&#x200B;设置污泥效果的全球不透明度。
* **霜冻**： *0.0 - 1.0*&#x200B;设置霜冻量。 开始从外边缘出现并向内移动。
* **霜冻强度**： *0.0 - 1.0*&#x200B;设置霜冻强度，控制效果的“不透明度”。
* **Frost裂缝**： *0.0 - 1.0*&#x200B;设置从冻结到液体过渡中的裂缝量。
* **Frost Normal Format**： *DirectX/OpenGL*&#x200B;开关Frost Normalmap效果绿色通道。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
