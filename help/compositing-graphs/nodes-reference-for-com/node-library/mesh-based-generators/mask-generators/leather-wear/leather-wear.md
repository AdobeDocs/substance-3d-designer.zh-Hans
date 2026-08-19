---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: 使用“皮革磨损”节点，根据网格曲率和接触点在皮革表面生成磨损蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 皮革磨损
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# 皮革磨损

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## 皮革磨损

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版使用皮革图案表示磨损，基于曲率在边缘表示更多磨损。 其功能与[玻璃纤维Edge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md)相似，参数基本相同。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于边放置的已烘焙贴图。 必填！
* **环境遮蔽**： *灰度输入*\
  使用的已烘焙贴图遮蔽了某些区域。 推荐，但不是必需的。
* **污渍输入**： *灰度输入*\
  可选污渍映射输入插槽，可通过“使用自定义污渍”参数切换。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **磨损级别**： *0.0 - 1.0*&#x200B;设置全局磨损级别，逐渐显示。
* **佩戴对比度**： *0.0 - 1.0*&#x200B;设置效果的对比度。
* **污渍量**： *0.0 - 1.0*&#x200B;设置要在边缘之间混合的污渍量（默认皮革图案）。
* **环境遮蔽蒙版**： *0.0 - 1.0*&#x200B;设置AO遮蔽磨损效果的范围。
* **曲率粗细**： *0.0 - 1.0*&#x200B;设置曲率边缘影响最终结果的范围。 即使设置为0，您仍需要曲率图。
* **使用自定义污渍**： *False/True*&#x200B;启用覆盖内置默认皮革图案。 请改用自定义输入槽。

## 示例图像

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
