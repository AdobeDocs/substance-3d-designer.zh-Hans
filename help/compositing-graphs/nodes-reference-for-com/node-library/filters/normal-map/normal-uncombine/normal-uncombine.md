---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: 使用“法线取消组合”节点将组合的法线映射数据拆分为单独的X、Y和Z组件。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常取消合并
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# 正常取消合并

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![正常取消合并图标](normal-uncombine.resources/normal-uncombine-01.png "正常取消合并图标"){width="200px"}

<b>英寸：</b>滤镜>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从法线映射中删除由Height映射描述的曲面细节。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>正常合并</b> <i>颜色</i>主要 | 应从中删除详细信息的正常映射。 |
| <b>Height</b> <i>灰度</i> | 表示应从组合法线图中删除的表面细节的Height图。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>未组合的普通</b> <i>颜色</i> | 从中删除输入Height映射所描述的曲面细节的法线映射。 |
| <b>猜测的强度</b> <i>浮动</i> | 强度估计，应设置为与输入Height映射连接的[法线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)节点，以匹配输入法线映射的强度。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>正常格式</b> *整数* | 输入法线图的格式。 有效地反转绿色通道。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX：</b> Y轴指向上</li> <li data-preserve-html="true"><b>OpenGL：</b> Y轴指向下</li> </ul> |

## 示例

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-02.jpg" alt="normal_uncombine_example_3_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-03.jpg" alt="normal_uncombine_example_3_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![正常取消合并：示例2](normal-uncombine.resources/normal-uncombine-04.png "正常取消合并：示例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-05.jpg" alt="normal_uncombine_example_1_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-06.jpg" alt="normal_uncombine_example_1_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![正常取消合并：示例4](normal-uncombine.resources/normal-uncombine-07.png "正常取消合并：示例4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-08.jpg" alt="normal_uncombine_example_2_before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-09.jpg" alt="normal_uncombine_example_2_after">
      <br><i>之后</i>
    </td>
  </tr>
</table>

![正常取消合并：示例6](normal-uncombine.resources/normal-uncombine-10.png "正常取消合并：示例6"){zoomable="yes"}
