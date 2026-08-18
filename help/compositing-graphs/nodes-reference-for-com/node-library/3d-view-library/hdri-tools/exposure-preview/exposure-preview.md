---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: 在最终渲染之前，使用“曝光度预览”节点预览HDRI环境中的曝光度调整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曝光度预览
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# 曝光度预览

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

## 曝光度预览

**位置：** *3D视图/HDRI 工具*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

用于预览曝光步骤的辅助节点。 用户设置最小值和最大值，节点将使用原始输入的多个不同曝光版本生成一个大得多的图像。 不同版本总是水平栈叠，数量取决于节点或图形的分辨率。

## 参数

* **最大曝光(EV)**： *-8.0 - 8.0*\
  顶部的最大曝光度，最亮的图像。
* **最低曝光度(EV)**： *-8.0 - 8.0*&#x200B;最低曝光度，最暗的图像。

## 示例图像

![](../../../../../../assets/exp-preview-ex.png)

</td>
</tr>
</table>
