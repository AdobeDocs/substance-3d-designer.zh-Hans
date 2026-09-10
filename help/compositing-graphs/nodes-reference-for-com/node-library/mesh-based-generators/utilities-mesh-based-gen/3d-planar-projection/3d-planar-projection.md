---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: 使用3D投影节点使用平面投影将纹理投影到网格表面上以进行纹理映射。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# 3D投影

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-planar-projection.resources/3d-planar-gray.png)![](3d-planar-projection.resources/3d-planar.png)

<b>在</b>中基于网格的生成器>实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据烘焙的网格数据（“位置”和“世界”法线图）执行平面投影。 允许您跨接缝投影和置入贴花，与原始UV映射无关。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>位置图</b> <i>颜色输入</i> | 烘焙位置图 |
| <b>世界空间正常</b> <i>颜色输入</i> | 世界空间法线映射 |
| <b>投影的纹理</b> <i>颜色输入</i> | 输入纹理以投影到目标上。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>定位</b> |  |
| <b>项目输入</b> <i>UV位置，世界空间位置</i> | 选择投影位置是以2D/UV还是以3D/世界空间设置。 |
| <b>目标UV位置</b> | 仅使用“UV位置输入”，最适用于在“位置”地图上的2D 视图中选取一个点。 |
| <b>目标位置</b> <i>（颜色值）</i> | 仅使用“世界空间位置输入”可定义精确的3D坐标。 |
| <b>目标正常</b> <i>（颜色值）</i> |  |
| <b>旋转</b> <i>0.0 - 1.0</i> | 沿投影的纹理的正常轴旋转投影的颜色。 |
| <b>缩放</b> <i>0.0 - 1.0</i> | 设置投影纹理的全局比例。 |
| <b>大小</b> <i>0.0 - 2.0</i> | 对投影的纹理执行非均匀缩放。 |
| <b>蒙版</b> |  |
| <b>最大深度</b> <i>0.0 - 1.0</i> | 控制投影纹理显示的深度以及何时将其切断。 |
| <b>深度的渐隐</b> <i>0.0 - 1.0</i> | 设置切断深度突然出现或渐隐的过渡。 |
| <b>正常阈值</b> <i>-1.0 - 1.0</i> | 为未与投影法向完全对齐的曲面设置阈值。 |
| <b>普通渐隐</b> <i>0.0 - 1.0</i> | 为未对齐到突然或渐隐的曲面设置过渡。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-planar-projection.resources/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
