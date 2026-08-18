---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: 使用散点跨图集的纹理，以便从扫描的材质创建拼贴图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 0%

---


# Atlas Scatter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/atlas-scatter.png){width="200px"}

## Atlas Scatter

**在：** *材质筛选器/扫描处理*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

从Atlas中提取元素，并将其散点在背景上。 Atlas输入是全素材，由排列并打包在单个纹理片上的单个元素组成。 此节点会将其拆分（使用内部[Atlas Splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md)进程）并散点，这类似于[形状飞溅](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)。 Atlas Scatter至少需要“不透明度映射”输入以及“贴图集”的“Height映射”输入才能正常工作。

>[!NOTE]
>
> 数以百计的[地图集](https://source.substance3d.com/allassets?assetType=substanceAtlas)可在[Substance Source](https://source.substance3d.com/)上使用，这些地图集可以在Atlas Scatter节点中使用。

## 输入和参数

### 参数

* **Atlas输入分辨率**： *分辨率，1到12*\
  手动设置完整输入地图集的分辨率，以确保良好的性能相对于质量比率。
* **X数量**： *1 - 64*\
  图案的X重复次数。
* **Y数量**： *1 - 64*\
  图案的Y重复次数。
* **图案**
  * **模式范围**： *0 - 10*\
    定义要散布的图案范围。 如果设置为0，将使用所有模式。
  * **图案分布模式**： *随机，图案索引，行索引，列索引*&#x200B;定义使用贴图集元素的顺序。
  * **模式分布图乘数**： *0.0 - 1.0*\
    根据输入图像的灰度值选择形状图案。
  * **图案旋转**： *0， 90， 180， 270*\
    按选定的度数对每个贴图集元素应用固定旋转。
  * **图案旋转随机**： *0.0 - 1.0*\
    将随机旋转应用于贴图集元素的设置部分。
  * **Atlas形状检测精度**：*简单或较小的形状、复杂或较大的形状、无故障模式*\
    设置检测形状的精度。 精度越高，对性能的影响越大。
  * **缩小贴图集不透明度（更快的检测）**： *-4 - 0*\
    用于控制输入贴图集不透明度贴图的缩小比例，该贴图集用于形状检测。 分辨率越低，性能越好，但代价是准确性。
  * **忽略小于**&#x200B;的形状： *0.0 - 1.0*&#x200B;设置必须检测形状的最小大小，以整体图像的比例表示
* **大小**
  * **缩放**： *0.0 - 5.0*\
    设置散布形状的相对比例。
  * **随机缩放**： *0.0 - 1.0*\
    定义用于对每个散布形状应用随机缩放的乘数。
  * **缩放无重叠**： *0.0 - 1.0*\
    缩小形状比例，以便它们不会重叠。
  * **比例图乘数**： *0.0 - 1.0*\
    将形状比例乘以输入图像灰度值的函数。
  * **大小**： *0.0 - 1.0*\
    按长度(X)和宽度(Y)设置散布形状的相对比例。
  * **来自Bg斜率的大小比例**： *0.0 - 1.0*\
    在背景斜率的函数中修改形状大小比例。
  * **保留长宽比**： *0.0 - 1.0*\
    确定应保留散布形状的原始比例的量，而不是使用其网格单元格比率，即“X数量”和“Y数量”值的比率。
* **位置**
  * **位置随机**： *0.0 - 2.0*\
    用于从网格起始点沿随机方向移动每个形状的乘数。
  * **随机分布**： *高斯，一致*\
    对随机位置从高斯分布切换到均匀分布。 与均匀分布相比，高斯分布会产生更自然的结果。
  * **矢量映射乘数**： *0.0 - 1.0*\
    控制矢量映射输入的影响，以便沿由映射的红色(X)和绿色(Y)通道指定的矢量的方向移动形状。
  * **水平偏移**： *-2.0 - 2.0*\
    沿X轴的位置偏移的乘数。
  * **垂直偏移**： *-2.0 - 2.0*\
    沿Y轴的位置偏移的乘数。
  * **越界选项**： *缩放形状，约束位置*\
    由于飞溅的技术性质，形状不能绘制到距离原始位置2个单元格以上的单元格大小。 如果形状变得过大或被移动过远，您有两个选项： — 缩放形状会在形状达到边界时减小形状大小 — 约束位置会将形状移回其原始位置
* **旋转**
  * **旋转**： *0.0 - 1.0*\
    允许您控制所有形状的局部旋转。
  * **旋转随机**： *0.0 - 1.0*\
    应用于每个形状的随机旋转量的乘数。
  * **从背景斜率旋转**： *0.0 - 1.0*\
    在背景斜率中修改形状旋转。 通常与“来自Bg斜率的大小比率”参数结合使用
  * **旋转贴图乘数**： *0.0 - 1.0*\
    将形状旋转乘以输入图像灰度值的函数。
  * **矢量映射乘数**： *0.0 - 1.0*\
    设置矢量图像输入的形状旋转函数。
* **Height**
  * **Height比例自动调整**： *False/True*\
    根据图案比例自动调整Height，以使形状Height与背景Height成比例。
  * **混合模式**： *Height混合，Alpha测试*\
    设置解决形状重叠的方法。
  * **Height偏移**： *-1.0 - 1.0*\
    将全局偏移应用于形状Height
  * **Height偏移随机**： *0.0 - 1.0*\
    应用于每个形状的随机Height偏移的乘数
  * **Height偏移映射多路复用器**： *0.0 - 1.0*\
    将形状Height偏移乘以输入图像灰度值的函数。
  * **Height比例**： *0.0 - 1.0*\
    可让您控制散布形状的全局Height缩放
  * **随机Height缩放**： *0.0 - 1.0*\
    应用于每个形状的随机Height缩放的乘数
  * **Height的比例映射乘数**： *0.0 - 1.0*\
    将形状Height比例乘以输入图像灰度值的函数。
  * **遵从背景**： *0.0 - 1.0*\
    设置为0时，形状Height将保持不变，设置为1时，形状Height将由下面的Height背景变形。
  * **平滑匹配背景**： *0.0 - 2.0*\
    允许您控制应用于形状与背景匹配时的Height变形的平滑量。
  * **从背景斜率倾斜**： *0.0 - 1.0*\
    根据局部背景斜率使形状Height变形：在形状Height中添加与背景斜率对应的线性渐变。
  * **后台Smoothness**： *0.0 - 2.0*\
    控制形状根据背景斜率进行倾斜时，应用到该斜率的平滑量。
  * **抠图黑色像素**： *False/True*\
    忽略模式输入中的黑色值。
  * **拼合图案库**： *False/True*\
    用于拼合形状下方的背景Height以匹配开始Height。
* **蒙版**
  * **掩码随机**： *0.0 - 1.0*\
    遮盖随机数量的形状，表示为总量的比率。
  * **掩码随机映射乘数**： *0.0 - 1.0*\
    根据灰度图像输入设置随机形状蒙版。
  * **来自Bg斜率的蒙版**： *-1.0 - 1.0*\
    根据形状所在位置的背景斜率控制形状的蒙版。
* **颜色**
  * **颜色调整**： *-1.0 - 1.0*\
    用于全局调整散布元素的颜色。
  * **颜色随机**： *0.0 - 1.0*\
    用于按每个形状的随机量移动颜色值的乘数。
  * **背景颜色**： *0.0 - 1.0*\
    将形状颜色移到背景颜色所在的位置
* **正常**
  * **从背景斜率倾斜**： *0.0 - 1.0*\
    根据背景法线将形状法向倾斜。
  * **正常随机**： *0.0 - 1.0*\
    将形状法向倾斜每个形状的随机量的乘数。
  * **普通格式**： *DirectX，OpenGL*\
    在不同的法线贴图格式之间切换（反转绿色通道）
* **粗糙度**
  * **粗糙度调整**： *-1.0 - 1.0*\
    允许您将全局形状粗糙度偏移。
  * **背景粗糙度**： *0.0 - 1.0*\
    将形状粗糙度移动到其位置的背景粗糙度。
  * **粗糙度随机**： *0.0 - 1.0*&#x200B;用于按每个形状的随机量抵消粗糙度的乘数。

## 示例图像

![](../../../../../../assets/atlas-scatter-11.png){width="512px"}

</td>
</tr>
</table>
