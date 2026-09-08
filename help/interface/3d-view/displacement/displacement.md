---
helpx_url: ""
breadcrumb-title: ''
description: 使用位移弹出窗口可快速调整应用于3D场景网格的位移和镶嵌。
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D视图 — 位移弹出窗口
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# 位移弹出窗口

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>“3D位移”工具栏中的视图弹出窗口提供了对网格位移和镶嵌的直接控制。</p>
            <p>有三个参数：<ul>
                <li>高度比例</li>
                <li>高度级别</li>
                <li>曲面细分</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="3D视图中的位移弹出窗口" />
        </td>
    </tr>
</table>

## 高度比例

网格顶点沿其法线的最大位移距离（以场景单位表示）。<br>
这是在Height地图中行进的距离，值为1.0。

当Substance图形连接到素材并且该图形包括带有以下项的[输出节点](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)
<code>heightScale</code> 用法，则弹出窗口中的Height缩放参数对于该素材&#x200B;*禁用*
因为它目前由图表驱动。

>[!TIP]
> 
>使用[Height到正常世界单位](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md)节点，并且其“Height深度”参数与“Height比例”值匹配
>确保使用位移时正确进行着色。

## 高度级别

Height映射中用作位移Height *中点*的灰度值。
即用作0.0海拔的阈值。

低于该阈值的值导致顶点向后移位，而高于阈值的值导致
顶点被向前移位。

## 曲面细分

镶嵌涉及通过在各个网格面的段上添加顶点然后连接来细分各个网格面
所有顶点到其中心的新顶点，使1个面变为&#x200B;**6**。

参数定义应递归细分面的次数。

镶嵌参数的&#x200B;*作用域*&#x200B;随当前使用的&#x200B;*渲染器*而变化：可以应用它
每个网格或每个材质。

### 每个网格

使用[光栅器](../3d-renderers/3d-renderers.md#rasterizer)或[GPU 路径追踪](../3d-renderers/3d-renderers.md#gpu-pathtracer)渲染器时，场景中的每个网格对象都有一个&#x200B;*单独的对象*
细分值。

细分是基于上下文的：优化方式使它仅具有&#x200B;*非均匀Height值*或
将细分*非平坦Height映射*，而不考虑参数值。

### 每种材质

使用[OpenGL](../3d-renderers/3d-renderers.md#opengl)渲染器时，场景中的每个素材都有一个&#x200B;*单独的*细分值，该值包括
应用于*使用该素材的所有表面*。

细分不是上下文的：曲面被细分指定的次数，而不管其当前值如何
Height值或纹理。

## 可视化镶嵌

您可以通过检查网格的&#x200B;**线框**&#x200B;来可视化网格化结果。<br>
显示每个渲染器线框的步骤说明如下：

### 光栅器/GPU 路径追踪

使用 <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **渲染器设置**
 按钮，然后在“Properties”（属性）停靠区中，转到&#x200B;**“Render settings”（渲染设置）>“Diagnostic mode”（诊断模式）**，然后选择&#x200B;**线框
 （世界空间）**&#x200B;选项。

### OpenGL

使用 <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **线框**
 按钮。
