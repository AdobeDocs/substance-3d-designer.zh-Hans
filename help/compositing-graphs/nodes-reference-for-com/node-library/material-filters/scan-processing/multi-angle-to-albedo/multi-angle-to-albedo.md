---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: 使用多角度反照率节点从多角度扫描图像中提取反照率映射，以获得干净的材料。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多角度反照率
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# 多角度反照率

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-albedo.resources/multi-angle-to-albedo.png){width="128px"}

<b>在</b>个材质过滤器中>扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点尝试从在不同光源角度下拍摄的一组输入照片/扫描图像中移除所有光源信息。 它将所有样本合并到一个图像中，该图像应是光照中性的，因此可能具有PBR校正。

请记住，您拥有的样本越多，光照角度的差异越大，您将取得更大的成功。 从四个样本开始，根据输入图像的不同，应该有可能获得近乎完美的结果。 输入图像应该与三脚架一起拍摄，除了从不同角度拍摄的光照之外，差异应该小到几乎为零，理想情况下甚至没有任何差异！

>[!NOTE]
>
> 有关此节点的正常映射版本，请参阅[多角度到正常](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)。 如果要对输入进行预处理，[多Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、[多裁剪](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md)和[多仿制修补](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)可能会很有用，因为它们旨在与这些节点组合使用。
> 
> [博客文章“您的智能手机是材料扫描仪”对此过程进行了更好的说明。](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入1-8</b> <i>颜色输入</i> | 输入数量由样本量参数决定。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>样本量</b> <i>2 - 8</i> | 设置要在处理中使用的样本（输入）数。 |
