---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: 使用“样条圆”节点创建用于生成圆形图案和形状的圆形样条。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条圆
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# 样条圆

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-circle-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成一个圆形的单个样条。

</td>
</tr>
</table>

## 输入连接器

<b>预览</b> *灰度*&#x200B;作为灰度图像的输入样条的预览。

<b>样条坐标</b> *颜色*&#x200B;在彩色图像的RGBA通道中编码的输入样条点的坐标：\
<b> R</b> - X位置\
<b> G</b> - Y位置\
<b> B</b> -Height\
    <b>A</b> — 打包的数据：\
        *符号：样条是封闭的（负）或开放的（正）；\
        *绝对值：Thickness+ 1。

<b>样条数据</b> *颜色*&#x200B;编码在彩色图像的RGBA通道中的输入样条的其他数据。\
<b> R</b> — 切线X\
<b> G</b> — 切线Y\
<b> B</b> — 未使用\
<b> A</b> — 未使用

<b>样条量</b> *整数*&#x200B;输入样条的数量。

## 输出连接器

<b>预览</b> *灰度*&#x200B;输出样条作为灰度图像的预览。

<b>样条坐标</b> *颜色*&#x200B;以彩色图像的RGBA通道编码的输出样条点的坐标。\
    <b>R</b> - X位置\
    <b>G</b> - Y位置\
    <b>B</b> -Height\
    <b>A</b> — 打包的数据：\
        *符号：样条是封闭的（负）或开放的（正）；\
        *绝对值：Thickness+ 1。

<b>样条数据</b> *颜色*&#x200B;以彩色图像的RGBA通道编码的输出样条的附加数据。\
    <b>R</b> — 切线X\
    <b>G</b> — 切线Y\
    <b>B</b> — 未使用\
    <b>A</b> — 未使用

<b>样条量</b> *整数*&#x200B;输出样条的数量。

## 参数

<b>圆形半径</b> *浮动*\
调整纹理空间中的圆的半径。

<b>圆形预旋转</b> *浮动*\
在应用“大小”之前，将旋转应用于基准圆。

<b>圆形大小</b> *浮点2*\
调整圆的水平大小(X)和垂直大小(Y)。

<b>圆形旋转后</b> *浮动*\
应用“大小”后，对基圆应用旋转。

<b>圆形位置</b> *浮点2*\
设置纹理空间中圆心的位置。

<b>启动Thickness</b> *浮动*&#x200B;调整圆圈起点的Thickness。\
此Thickness沿样条插入到“终止”Thickness。\
注意：Thickness由特定的“样条”节点使用。

<b>结束Thickness</b> *浮动*&#x200B;调整圆圈端点的Thickness。\
此Thickness沿样条插入到“起始”Thickness。\
注意：Thickness由特定的“样条”节点使用。

<b>启动Height</b> *浮动*&#x200B;调整圆起点的Height，其中较低的值表示较低或较深的位置。\
此Height沿样条插入到“终止”Height。

<b>结束Height</b> *浮动*&#x200B;调整圆端点的Height，其中较低的值表示较低或较深的位置。\
此Height从“起始”Height沿样条插值。

<b>剪辑</b> *浮点2*&#x200B;沿圆偏移样条的起点和终点。\
这些值已规范化。

<b>螺旋线</b> *浮动*&#x200B;将圆圈的起始点从其半径移动到其中心。\
然后沿样条插入从中心到样条端点的距离。\
该值已规范化。

<b>螺旋形转折</b> *浮动*&#x200B;定义螺旋线围绕其中心旋转的圈数。

<b>螺旋电源</b> *浮动*&#x200B;将幂曲线应用于距绘制螺旋线时所用中心的距离。\
大于1的值意味着螺旋线的更大部分仍然靠近中心。

<b>翻转方向</b> *布尔值*\
反转样条方向。

<b>均匀分布</b> *布尔值*\
为True时，样条点的间距从起点到终点均匀。

<b>追加输入样条</b> *布尔值*\
将生成的样条添加到连接到<b>样条</b>输入的样条列表的末尾。

<b>非方形校正&#x200B;</b>*布尔值*&#x200B;调整点的位置和Thickness以保持样条形状的非方形分辨率。\
这也会影响均匀分布。

+++预览
<b>显示方向帮助程序</b> *布尔值*&#x200B;在预览输出中，在样条线的起始处显示一个点，在其结尾处显示一个箭头。

<b>显示Thickness信封</b> *布尔值*\
在样条Thickness的边显示附加线。

<b>段数量</b> *整数*&#x200B;调整用于在预览输出中绘制样条可视化效果的段数。\
值越高，线条越平滑。

<b>Thickness（像素）</b> *浮动*&#x200B;在预览输出中调整样条可视化的Thickness（以像素为单位）。

+++

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/SplineCircle-Variant1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/SplineCircle-Demo.gif "节点示例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![示例3](../../../../../../assets/SplineCircle-Variant2.jpg "示例3")

</td>
<td style="border: 0;" valign="top">

![示例4](../../../../../../assets/SplineCircle-Variant3.jpg "示例4")

</td>
</tr>
</table>
