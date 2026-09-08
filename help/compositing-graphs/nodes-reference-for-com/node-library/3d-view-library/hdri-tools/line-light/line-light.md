---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: 使用线光源节点在HDRI环境中创建线性光源，以模拟荧光灯和条形光照。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 线光源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# 线光源

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-line-light.png){width="200px"}

## 线光源

**位置：** *3D视图/HDRI 工具*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

基于空间中的两个点的坐标生成球面投影的线形。 与[形状光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md)相比，它有更多的选项用于调整形状方向以及将重复图案应用于光形。

该节点的定位模式比其他HDRI光节点稍微复杂一些。 建议尝试几种不同的大小模式，以找到适合您的场景。

## 输入

* **背景图像输入**： *颜色输入*\
  合成所生成光的可选背景。
* **形状图像输入**： *颜色输入*\
  要映射到线光源的可选图像。 仅在“形状颜色模式”设置为“图像输入”时使用。
* **图案图像输入**： *灰度输入*\
  自定义图案图像，在“Pattern”参数设置为“Image Input”时使用。

## 参数

* **位置模式**：*地面/天花板、距原点距离、世界位置*\
  从三种不同的放置模式中进行选择。 地面/天花板和距原点距离支持在2D视图中操作，“世界”位置只能通过属性更改，但支持更精确的放置。
* **显示地网格**： *False/True*\
  用于允许绘制调试地网格的帮助器函数。 帮助估计线段在空间中的位置。
* **位置坐标**
  * **向上矢量**： *Z向上，Y向上*\
    仅在“世界位置”模式下确定坐标系的方向。
  * **点1UV位置**：\
    仅适用于地面/天花板和距原点距离。 设置UV空间中的第一个点位置。
  * **点2UV位置**：\
    仅适用于地面/天花板和距原点距离。 在UV空间中设置第二个点位置。
  * **点1世界位置**： *-2.0 - 2.0*\
    仅适用于世界位置模式。 设置世界空间中的第一个点。 不支持2D视图交互。
  * **点2世界位置**： *-2.0 - 2.0*\
    仅适用于世界位置模式。 设置第二个世界空间点。 不支持2D视图交互。
  * **行绝对Height**： *0.0 - 1.0*\
    仅在“地面/天花板位置模式”下，设置距天花板的绝对Height。 使用“显示地面网格”可以更好地估计位置。
  * **距原点距离**： *0.0 - 1.0*\
    仅适用于距原点距离位置模式。 设置两个点到全景图中心的距离。
* **形状颜色模式**：*RGB、色温（开氏温度）、图像输入*\
  选择用来设置形状颜色的方法。 “Image Input（图像输入）”允许使用第二个输入插槽。
* **颜色**： *（颜色值）*\
  仅当“形状颜色模式”设置为“RGB”时。 为形状选取颜色。
* **温度**： *800.0 - 20000.0*\
  仅在“形状颜色模式”设置为“色温”时。 设置形状颜色的开氏值。
* **形状图像UV模式**： *伸缩，仅伸缩，重复+间距*\
  仅当“形状颜色模式”设置为“图像输入”时。 设置图像应用于线形的方式，确定UV重复行为。
* **形状图像重复间距**： *0.0 - 1.0*\
  仅当“形状颜色模式”设置为“图像输入”并且UV模式设置为“重复+间距”时。 设置图像沿线条重复时的间距量。
* **形状图像灰度系数**： *sRGB，线性*\
  仅当“形状颜色模式”设置为“图像输入”时。 确定如何解释形状图像输入。
* **曝光(EV)**： *0.0 - 10.0*\
  为生成的形状设置曝光值，使其与背景图像曝光值完美匹配。
* **直线旋转**： *0.0 - 1.0*\
  沿直线长度的轴旋转直线。 旋转时，线条被视为平板。
* **行Thickness**： *0.0 - 1.0*\
  设置线路卡的Thickness。
* **图案**：*平滑方形、锐方形、锥形、半球、图像输入*\
  选择要使用的图案形状。
* **图案硬度**： *0.0 - 1.0*\
  设置图案的硬度/对比度。
* **图案UV模式**： *拉伸、仅中间拉伸、重复+间距*\
  设置如何使用应用于形状图像顶部的辅助图案蒙版。
* **图案重复间距**： *0.0 - 1.0*\
  仅当图案UV模式设置为“重复+间距”时。 设置重复图案之间的间距量。
* **启用地面剪切**： *False/True*\
  启用线段绘制的剪切。 使用地面/天花板放置模式时效果不可见。
* **Height**： *-2.0 - 0.0*\
  设置用于裁剪的倒圆角平面的相对Height。 影响绘制的地面网格。
* **启用后台输入**： *False/True*\
  切换可选背景图像的使用。 复合图像在背景之上生成了光照。
* **背景颜色**： *（颜色值）*\
  如果未使用背景输入，请在此处设置纯色背景值。
* **背景灰度系数**： *sRGB，线性*&#x200B;如果使用背景输入，请设置如何解释背景输入。

## 示例图像

![](../../../../../../assets/line-light-ex.gif)

</td>
</tr>
</table>
