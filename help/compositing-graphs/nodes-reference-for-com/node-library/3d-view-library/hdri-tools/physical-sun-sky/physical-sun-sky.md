---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: 使用“物理SunSky”节点生成物理上精确的太阳和天空光照环境，以进行逼真的材料预览。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物理SunSky
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# 物理太阳/天空

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

基于Hosek-Wikie天空光照模型的物理太阳和天空实现。 为人工HDRI提供了良好的基础。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>太阳位置</b> | 范围= [0,1]x[0,1] （经纬角） |
| <b>混浊度</b> <i>1.0 - 10.0</i> | 浊度范围为1至10 |
| <b>反照率</b> <i>0.0 - 1.0</i> | 反照率范围从0到1。 |
| <b>地面颜色</b> <i>（颜色值）</i> | 地面平面的颜色。 |
| <b>曝光(EV)</b> <i>-1.0 - 4.0</i> | 生成的输出的曝光值。 |
| <b>太阳大小</b> <i>0.0 - 4.0</i> | 太阳的比率，任何与1不同的值在物理上都是不正确的。 值具有微妙的效果！ |
| <b>太阳强度</b> <i>0.0 - 1.0</i> | 太阳光盘的强度。 太阳光盘很小，因此效果不是立即可见。 |
| <b>天空强度</b> <i>0.0 - 1.0</i> | 天空的强度。 还会影响太阳在天空中的闪烁，而不会影响光盘本身。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/sky-ex.gif" />
        </td>
    </tr>
</table>
