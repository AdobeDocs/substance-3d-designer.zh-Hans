---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: 使用Tri平面节点从三个正交平面投影纹理，在复杂几何上实现无缝纹理映射。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 三平面
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# 三平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

<b>在</b>中基于网格的生成器>实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

该高级节点基于烘焙的位置和三平面投影数据在2D中执行世界空间法线映射。 这意味着它实际上完全将UV坐标转换为基于网格本身的（大多数）无接缝映射。

这是避免接缝的好方法，不必每次都重新生成（使用Baker可以实现类似效果）。 缺点是这个节点很重，所以速度不快。

请记住，烘焙应具有高精度：8位烘焙不会产生非常好的结果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>位置</b> <i>颜色输入</i> | 烘焙位置映射。 理想情况下为16位或更高的精度。 |
| <b>世界空间正常</b> <i>颜色输入</i> | 烘焙的世界空间法线图，理想情况下为16位或更高的精度。 |
| <b>输入X</b> <i>彩色输入（灰度输入）</i> | 通过三平面投影从UV重新映射到世界空间的输入图。 当“图像输入”设置为1时，适用于所有轴；如果设置为3，适用于X轴。 |
| <b>输入Y</b> <i>彩色输入（灰度输入）</i> | 仅当图像输入设置为3时。 在Y轴上从UV重新映射到世界空间的输入图。 |
| <b>输入Z</b> <i>彩色输入（灰度输入）</i> | 仅当图像输入设置为3时。 在Z轴上从UV重新映射到世界空间的输入图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>投影</b> <i>所有轴、仅限X、仅限Y、仅限Z</i> | 设置要混合的轴。 |
| <b>图像输入</b> <i>1个输入，3个输入</i> | 设置是为所有轴使用一个映射，还是为每个轴使用一个特定映射。 |
| <b>混合模式</b> <i>线性，高级</i> | 提高准确性和精确度。 |
| <b>混合对比度</b> <i>0.001 - 1.0</i> | 过渡对比度，在平滑或粗糙过渡之间混合。 |
| <b>标准化因子</b> <i>0.0 - 1.0</i> | 通过恢复混合区域的对比度损失来改善投影混合。 |
| <b>拼贴</b> <i>0.0 - 10.0</i> | 平铺输入纹理的次数。 |
| <b>全局轮换</b> <i>0.0 - 1.0</i> | 所有轴的全局轮换。 |
| <b>修复镜像投影</b> <i>False/True</i> | 设置如何处理镜像投影。 |
| <b>旋转X</b> <i>0.0 - 1.0</i> | 在投影X轴上单独旋转。 |
| <b>旋转Y</b> <i>0.0 - 1.0</i> | 在投影Y轴上单独旋转。 |
| <b>旋转Z</b> <i>0.0 - 1.0</i> | 沿投影Z轴进行单独旋转。 |
| <b>偏移X</b> <i>0.0 - 1.0</i> | 在投影X轴上偏移。 |
| <b>随机偏移X</b> <i>0.0 - 1.0</i> | 允许X轴偏移的随机化。 |
| <b>偏移Y</b> <i>0.0 - 1.0</i> | 在投影Y轴上偏移。 |
| <b>随机偏移Y</b> <i>0.0 - 1.0</i> | 允许Y轴偏移的随机化。 |
| <b>偏移Z</b> <i>0.0 - 1.0</i> | 在投影Z轴上偏移。 |
| <b>随机偏移Z</b> <i>0.0 - 1.0</i> | 允许Z轴偏移的随机化。 |
