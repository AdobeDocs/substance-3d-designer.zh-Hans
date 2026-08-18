---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: 使用“从下到上”节点，可根据网格世界位置从下到上生成渐变蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 从下到上
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# 从下到上

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## 从下到上

**在：** *基于网格的生成器/蒙版生成器*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home)中的[智能蒙版](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks)。

这将生成从模型底部到顶部的白色到黑色的过渡，对于进行基于几何的衰减和选择非常有用。

## 参数

### 输入

* **位置**： *颜色输入*\
  烘焙位置图。 必填！
* **粗糙度：** *灰度输入*\
  这与PBR粗糙度无关，而是用于分解过渡的（可选）变化图。 仅在“粗糙度”设置为大于0时显示。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  在黑白图像之间移动结果的平均色阶，就像亮度调整一样。
* **对比度**： *0.0 - 1.0*\
  调整过渡的对比度。
* **粗糙度\_变化**： *0.0 - 1.0*&#x200B;确定粗糙度图要混合以生成变化的量。 将此值增大到0以上可显示映射槽。

## 示例图像

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
