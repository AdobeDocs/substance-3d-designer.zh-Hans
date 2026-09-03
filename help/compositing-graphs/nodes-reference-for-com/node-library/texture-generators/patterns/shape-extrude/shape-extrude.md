---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: 使用“形状凸出”节点在Substance 3D Designer纹理中凸出形状并创建类似3D的深度效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状凸出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# 形状凸出

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude-01.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

一个高级节点，允许将2d二进制“形状”输入渲染为3D旋转的高图。 其工作方式与3D包中的凸出类似，沿其轴凸出形状，从而创建体积块。 结合使用轮廓渐变蒙版，还可以创建旋转/车床类型主体。 对于为高地图创建复杂的人工形状非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>凸出形状输入</b> <i>灰度输入</i> | 如果“Extrude Shape”（凸出形状）设置为“Custom”（自定），请在这里插入您自己的（最好是）“Binary Shape”（二进制形状）蒙版 |
| <b>配置文件渐变</b> <i>灰度输入</i> | 如果“截面梁类型”设置为“垂直渐变”，则可用于为旋转主体定义形状沿轴的比例。 |
| <b>个人资料蒙版</b> <i>灰度输入</i> | 用于沿凸出形状的轴隐藏或显示凸出形状的蒙版槽。 可用于中断形状沿其轴的连续性。 仅解释为二进制：灰度put值四舍五入为0或1。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>凸出Height</b> <i>0.0 - 1.0</i> | 从中心向上拉伸形状的量。 |
| <b>凸出深度</b> <i>0.0 - 1.0</i> | 从中心向下拖动形状的数量。 |
| <b>凸出形状</b> <i>多维数据集，圆柱体，自定义输入</i> | 使用内置形状或在外部输入您自己的自定形状。 |
| <b>凸出形状大小</b> <i>0.0 - 1.0</i> | 仅用于内置立方体和圆柱体，确定基本形状大小，可以缩放为非均匀形状。 |
| <b>缩放</b> <i>0.0 - 1.0</i> | 设置效果的全局比例。 对于内置形状，这是统一的基本形状缩放，不会影响Height或深度。<br><br>对于自定义输入，这将以统一的方式缩放整个最终结果。 |
| <b>配置文件类型</b> <i>直线，垂直渐变，蒙版</i> | 用于确定效果行为和可选额外输入图使用情况的主控件。<br><br>垂直渐变是标准的凸出行为，垂直渐变允许沿整个轴自定义缩放值，蒙版允许通过蒙版隐藏沿轴的部分。 |
| <b>斜角Height</b> <i>0.0 - 1.0</i> | 设置斜角沿拉伸轴到达的距离。 |
| <b>斜面强度</b> <i>0.0 - 1.0</i> | 设置斜角从原始形状中收缩的数量。 |
| <b>斜角曲线</b> <i>-1.0 - 1.0</i> | 设置斜角效果的凸曲线或凹曲线。 值为0表示直线，无曲线。 |
| <b>镜像斜面</b> <i>False/True</i> | 切换以在形状的顶部和底部应用斜角。 |
| <b>缩减多倍数</b> <i>0 - 2</i> | 内置的易于缩减的控制功能。 可用于快速添加消除锯齿功能；请确保也提高节点分辨率。 |
| <b>位置</b> | 旋转的主控件导致3D空间。 与2D 视图中的intervatice Gizmo相关。 |
| <b>输出范围</b> <i>[0, 1], [-1, 1]</i> | 设置输出最小值和最大值。 如果range设置为[-1,1]，则负值显示为黑色。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-02.png" />
        </td>
    </tr>
</table>
