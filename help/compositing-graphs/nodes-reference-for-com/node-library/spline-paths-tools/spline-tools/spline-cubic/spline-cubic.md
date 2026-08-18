---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: 使用“样条三次”节点为曲线路径创建具有四个控制点的平滑三次样条。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条（三次）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# 样条（三次）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-cubic-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在任意位置生成两点<b>p1 </b>和<b>p2</b>之间的单个样条。

样条线的轨迹由<b>p1</b>的“出”切线和<b>p2</b>的“入”切线控制。

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

<b>翻转方向</b> *布尔值*\
反转样条方向。

<b>追加输入样条</b> *布尔值*\
将生成的样条添加到连接到<b>样条</b>输入的样条列表的末尾。

<b>非方形校正&#x200B;</b>*布尔值*&#x200B;调整点的位置和Thickness以保持样条形状的非方形分辨率。\
这也会影响均匀分布。

+++高度
<b>启动Height</b> *浮动*&#x200B;调整p1点的Height，其中较低的值表示较低或较深的位置。\
这会影响p1处的样条的Height。

<b>结束Height</b> *浮动*&#x200B;调整p2点的Height，其中较低的值表示较低或较深的位置。\
这会影响p2处的样条的Thickness。

<b>自动切线Height</b> *布尔值*&#x200B;自动设置样条切线的Height，以从“开始”Height线性插值到“结束”Height。

<b>p1正切Height</b> *浮动*（当“自动正切Height”为True时可用）\
调整p1点“out”切线的Height，其中较低的值表示较低或较深的位置。\
当样条从p1逐渐变淡时，这会影响样条的Height。

<b>p2正切Height</b> *浮动*（当“自动正切Height”为True时可用）\
调整p2点“in”切线的Height，其中较低的值表示较低或较深的位置。\
当样条从p2逐渐变淡时，这会影响样条的Height。

+++

+++粗细
<b>启动Thickness</b> *浮动*&#x200B;调整p1点的Thickness。\
这会影响p1处的样条的Thickness。\
注意：Thickness由特定的“样条”节点使用。

<b>结束Thickness</b> *浮动*&#x200B;调整p2点的Thickness。\
这会影响p2处的样条的Thickness。\
注意：Thickness由特定的“样条”节点使用。

<b>自动切线Thickness</b> *布尔值*&#x200B;自动设置样条切线的Thickness，以从“开始”Thickness线性插值到“结束”Thickness。\
注意：Thickness由特定的“样条”节点使用。

<b>p1正切Thickness</b> *浮动*（当“自动正切Thickness”为True时可用）\
调整p1点“出”切线的Thickness。\
当样条从p1逐渐变淡时，这会影响样条的Thickness。\
注意：Thickness由特定的“样条”节点使用。

<b>p2正切Thickness</b> *浮动*（当“自动正切Thickness”为True时可用）\
调整p2点“in”切线的Thickness。\
当样条从p2逐渐变淡时，这会影响样条的Thickness。\
注意：Thickness由特定的“样条”节点使用。

+++

+++点坐标
<b>p1</b> *Float2*&#x200B;设置纹理空间中p1点的位置。

<b>p1正切</b> *Float2*&#x200B;设置纹理空间中p1点“out”切线手柄的位置。

<b>p2</b> *Float2*&#x200B;设置纹理空间中p2点的位置。

<b>p2正切</b> *Float2*&#x200B;设置纹理空间中p2点“in”切线手柄的位置。

+++

+++预览
<b>显示切线</b> *布尔值*&#x200B;在“预览”输出中显示p1点“out”正切和p2点“in”正切。

<b>显示方向帮助程序</b> *布尔值*&#x200B;在预览输出中，在样条线的起始处显示一个点，在其结尾处显示一个箭头。

<b>段数量</b> *整数*&#x200B;调整用于在预览输出中绘制样条可视化效果的段数。\
值越高，线条越平滑。

<b>Thickness（像素）</b> *浮动*&#x200B;在预览输出中调整样条可视化的Thickness（以像素为单位）。

+++

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/SplineCubic-Variant1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/SplineCubic-Variant2.jpg "节点示例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例3](../../../../../../assets/SplineCubic-Demo.gif "节点示例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
