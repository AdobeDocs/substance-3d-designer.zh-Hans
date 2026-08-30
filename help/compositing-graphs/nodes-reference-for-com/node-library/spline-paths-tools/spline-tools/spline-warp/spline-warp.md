---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: 使用“样条变形”节点沿样条路径扭曲纹理，以创建弯曲的有机图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条变形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---


# 样条变形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-warp.resources/spline-warp-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据输入强度映射或矢量映射置换输入样条。

可以使用衰减控件沿样条调整变形效果的强度。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>预览</b> <i>灰度</i> | 作为灰度图像的输入样条的预览。 |
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |
| <b>强度图</b> <i>灰度</i> | （当“使用矢量图”设置为“假”时可用）用于控制输入样条上变形效果的方向和强度的输入灰度图像。<br>图像中每个像素的颜色指定乘数，用于沿样条点的法线（即，垂直于样条线的方向）将样条点移动到图像的整个范围。<br>当读取为乘数： 0和1时，图像中的[0； 1]值将重新映射到[-1； 1]范围：0和1以相同的距离替换样条，但方向相反。 0.5使样条保持不变。 |
| <b>矢量图</b> <i>灰度</i> | （当“使用矢量图”设置为“真”时可用）用于控制输入样条上变形效果的方向和强度的输入彩色图像。<br>图像中每个像素的颜色指定矢量(X、Y)，坐标以红色(X)和绿色(Y)通道编码。 +X表示正确，+Y表示失败。<br>当读取为矢量坐标时，图像中的[0； 1]值将重新映射到[-1； 1]范围：0个红色替换点左侧，0个绿色替换点上侧。 0.5红色和绿色保留花键位置。 |
| <b>衰减曲线</b> <i>灰度</i> | 使用曲线第一行像素的值描述曲线的图像。<br>在使用衰减曲线参数设置为True时，此输入用于控制在样条起始和结束附近弯曲效果的衰减。<br>曲线提供了衰减的配置文件，行中的第一个像素是样条起始处的变形效果强度，最后一个像素是结尾处的强度。 灰度值是强度。<br>您可以使用“曲线”节点创建曲线。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>预览</b> <i>灰度</i> | 输出样条作为灰度图像的预览。 |
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输出样条点的坐标。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输出样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输出样条的数量。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>变形强度</b> <i>浮动</i> | 花键移动的强度。 |
| <b>变形中心</b> <i>浮动</i> | 指定与保留样条相对应的“强度映射”值。<br>值为0或1表示只能在一侧移动样条。 |
| <b>采样模式</b> <i>整数</i> | 将强度映射或矢量映射中的值映射到样条的方法： <br>- <i>纹理空间</i>：将这些值应用于样条，如果使用纹理的UV坐标将这些值放置在纹理中，则将这些值应用于样条。 这有效地将值应用于样条的“原位”；<br>- <i>沿样条水平</i>：值直接应用于编码后的样条坐标（请参阅样条坐标输入），其中每行从上到下应用于不同的样条；<br>- <i>Hor。 沿样条线(rand. 偏移X)</i>：值直接应用于已编码的样条坐标（请参阅样条坐标输入），并且在每个样条的“比例映射”（即，样条坐标中的每一行）中具有随机水平偏移；<br>- <i>Hor。 沿样条线(rand. 偏移Y)</i>：值直接应用于已编码的样条坐标（请参阅样条坐标输入），并且在每个样条的“比例映射”（即，样条坐标中的每一行）中具有随机垂直偏移。 |
| <b>使用矢量图</b> <i>布尔值</i> | 将放置样条的方法切换到使用矢量映射输入来指定位移的方向。<br>图像中每个像素的颜色指定矢量(X、Y)，坐标以红色(X)和绿色(Y)通道编码。 +X表示正确，+Y表示失败。<br>当读取为矢量坐标时，图像中的[0； 1]值将重新映射到[-1； 1]范围：0个红色替换点左侧，0个绿色替换点上侧。 0.5红色和绿色保留花键位置。 |
| <b>使用衰减曲线</b> <i>布尔值</i> | 允许使用在衰减曲线输入图像中编码的曲线控制样条沿线的变形效果的强度。 |
| <b>强度图拼贴</b> <i>浮动</i> | （当“采样模式”未设置为“纹理空间”时可用）直接映射到样条坐标时调整强度映射的拼贴（请参阅样条坐标输入）。 |
| <b>开始衰减</b> <i>浮动</i> | （当“使用衰减曲线”设置为“假”时可用）在样条开始处衰减变形效果的乘数。<br>值为1表示在样条开始处不应用变形。 |
| <b>结束衰减</b> <i>浮动</i> | （当“使用衰减曲线”设置为“假”时可用）在样条末端附近衰减变形效果的乘数。<br>值为1表示样条末端不应用变形。 |
| <b>重新计算切线</b> <i>布尔值</i> | 如果为True，则在应用变形效果后重新计算样条的正切。<br>这样可以确保样条在节点（如样条上的正切或样条流映射器）中使用时，样条的散点与其轨迹保持一致。 |
| <b>预览</b> |  |
| <b>段数量</b> <i>整数</i> | 调整用于在预览输出中绘制样条可视化效果的段数。<br>值越高，线条越平滑。 |
| <b>显示方向帮助程序</b> <i>布尔值</i> | 在“预览”输出中，在样条的起始处显示一个点，在其结尾处显示一个箭头。 |
| <b>显示Thickness信封</b> <i>布尔值</i> | 在样条Thickness的边显示附加线。 |
| <b>Thickness（像素）</b> <i>浮动</i> | 调整预览输出中样条可视化的Thickness（以像素为单位）。 |
| <b>背景预览强度</b> <i>浮动</i> | 值与背景预览输入图像相乘。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2之前">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![节点示例1](spline-warp.resources/SplineWarp-Demo.gif "节点示例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
