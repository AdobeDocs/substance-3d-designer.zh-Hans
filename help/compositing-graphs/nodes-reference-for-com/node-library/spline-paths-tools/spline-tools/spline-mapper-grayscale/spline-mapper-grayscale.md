---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: 使用“样条映射器灰度”节点沿带有可自定义参数的样条路径映射灰度纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条映射器灰度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---


# 样条映射器灰度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-mapper-grayscale-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将输入灰度图像映射到沿输入样条拉伸的原始形状上。

原始形状可以是平面、半圆柱或圆柱体。 圆柱体可以沿着样条线扭转，从而相应地使映射的图像变形。

</td>
</tr>
</table>

所述节点输出所述映射图像作为灰度图像，以及诸如Height、UV（即图像坐标）和用于独立地选择每个映射样条的ID蒙版的其他信息。

>[!IMPORTANT]
>
> 当使用极低的Thickness值时，结果可能包括样条包络外的不期望伪像。 这是一个已知问题。

>[!NOTE]
>
> 另请参阅[样条映射器颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md)。

## 输入连接器

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

<b>彩图</b> *灰度*&#x200B;应沿输入样条映射的输入灰度图像。

<b>Height映射</b> *灰度*&#x200B;应沿输入样条映射的输入灰度Height映射。

<b>Twist Curve</b> *灰度*&#x200B;使用第一行像素的值描述曲线的图像。\
当<b>形状</b>参数设置为&#x200B;*半圆柱体*&#x200B;或&#x200B;*圆柱体*&#x200B;时，此输入用于控制形状周围的UV扭曲。 用<b>扭转UVs曲线乘数</b>参数控制其影响。\
曲线提供沿样条旋转量的轮廓，行中的第一个像素是样条起始处的旋转，最后一个像素是终止处的旋转。 灰度值表示若干转弯。\
您可以使用[曲线](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)节点来创作曲线。

## 输出连接器

<b>颜色</b> *灰度*&#x200B;将输入彩色图像映射为输入样条作为灰度图像的结果。

<b>Height</b> *灰度*&#x200B;将输入Height图像映射为输入样条作为灰度图像的结果。

<b>UV</b> *颜色*&#x200B;跨输入样条映射的UV（即坐标），在彩色图像中编码。

<b>ID</b> *灰度*&#x200B;沿输入样条映射的图像蒙版，其中白色值从一个样条向下一个样条递增1，以便可以独立选择每个形状。

## 参数

<b>段数量</b> *整数*&#x200B;样条在图像坐标遍历之前被简化为段。\
段数量越多，沿曲线映射就越平滑。

<b>自动缩放UV</b> *布尔值*&#x200B;自动调整坐标的比例，以便在沿样条映射正方形图像时保留该图像。<b></b>

<b>UV 缩放</b> *浮点2*&#x200B;在X（水平）和Y（垂直）中调整映射坐标的比例。\
值越高，平铺的图像就越密。<b></b>

<b>模式</b> *整数*&#x200B;选择图像应沿其映射的样条的方法：\
*- Draw样条列表*：使用输入列表中的所有样条；\
*— 绘制单样条*：仅使用具有指定索引的样条；\
*- Draw样条范围*：仅使用指定范围中包含索引的样条。

<b>绘制样条索引</b> *整数* （“模式”设置为“绘制单样条”时可用）图像应映射到的样条索引。

<b>绘制样条范围</b> *Integer2* （当“模式”设置为“绘制样条范围”时可用）图像应映射的样条索引范围。

<b>开始</b> *浮动*&#x200B;偏移应映射的样条部分的开始。\
该值表示样条的规范化长度。

<b>结束</b> *浮动*&#x200B;偏移应映射的样条部分的端点。\
该值表示样条的规范化长度。

<b>Thickness模式</b> *整数*&#x200B;设置映射图像Thickness的方法：\
*— 手动*：使用任意值显式设置Thickness；\
*— 来自样条*：使用样条的Thickness。

<b>Thickness</b> *浮点* （在“Thickness模式”设置为“手动”时可用）沿样条映射的图像Thickness的任意值。<b></b>

<b>Thickness乘数</b> *浮点* （“Thickness模式”设置为“来自样条”时可用）映射图像沿样条的Thickness的全局乘数，当该Thickness由样条驱动时。

<b>形状</b> *整数*&#x200B;用于沿样条映射图像坐标的基本形状：\
*— 平面*：坐标映射到平面上；\
*— 半圆柱体*：坐标映射到基圆轴跟随样条方向的一个半圆柱体；\
*— 圆柱体*：坐标映射到基圆的轴沿样条方向移动的圆柱体。<b></b>

<b>柱面Height乘数</b> *浮点*（在“形状”设置为“半圆柱体”或“圆柱体”时可用）圆柱体Height在Height输出中贡献的强度的乘数。\
Height调整是累计的。

<b>圆柱体Height偏移</b> *浮点*（当“形状”设置为“半圆柱体”或“圆柱体”时可用）\
将“圆柱体”或“半圆柱体”形状轮廓的中心从样条曲面偏移到曲面下面的一个直径。

<b>扭转UV强度</b> *浮动*（在“形状”设置为“半圆柱体”或“圆柱体”时可用）图像坐标围绕圆柱体的扭曲，以旋转次数为单位。\
扭转仅涉及在样条线的末端旋转圆柱体。 然后沿样条插入旋转。

<b>扭转UV曲线乘数</b> *浮点*（在“形状”设置为“半圆柱体”或“圆柱体”时可用）Twist Curve输入对圆柱体扭曲的贡献强度的乘数。\
曲线提供沿样条旋转量的轮廓，行中的第一个像素是样条起始处的旋转，最后一个像素是终止处的旋转。 灰度值表示若干转弯。

<b>扭转UV曲线偏移</b> *浮点* （当“形状”设置为“半圆柱体”或“圆柱体”时可用）将全局偏移应用于Twist Curve提供的旋转值（轮次数）。

<b>样条Height乘数</b> *浮动*&#x200B;调整样条线Height输入对Height输出的贡献的强度。\
Height调整是累积的。<b></b>

<b>输入Height乘数</b> *浮动*&#x200B;调整Height映射输入对Height输出的贡献的强度。\
Height调整是累计的。

<b>非方形校正&#x200B;</b>*布尔值*&#x200B;调整点的位置和Thickness以保持样条形状的非方形分辨率。\
这也会影响均匀分布。

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/SplineMapperGrayscale-Demo.gif "节点示例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例3](../../../../../../assets/SplineMapperGrayscale-Variant1-After1.jpg "节点示例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
