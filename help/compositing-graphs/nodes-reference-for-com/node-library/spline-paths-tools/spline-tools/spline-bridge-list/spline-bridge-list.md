---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: 使用“样条桥列表”节点可在复杂图案列表中多个样条之间桥接纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条桥（列表）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---


# 样条桥（列表）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/spline-bridge-list-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成沿这些样条遍历输入列表中的所有样条的样条。

生成的样条可以是线性（直线）或二次贝塞尔曲线（曲线）。

</td>
</tr>
</table>

>[!TIP]
>
> 生成的样条从列表中的第一个样条转到最后一个样条，并严格遵循列表中这些样条的顺序来遍历中间样条。
> 
> 因此，您应留意预先将样条附加在一起的顺序。

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

<b>桥样条量</b> *整数*&#x200B;跨输入样条生成的样条数。

<b>桥样条类型</b> *整数*&#x200B;生成的样条类型：
* 线性：将中间样条与直线轨迹从起点到终点连接起来的锐样条；
* 二次贝塞尔曲线：连接中间样条与从起点到终点平滑轨迹的曲线样条。\
  注意：计算二次贝塞尔曲线样条需要至少3条输入样条。

<b>输入样条已关闭</b> *布尔值*&#x200B;控制输入样条的第一个点和最后一个点是否应作为一个点进行处理。 这防止了重复第一和最后遍历样条。

<b>翻转方向</b> *布尔值*&#x200B;反转样条线的方向。

<b>关闭Bridge样条</b> *布尔型*&#x200B;扩展遍历样条以连接回输入列表中的第一个样条。

<b>第一桥样条偏移&#x200B;</b>*浮点2*&#x200B;将偏移应用于所有遍历样条的开始。 该值是输入样条的规范化长度。\
生成的样条与所遍历样条的起始点或结束点相接在一起，并留在该处。

<b>上次桥样条偏移&#x200B;</b>*浮点2*\
将偏移应用到所有遍历样条的末尾。 该值是输入样条的规范化长度。\
生成的样条与所遍历样条的起始点或结束点相接在一起，并留在该处。

<b>随机偏移范围</b> *整数*&#x200B;用于应用于样条的随机偏移的最大距离。\
*— 父样条：*&#x200B;使用父样条的完整长度。 可能会导致重叠。\
*— 间隔：*&#x200B;使用网桥样条之间的间隔。 这可以缓解重叠问题。 此距离随着桥式样条的增加而减小。

<b>开始随机偏移</b> *浮点*&#x200B;应用于桥样条的开始位置的随机偏移的乘数，其中最大距离由<b>随机偏移范围</b>参数指定。

<b>结束随机偏移</b> *浮点*&#x200B;应用于桥样条的结束位置的随机偏移的乘数，其中最大距离由<b>随机偏移范围</b>参数指定。

<b>全局随机偏移</b> *浮点*&#x200B;应用于&#x200B;*双方*&#x200B;桥样条的起始位置和结束位置的&#x200B;*相等数量*&#x200B;随机偏移的乘数，其中最大距离由<b>随机偏移范围</b>参数指定。

<b>均匀分布</b> *布尔值*&#x200B;为True时，生成的样条的点从开始到结束均匀分布。

+++粗细
<b>Thickness模式</b> *整数*&#x200B;获取桥样条Thickness值的方法。\
*— 从父样条继承：*&#x200B;使用父样条在桥样条起点和终点位置的Thickness\
*— 覆盖：*&#x200B;使用了您在<b>Thickness</b>参数中指定的任意值

<b>Thickness</b> *浮动*&#x200B;应用于桥样条的绝对Thickness值。

<b>Thickness随机</b> *浮点*&#x200B;桥样条Thickness的随机乘数，其中应用此乘数的初始Thickness由<b>Thickness模式</b>参数指定。

+++

+++高度
<b>Height模式</b> *整数*&#x200B;获取桥样条Height值的方法。\
*— 从父样条继承：*&#x200B;使用父样条在桥样条起点和终点位置的Height\
*— 覆盖：*&#x200B;使用了您在<b>Height</b>参数中指定的任意值

<b>Height偏移</b> *浮动*&#x200B;将Height应用于桥样条之前，从父样条继承的Height的偏移量。

<b>Height</b> *浮动*&#x200B;应用于桥样条的绝对Height值。

<b>Height随机</b> *浮动*&#x200B;对桥样条Height的随机调整，其中调整取决于选定的<b>Height模式</b>参数：\
*— 从父样条继承：*&#x200B;该值是继承Height的乘数。\
*— 覆盖：*&#x200B;该值是添加到Height的偏移。

+++

<b>非方形校正&#x200B;</b>*布尔值*

调整点的位置和Thickness以保持样条形状的非方形分辨率。\
这也会影响均匀分布。

+++预览
<b>显示方向帮助程序</b> *布尔值*&#x200B;在预览输出中，在样条线的起始处显示一个点，在其结尾处显示一个箭头。

<b>显示Thickness信封</b> *布尔值*\
在样条Thickness的边显示附加线。

<b>段数量</b> *整数*&#x200B;调整用于在预览输出中绘制样条可视化效果的段数。\
值越高，线条越平滑。

<b>Thickness（像素）</b> *浮动*&#x200B;以像素为单位调整样条可视化在预览输出中的Thickness。

<b>背景预览强度</b> *浮动*&#x200B;预览可视化的强度。

+++

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_Before.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_After.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/SplineBridge-List_Demo.gif "节点示例2")

</td>
</tr>
</table>

![图形中的节点](../../../../../../assets/SplineBridge-List_Graph.jpg "图形中的节点")
