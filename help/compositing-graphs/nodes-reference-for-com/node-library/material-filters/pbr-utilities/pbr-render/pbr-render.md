---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: 使用PBR 渲染节点以真实的光照渲染基于物理的材质，从而预览材质外观。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 1%

---


# PBR 渲染

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render.png){width="250px"}

**在：** *材质滤镜/PBR实用工具*

**复杂**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

使用基于图像的光照(IBL)将PBR素材渲染到球体、平面或圆柱体上。这是节点内的渲染引擎，对于生成缩览图、预览或2D资源非常有用。 它不是如3D视图那样进行渲染，而是图形中生成的实际纹理。

此节点要求至少插入一个完整的PBR材料。 理想情况下，可使用“链接创建模式”将材料连接到PBR 渲染。 此外，您还需要一个球面展开的HDRI环境，以便渲染从中计算光照。 可以在PBR Materials下找到用于测试的材质，也可以在库中的[&#x200B; 3D View下找到环境地图。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **CPU (SSE2)引擎**
> 
> PBR 渲染节点非常重，无法与SSE2 CPU引擎配合使用。 如果节点性能极差，则按F9切换到另一个引擎。

## 输入

* **素材通道** **输入**\
  使用多个材质输入在几何图形上渲染材质：
  * 底色
  * 法线
  * 自发光
  * 粗糙度
  * 金属
  * 镜面色阶
  * 高度
  * 环境光遮蔽
  * 不透明度蒙版
  * 各向异性水平
  * 各向异性角度
  * 半透明度
  * 散射距离缩放
* **镜头Dirt映射**： *灰度输入*&#x200B;镜头上Dirt的自定映射，当镜头光晕可见时显示。
* **镜头光圈图**：*灰度输入*&#x200B;可用于覆盖散景散景失焦形状。 对比越明显，它就越明显。 请记住，只对纹理中的一个圆圈进行取样，因此任何形状都必须适合一个圆圈。
* **背景输入**： *颜色输入*\
  将&#x200B;**背景模式**&#x200B;参数设置为&#x200B;*背景输入*&#x200B;时用作背景的自定义映射
* **环境图**： *颜色输入*&#x200B;用于计算光照的环境图。 必须球面映射且在HDR中。

输出

* **美丽**\
  最终渲染
* **原始辐照度**\
  最终渲染的辐照度数据\
  *Alpha：*&#x200B;不透明度映射
* **原始Specular**\
  最终渲染的Specular数据\
  *Alpha：* Specular阴影映射
* **正常世界空间**\
  最终渲染的世界空间法线数据\
  *Alpha：*&#x200B;世界空间Height地图
* **法向切空间**\
  最终渲染的切空间法线数据\
  *Alpha：*&#x200B;正切空间Height映射
* **UV**\
  最终渲染的UV数据\
  *Alpha：*&#x200B;不透明度映射

## 参数

* **形状**： *球体、平面、圆柱体*\
  设置用于渲染的形状。 无法自定义形状。
* **位移强度**： *0.0 - 0.5*&#x200B;设置来自Height的位移强度。
* **环境旋转**： *0.0 - 1.0*\
  旋转光照环境。 与移动相机时相比预旋转。
* **背景模式**：*颜色、环境、环境、背景输入*\
  设置背景中显示的内容。 颜色是纯色，环境是使用可选模糊插入的地图。 “环境”是一种非常模糊的环境。
* **背景颜色**： *（颜色值）*\
  仅在“背景”模式设置为“颜色”时可用。
* **环境背景模糊**： *0.0 - 1.0*\
  仅在“背景”模式设置为“环境”时可用。
* **形状**
  * **缩放**： *0.0 - 2.0*\
    设置球体的比例。
  * **平面大小**： *0.0 - 1.0*\
    设置平面的比例。
  * **圆柱半径**： *0.0 - 1.0*\
    设置圆柱的半径。
  * **圆柱体长度**： *0.0 - 1.0*\
    设置圆柱的长度。
  * **旋转**： *0.0 - 1.0*\
    旋转形状，而不旋转光照。
  * **旋转方向**： *0.0 - 1.0*\
    在2D中设置旋转轴。
  * **围绕方向**&#x200B;旋转： *0.0 - 1.0*\
    在旋转轴上旋转形状。
  * **形状位置**： *-1.0 - 1.0*\
    移动形状。
  * **UV拼贴**： *1.0 - 6.0*\
    设置UV拼贴的量。
  * **球体UV 缩放**： *0.0 - 4.0*\
    设置UV在球面上的比例。
  * **平面UV 缩放**： *1.0 - 4.0*\
    设置UV在平面上的比例。
  * **圆柱体UV 缩放**： *1.0 - 6.0*\
    设置UV在圆柱上的比例。
  * **UV 偏移**： *0.0 - 1.0*\
    偏移UV
  * **倾斜UV**： *False/True*\
    将球体的UV倾斜45度。
* **相机**
  * **曝光**： *-4.0 - 4.0*\
    设置相机曝光。
  * **色调映射器**： *线性，ACES，Filmic Hejl*\
    设置用于最终图像的色调映射解决方案。
  * **相机模式**：*透视，正交*\
    在两个投影模式之间切换相机。
  * **视域**： *0.01 - 100.0*\
    设置相机视场角度。
  * **距离**： *0.0 - 4.0*\
    设置相机到对象中心的距离。
  * **晕影强度**： *0.0 - 1.0*\
    设置晕影效果的强度。
  * **晕影半径**： *0.0 - 1.0*\
    设置晕影效果的半径。
  * **屏幕位置**：\
    围绕对象移动相机，也可以在2D视图中使用线框进行更改。
* **字段深度**
  * **光圈半径** ： *0.0 - 0.1*&#x200B;设置光圈半径。 值越高，离焦区域越模糊（散景）。
  * **光圈刀片**： *3 - 9*\
    设置散景模糊的形状。
  * **光圈圈**： *0.0 - 1.0*\
    向散景形状添加内部渐变。
  * **光圈分布**： *0.0 - 2.0*\
    向散景图添加色差。
  * **旋转散景**： *0.0 - 1.0*\
    向离焦散景模糊区域添加涡旋或旋转类型的效果。
  * **焦点模式**： *自动，点*\
    设置焦点是预先确定的还是用户设置的。 点焦点允许您在2D视图中移动一个点以确定焦距。
  * **焦点**：\
    如果焦点设置为“点”，则可以移动该点。 有一个二维视图小工具。
  * **焦点偏移**： *-0.5 - 0.5*\
    如果焦点设置为“自动”，则允许您来回移动它。
  * **使用自定光圈图**： *False/True*\
    覆盖上面的Aperture设置，并使用Aperture映射输入来确定散景形状。 需要输入。
* **后期效果**
  * **启用Post Effects**： *False/True*\
    在最终渲染中切换&#x200B;*所有*&#x200B;后期效果。
  * **开花强度** ：*0.0 - 2.0*&#x200B;设置开花效果的强度。
  * **开花阈值** ： *0.0 - 2.0*&#x200B;设置开花显示的低阈值。
  * **开花色度偏移** ： *0.0 - 1.0*
  * **镜头光晕强度** ：*0.0 - 1.0*&#x200B;设置镜头光晕效果的强度。
  * **镜头光晕强度** ：*0.0 - 1.0*&#x200B;设置镜头光晕强度。 确保环境背景中的光线处于查看状态，以便正确查看此效果。
  * **镜头Dirt强度** ：*0.0 - 1.0*&#x200B;在镜头光晕上设置镜头Dirt映射的效果。
* **渲染设置**
  * **扩散质量**：*16个样本，32个样本，64个样本，128个样本*\
    在漫射图的品质级别之间切换。
  * **扩散发射多倍数**： *0.0 - 1.0*\
    控制发射部分对辐照度的贡献程度。
  * **漫射阴影强度**： *0.0 - 1.0*\
    控制漫射阴影的强度。
  * **Specular抖动**： *0.0 - 1.0*\
    设置Specular的抖动量。
  * **Specular阴影乘数**： *0.0 - 1.0*\
    控制Specular反射中的阴影强度。
  * **不透明度模式***抖动Alpha测试，简单Alpha混合*\
    控制应用透明度的方法。 *简单Alpha混合*&#x200B;模式在统一背景上最明显。
  * **环境遮蔽强度**： *0.0 - 1.0*\
    设置环境遮蔽阴影的强度。
* **材质调整**
  * **重新计算法线**： *False/True*\
    将根据位移强度从Height映射中重新计算法线。
  * **普通格式**： *DirectX，OpenGL*\
    在不同的法线贴图格式之间切换（反转绿色通道）
  * **电介质F0输入**： *常量值，Specular level输入*\
    设置什么驱动F0值。 Specular level输入表示将由输入映射驱动。
  * **电介质F0**： *0.0 - 0.08*\
    如果为“电介质F0输入”选择了“常量值”，则此滑块允许您设置全局值。
* **透明外套**
  * **启用透明涂层**： *False/True*\
    在输入材料上启用附加的简单透明涂层。
  * **透明外套重量**： *0.0 - 1.0*\
    设置透明涂层图层的强度或强度。
  * **清除外套Specular level**： *0.0 - 1.0*\
    设置透明涂层的粗糙度。
  * **从基底图层继承Normal**： *False/True*&#x200B;如果透明皮忽略或使用来自基础材质的法线，则设置。
* **具发射性**
  * **启用发射光照** *True/False*&#x200B;切换发射光照的扩散作用。
  * **发射强度**： *0.0 - 10.0*\
    设置发射映射的全局乘数。
* **次表面散射**
  * **启用次表面散射** *True/False*\
    在最终渲染中切换子表面散射。\
    *注意：*&#x200B;次表面散射要求&#x200B;**半透明**&#x200B;输入值为大于0.0 *的*
  * **散射距离** *0.0 - 1.0*\
    调整散布效果的最大距离。\
    *注意：*&#x200B;此值与&#x200B;**散射距离刻度**&#x200B;输入值&#x200B;*每个颜色通道*&#x200B;相乘。
  * **红移** *0.0 - 1.0*\
    调整散射中红移效果的强度。
  * **瑞利** *0.0 - 1.0*\
    调整散射中的瑞利效果强度。

## 示例图像

所有图像都是使用[Substance 3D资源](https://substance3d.adobe.com/assets)库中的材质，直接在Designer内部的2D视口中生成的。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/pbr-render-v2.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/sphere-thermal-insulation-panel.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/sphere-ominous-obsidian.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/sphere-forest-gravel-1.jpg" width="300px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_image" src="../../../../../../assets/sphere-chesterfield-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_image" src="../../../../../../assets/sphere-carbon-fiber.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c2_image" src="../../../../../../assets/plane-inclined-lumber-tiles.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c3_image" src="../../../../../../assets/cylinder-medieval-leaded-glass-window.jpg" width="300px"/></div> |
|  |  |  |  |
