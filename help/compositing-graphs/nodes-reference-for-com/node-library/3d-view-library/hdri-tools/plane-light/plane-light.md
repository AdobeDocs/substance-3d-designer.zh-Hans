---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: 使用“平面光”节点将平面光源添加到HDRI环境中，以进行定向光照控制。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 平面光
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# 平面光

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成球面投影的平面形状。 可使用输入参数在3D中放置和定向平面。

与简单的[形状光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md)的区别在于，在简单的距原点距离投影之外，它具有更高级的放置选项，并可应用更多图案和蒙版，类似于[线光](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>背景图像输入</b> <i>颜色输入</i> | 合成所生成光的可选背景。 |
| <b>形状图像输入</b> <i>颜色输入</i> | 要映射到线光源的可选图像。 仅在“形状颜色模式”设置为“图像输入”时使用。 |
| <b>图案图像输入</b> <i>灰度输入</i> | 自定义图案图像，在“Pattern”参数设置为“Image Input”时使用。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>位置模式</b> <i>地面/上限、距原点距离、世界位置</i> | 从三种不同的放置模式中进行选择。 地面/天花板和距原点距离支持在2D视图中操作，“世界”位置只能通过属性更改，但支持更精确的放置。 |
| <b>显示网格</b> <i>False/True</i> | 用于允许绘制调试地网格的帮助器函数。 帮助估计线段在空间中的位置。 |
| <b>位置坐标</b> |  |
| <b>向上矢量</b> <i>Z向上，Y向上</i> | 仅在“世界位置”模式下确定坐标系的方向。 |
| <b>平面UV位置</b> | 仅用于地面/上限和距原点距离。 在UV空间中设置平面位置。 |
| <b>平面世界位置</b> <i>-2.0 - 2.0</i> | 仅适用于世界位置模式。 设置平面位置世界空间。 不支持2D 视图交互。 |
| <b>平面绝对Height</b> <i>0.0 - 1.0</i> | 仅在“地面/天花板位置模式”下，设置距天花板的绝对Height。 使用“显示网格”可以更好地估计位置。 |
| <b>距原点距离</b> <i>0.0 - 1.0</i> | 仅适用于距原点距离位置模式。 设置两个点到全景图中心的距离。 |
| <b>形状颜色模式</b> <i>RGB、温度（开氏温度）、图像输入</i> | 选择用来设置形状颜色的方法。 “Image Input（图像输入）”允许使用第二个输入插槽。 |
| <b>颜色</b> <i>（颜色值）</i> | 仅当“形状颜色模式”设置为“RGB”时。 为形状选取颜色。 |
| <b>温度</b> <i>800.0 - 20000.0</i> | 仅在“形状颜色模式”设置为“色温”时。 设置形状颜色的开氏值。 |
| <b>形状图像UV模式</b> <i>拉伸，仅中间拉伸，重复+间距</i> | 仅当“形状颜色模式”设置为“图像输入”时。 设置图像应用于线形的方式，确定UV重复行为。 |
| <b>形状图像重复间距</b> <i>0.0 - 1.0</i> | 仅当“形状颜色模式”设置为“图像输入”并且UV模式设置为“重复+间距”时。 设置图像沿线条重复时的间距量。 |
| <b>形状图像灰度系数</b> <i>sRGB，线性</i> | 仅当“形状颜色模式”设置为“图像输入”时。 确定如何解释形状图像输入。 |
| <b>曝光(EV)</b> <i>0.0 - 10.0</i> | 为生成的形状设置曝光值，使其与背景图像曝光值完美匹配。 |
| <b>平面缩放</b> <i>0.0 - 1.0</i> | 设置平面形状的均匀缩放。 |
| <b>平面大小</b> <i>0.0 - 1.0</i> | 设置平面形状的非均匀大小。 |
| <b>平面旋转</b> <i>0.0 - 1.0</i> | 沿其中心轴旋转平面。 |
| <b>图案</b> <i>平滑方形，锐方形，锥形，半球，图像输入</i> | 选择要使用的图案形状。 |
| <b>图案硬度</b> <i>0.0 - 1.0</i> | 设置图案的硬度/对比度。 |
| <b>图案UV模式</b> <i>拉伸，仅中间拉伸</i> | 设置如何使用应用于形状图像顶部的辅助图案蒙版。 |
| <b>启用地面剪切</b> <i>False/True</i> | 如果平面可以被地平面剪切，或者低于地平面时仍然显示，则启用此选项。 使用“显示地面网格”可更好地估算这一点。 |
| <b>Height</b> <i>-2.0 - 0.0</i> | 调整地面Height以进行剪切。 |
| <b>启用后台输入</b> <i>False/True</i> | 切换可选背景图像的使用。 复合图像在背景之上生成了光照。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 如果未使用背景输入，请在此处设置纯色背景值。 |
| <b>背景灰度系数</b> <i>sRGB，线性</i> | 如果使用“背景输入”，请设置如何解释背景输入。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/plane-light-ex.gif" />
        </td>
    </tr>
</table>
