---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: 使用样条渲染节点将样条渲染为具有可自定义宽度、颜色和混合模式的纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---


# 样条渲染

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-render-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在输入<b>Background</b>上沿输入<b>样条</b>绘制段字符串。

</td>
</tr>
</table>

## 输入连接器

<b>背景&#x200B;</b>*灰度*&#x200B;应在其上绘制样条的灰度图像。

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

<b>输出</b> *灰度*\
在背景上绘制输入样条的结果图像。

## 参数

<b>模式</b> *整数*&#x200B;选择应绘制的样条的方法：
* *绘制样条列表*：绘制输入列表中的所有样条；
* *绘制单样条*：仅从输入列表中绘制指定的样条；
* *绘制样条范围*：仅从输入列表中绘制指定范围内的样条。

<b>绘制样条索引</b> *整数* （当“模式”设置为“绘制单样条”时可用）应绘制的样条的索引。

<b>绘制样条范围</b> *Integer2* （当“模式”设置为“绘制样条范围”时可用）应绘制的样条索引范围。

<b>显示方向帮助程序</b> *布尔值*&#x200B;对于每个样条，在样条的开始处绘制一个点，在结束处绘制一个箭头。

<b>段数量</b> *整数*&#x200B;调整沿样条绘制的段数。\
值越高，线条越平滑。

<b>包络样条量</b> *整数*\
应沿每个样条的Thickness绘制的重复段数。

<b>开始</b> *浮动*&#x200B;偏移应绘制的样条部分的起点。\
该值表示样条的规范化长度。

<b>结束</b> *浮动*&#x200B;偏移应绘制的样条部分的端点。\
该值表示样条的规范化长度。

<b>Thickness大小模式</b> *整数*&#x200B;计算绘制段Thickness的方法：
* *图像*：在纹理空间中规范化该值，其中1是图像的全宽。 Thickness与纹理分辨率有关；
* *像素*：该值是纹理中的绝对像素数，其中1是整像素。 Thickness与纹理分辨率是分开的。

<b>Thickness（图像）</b> *浮点*（在“Thickness大小模式”设置为“图像”时可用）在纹理空间中标准化的绘制段的Thickness，其中1是图像的全宽。

<b>Thickness（像素）</b> *浮动*（在“Thickness大小模式”设置为“像素”时可用）绘制段的Thickness作为纹理中的绝对像素数，其中1是整像素。

<b>启用接头</b> *布尔值*&#x200B;使用磁盘填充沿样条绘制的单个段之间的间隙。

<b>非方形校正&#x200B;</b>*布尔值*&#x200B;调整点的位置和Thickness以保持样条形状的非方形分辨率。\
这也会影响均匀分布。

+++颜色
<b>背景强度</b> *浮点*&#x200B;该值乘以背景输入图像。

<b>样条样式</b> *整数*&#x200B;用于为样条着色的方法：
* *纯色*：使用一致的灰度值绘制线段；
* *渐变*：沿每个线段字符串从头到尾应用从黑色到白色的渐变；
* *Height*：样条的Height用作绘制线段的灰度值。

<b>样条颜色</b> *浮动*&#x200B;用于绘制线段的统一灰度值。\
选择“纯色”以外的“样条样式”时，此颜色会与样式的颜色相乘。

<b>随机明亮度</b> *浮点*&#x200B;对于样条中每个未剪切段的字符串，将指定范围内的随机偏移应用于用于绘制该字符串的灰度值。

<b>混合模式</b> *整数*&#x200B;混合背景颜色和沿样条绘制的重叠段颜色的方法：
* *最大*：使用最亮的值；
* *相加*：值相加。

+++

+++随机区段
<b>随机段开始</b> *浮动*&#x200B;调整段字符串离样条起始点更近的被剪切的概率。

<b>随机段结束</b> *浮动*&#x200B;调整段字符串靠近样条端点的被剪切的概率。

<b>随机偏移</b> *浮动*&#x200B;设置沿每个剪切段的法线应用的最大位移量。\
当“起始”和“结束”均设置为0时，此参数不起作用。

<b>随机偏移中心</b> *浮动*&#x200B;沿每个剪切段的法线偏移应用于每个剪切段的随机位移的中心。

+++

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
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

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/SplineRender-Demo.gif "节点示例1")

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
