---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: 使用“正常取消组合”节点将组合法线图数据拆分为单独的X、Y和Z组件。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常取消合并
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# 正常取消合并

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![正常取消合并图标](../../../../../../assets/NormalUncombine.png "正常取消合并图标"){width="200px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从法线图中移除由高度图描述的曲面细节。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 输出连接器

</td>
<td style="border: 0;" valign="top">

### 参数

</td>
</tr>
</table>

## 输入连接器

|  |  |
| --- | --- |
| <b>正常合并</b> *颜色*&#x200B;主要 | 应从中删除详细信息的法线图。 |
| <b>Height</b> *灰度* | 表示应从组合法线图中移除的曲面细节的高度图。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>未组合的普通</b> *颜色* | 删除由输入高度图描述的曲面细节的法线图。 |
| <b>猜测的强度</b> *Float* | 强度估计，为了匹配输入高度图的强度，应将其设置为与输入法线图连接的[正常](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)节点。 |

## 参数

|  |  |
| --- | --- |
| <b>正常格式</b> *整数* | 输入法线图的格式。 有效地反转绿色通道。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX：</b> Y轴指向</li> <li data-preserve-html="true"><b>OpenGL：</b> Y轴点向下</li> </ul> |

## 示例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![正常取消合并：示例2](../../../../../../assets/normal_uncombine_example_4.png "正常取消合并：示例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![正常取消合并：示例4](../../../../../../assets/normal_uncombine_example_6.png "正常取消合并：示例4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![正常取消合并：示例6](../../../../../../assets/normal_uncombine_example_5.png "正常取消合并：示例6"){zoomable="yes"}
