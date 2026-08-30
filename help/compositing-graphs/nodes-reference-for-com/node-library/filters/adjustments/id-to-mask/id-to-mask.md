---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: 使用“ID到蒙版灰度”节点，将ID映射值转换为用于材质选择的灰度蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 用于遮盖灰度的ID
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# 用于遮盖灰度的ID

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![用于遮盖灰度图标的ID](id-to-mask.resources/IDToMask.png "用于遮盖灰度图标的ID"){width="200px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在ID映射中创建蒙版，其中具有选定像素值的像素为白色。

ID图是整体像素（如形状）全部包含相同唯一标识值的图像。 在本例中，该值是一个整数。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>ID</b> <i>灰度</i>主要 | 应从中提取蒙版的输入ID映射。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 从输入ID映射中提取的二进制蒙版。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>选择模式</b> *整数* | 在ID图中选择蒙版中应为白色的像素值的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>独奏：</b>选择单个像素值</li> <li data-preserve-html="true"><b>范围：</b>选择像素值范围</li> </ul> |
| <b>ID整数</b> *整数* *在“选择模式”设置为“独奏”时可用* | ID映射中的像素值，它在输出蒙版中应为白色。 |
| <b>ID范围</b> *整数2* *在“选择模式”设置为“范围”时可用* | ID映射中像素值的范围（从开始到结束），它在输出蒙版中应为白色。 |

## 示例

<table>
  <tr>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![要遮盖的ID：示例2](id-to-mask.resources/id_to_mask_example_2.gif "要遮盖的ID：示例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![要遮盖的ID：示例3](id-to-mask.resources/id_to_mask_example_3.png "要遮盖的ID：示例3"){zoomable="yes"}

</td>
</tr>
</table>
