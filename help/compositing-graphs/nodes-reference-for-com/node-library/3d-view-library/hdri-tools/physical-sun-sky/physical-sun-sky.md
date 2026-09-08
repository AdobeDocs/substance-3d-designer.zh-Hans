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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# 物理太阳/天空

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## 物理太阳/天空

**位置：** *3D视图/HDRI 工具*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

基于Hosek-Wikie天空光照模型的物理太阳和天空实现。 为人工HDRI提供了良好的基础。

## 参数

* **太阳位置**：\
  范围= [0,1]x[0,1] （经纬角）
* **混浊度**： *1.0 - 10.0*\
  浊度范围为1至10
* **反照率**： *0.0 - 1.0*\
  反照率范围从0到1。
* **地面颜色**： *（颜色值）*\
  地面平面的颜色。
* **曝光(EV)**： *-1.0 - 4.0*\
  生成的输出的曝光值。
* **太阳大小**： *0.0 - 4.0*\
  太阳的比率，任何与1不同的值在物理上都是不正确的。 值具有微妙的效果！
* **太阳强度**： *0.0 - 1.0*\
  太阳光盘的强度。 太阳光盘很小，因此效果不是立即可见。
* **天空强度**：*0.0 - 1.0*&#x200B;天空强度。 还会影响太阳在天空中的闪烁，而不会影响光盘本身。

## 示例图像

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
