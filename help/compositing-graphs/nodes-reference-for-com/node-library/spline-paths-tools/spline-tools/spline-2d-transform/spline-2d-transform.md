---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: 使用“样条2D变换”节点通过平移、旋转和缩放操作来变换样条。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条2D变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# 样条2D变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-2d-transform-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将全局变换应用于所有输入样条，包括反转其方向。

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

<b>翻转方向</b> *布尔值*&#x200B;反转样条线的方向。

<b>转换矩阵</b> *浮点4*&#x200B;应用于样条的变换矩阵。\
有三种编辑矩阵参数的模式可用：\
*— 变换Gizmo*：选择“样条2D变换”节点时，调整2D视图中显示的Gizmo的手柄；\
*— 旋转/拉伸*：单独控制样条的旋转和拉伸。 请注意，这些值始终相对于当前变换应用。 例如，将50%宽度应用两次会产生25%宽度；\
*— 矩阵值*：单击“编辑矩阵值”按钮可直接输入矩阵的原始数值。

<b>偏移</b> *浮动2*&#x200B;将位置偏移应用于X（水平）和Y（垂直）样条。

+++预览
<b>显示方向帮助程序</b> *布尔值*&#x200B;在预览输出中，在样条线的起始处显示一个点，在其结尾处显示一个箭头。

<b>显示Thickness信封</b> *布尔值*\
在样条Thickness的边显示附加线。

<b>段数量</b> *整数*&#x200B;调整用于在预览输出中绘制样条可视化效果的段数。\
值越高，线条越平滑。

<b>Thickness（像素）</b> *浮动*&#x200B;以像素为单位调整样条可视化在预览输出中的Thickness。

+++

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant2-After.jpg" alt="样条2DTransform-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-After.jpg" alt="Spline2DTransform-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/Spline2DTransform-Demo1.gif "节点示例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
