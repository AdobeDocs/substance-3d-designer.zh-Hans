---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: 利用“多角度 — 法向”法线图，从多角度扫描图像中生成精确表面细节的节点。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多角度法线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# 多角度法线

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点从在不同光照条件下拍摄的一组照片/扫描中构造一个正常映射。 与尝试从单个反照率图像中提取法线相比，它允许进行更精确的法线映射转换。

它比[多角度反照率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)更复杂，因为它要求您为输入使用设置精确的光照角度。 每个样本的光照角度应该均匀分布，并且需要按顺序输入样本。 因此，对于三个样本，光照角度应该取为：0、120、240 — 或该角度的任何统一偏移量（例如90、210、330）。

>[!NOTE]
>
> 有关此节点的反照率版本，请参阅[反照率多角度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)。 如果要对输入进行预处理，[多Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、[多裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md)和[多仿制修补](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)可能会很有用，因为它们旨在与这些节点组合使用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入1-8</b> <i>颜色输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>样本量</b> <i>2 - 8</i> | 设置要处理的样本量（输入）。 |
| <b>强度</b> <i>0.0 - 1.0</i> | 设置正常映射强度。 |
| <b>第一个示例光线角度</b> <i>0.0 - 360.0</i> | 设置第一个输入的光照角度方向。 |
| <b>下一个示例光线角度</b> <i>逆时针，顺时针</i> | 设置下一个采样中光照移动的方向。 |
