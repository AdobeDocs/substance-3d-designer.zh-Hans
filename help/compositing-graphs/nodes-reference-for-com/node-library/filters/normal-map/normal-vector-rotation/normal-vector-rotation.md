---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: 使用“法线矢量旋转”节点旋转法线映射矢量，以调整表面光照和细节方向。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法线矢量旋转
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# 法线矢量旋转

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation-01.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

旋转切空间中输入Normalmap的所有向量的常规实用节点。 并不会真正变换像素，而会修改它们所表示的值 它可以利用可选映射向灰度小平面添加随机旋转。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>正常</b> <i>颜色输入</i> | 要执行旋转的基本映射。 必需。 |
| <b>旋转贴图（可选）</b> <i>灰度输入</i> | 调整旋转强度的灰度映射。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>旋转角度</b> <i>0.0 - 1.0</i> | 设置旋转正常映射的角度 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同的法线贴图格式之间切换（反转绿色通道） |
