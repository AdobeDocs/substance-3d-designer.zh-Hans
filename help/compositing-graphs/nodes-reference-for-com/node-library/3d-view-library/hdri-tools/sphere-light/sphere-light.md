---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: 使用“球面光”节点将球面光源添加到HDRI环境中，以增强光照控制。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 球面光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# 球面光

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](sphere-light.resources/panorama-sphere-light.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成一个球面投影的球面形状。 球体变换由变换小工具驱动。

球面光具有非常广泛的用途，并且有多种选项，不仅可生成简单的圆形光，还可生成行星或其他天体。 如果您不需要更高级的光照和旋转选项，请改为查看[形状光照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>背景图像输入</b> <i>颜色输入</i> | 合成所生成光的可选背景。 |
| <b>形状图像输入</b> <i>颜色输入</i> | 要映射到球面光的可选图像。 仅在“形状颜色模式”设置为“图像输入”时使用。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>位置模式</b> <i>距原点距离，世界位置</i> | 选择两种放置模式。 距原点距离类似于极坐标，球体相对于全景图的中心设置，世界位置类似于标准的三维坐标。 |
| <b>位置坐标</b> |  |
| <b>向上矢量</b> <i>Z向上，Y向上</i> | 仅在“世界位置”模式下确定坐标系的方向。 |
| <b>球面世界位置</b> <i>-2.0 - 2.0</i> | 仅在“世界位置”模式下，在世界空间中设置球体位置。 |
| <b>位置</b> | 仅适用于距原点距离模式。 设置相对于中心的位置。 可在2D视图中操作。 |
| <b>距原点距离</b> <i>0.0 - 20.0</i> | 仅适用于距原点距离模式。 设置到原点的距离，影响球体的可见大小。 |
| <b>形状颜色模式</b> <i>RGB、温度（开氏温度）、图像输入</i> | 选择用来设置形状颜色的方法。 “Image Input（图像输入）”允许使用第二个输入插槽。 |
| <b>颜色</b> <i>（颜色值）</i> | 仅当“形状颜色模式”设置为“RGB”时。 为形状选取颜色。 |
| <b>形状温度</b> <i>800.0 - 20000.0</i> | 仅在“形状颜色模式”设置为“色温”时。 设置形状颜色的开氏值。 |
| <b>球面图像输入灰度系数</b> <i>sRGB，线性</i> | 仅当“形状颜色模式”设置为“图像输入”时。 确定如何解释形状图像输入。 |
| <b>球面旋转</b> <i>0.0 - 1.0</i> | 仅当“形状颜色模式”设置为“图像输入”时。 围绕中心旋转球体，以定位所映射的图像。 |
| <b>曝光(EV)</b> <i>0.0 - 10.0</i> | 为生成的形状设置曝光值，使其与背景图像曝光值完美匹配。 |
| <b>球面半径</b> <i>0.0 - 1.0</i> | 设置球体的半径/大小。 |
| <b>球体硬度</b> <i>0.0 - 1.0</i> | 设置球体的硬度/衰减。 |
| <b>着色</b> <i>无，肢体变暗，着色光</i> | 设置是否应将着色应用于球体。 允许球体不显示为实心、未照亮的对象。 肢体变暗意味着边缘略微变暗，着色光意味着球体由可选的着色光照亮。 |
| <b>着色光源世界位置</b> <i>-1.0 - 1.0</i> | 如果“着色”设置为“着色光”，则此处控制光在球体上的位置。 |
| <b>Penombra透明度</b> <i>0.0 - 1.0</i> | 如果“着色”设置为“着色光”，则控制着色的衰减。 |
| <b>启用后台输入</b> <i>False/True</i> | 切换可选背景图像的使用。 复合图像在背景之上生成了光照。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 如果未使用背景输入，请在此处设置纯色背景值。 |
| <b>背景灰度系数</b> <i>sRGB，线性</i> | 如果使用“背景输入”，请设置如何解释背景输入。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/spherelight-ex1.png" />
        </td>
    </tr>
</table>
