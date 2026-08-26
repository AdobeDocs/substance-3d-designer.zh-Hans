---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/triangle-grid.html"
breadcrumb-title: ''
description: 使用Triangle Grid节点生成三角形网格图案，以便在Substance 3D Designer中创建几何纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Triangle Grid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangle Grid
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---


# Triangle Grid

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/trianglegridgrayscale.jpg){width="200px"}

![](../../../../../../assets/trianglegridcolor.jpg){width="200px"}

<b>英寸：</b>纹理生成器>图案

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**Triangle Grid**&#x200B;节点使用Z向正交投影在3D空间内生成&#x200B;*顶点*&#x200B;中的&#x200B;*三角化曲面*&#x200B;的灰度表示。

使用&#x200B;**颜色输出**&#x200B;参数可以选择用于表示法的数据，从而生成各种视觉样式。\
可以调整顶点的&#x200B;*位置*，这会影响生成的网格。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 输出连接器

</td>
<td style="border: 0;" valign="top">

### 参数

</td>
</tr>
</table>

## 输入连接器

|  |  |
| --- | --- |
| <b>Height</b> *灰度*&#x200B;主要 | 用于映射顶点的&#x200B;*Height*（即Z位置）的灰度图像输入。    此输入的影响由“Height输入乘数”参数控制。 |
| <b>矢量图</b> *颜色* | 用于映射X轴和Y轴上的顶点的&#x200B;*位移*&#x200B;的彩色图像输入。    X/Y偏移分别映射到图像的R/G通道。    此输入的影响由“矢量映射位移”参数控制。 |
| <b>颜色输入</b> *颜色* | 用于映射顶点、段或三角形的&#x200B;*颜色*&#x200B;的彩色图像输入。    此输入在“颜色源”参数设置为“颜色输入”时使用。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *颜色* | 输出图像。 |

## 参数

|  |  |
| --- | --- |
| <b>颜色输出</b> *整数* | 表示三角化曲面的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>每个顶点：</b>为每个顶点分配一种颜色，并沿三角形表面插值</li> <li data-preserve-html="true"><b>每个三角形：</b>为每个三角形分配一种平面颜色</li> <li data-preserve-html="true"><b>细线</b><b>：</b>将轮廓应用于顶点之间的段</li> <li data-preserve-html="true"><b>到边缘的距离</b><b>：</b>渲染到每个三角形上最近的段的距离</li> <li data-preserve-html="true"><b>中心</b><b>：</b>呈现到每个三角形的重心处的规范化距离</li> </ul> |
| <b>三角化</b> *整数* | 设置曲面的三角化方法，即四边形中的&#x200B;*对相对顶点*&#x200B;应连接：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自动：</b>自动选择一对顶点，使三角形<i>朝向相机最小远处</i><br/> <b>45°：</b>连接相对顶点，产生一条相对于X右轴<i>旋转45度</i>的线</li> <li data-preserve-html="true"><b>-45°：</b>连接相对顶点，产生一条相对于X右轴<i>旋转–45度</i>的线</li> <li data-preserve-html="true"><b>Quincux horizontal：</b>交替三角化方向<i>每隔一行</i>顶点</li> <li data-preserve-html="true"><b>Quincux垂直：</b>替代三角化方向<i>每隔一列</i>顶点<br/> </li> </ul> |
| <b>X数量</b> *整数* | 在X轴上生成的顶点的数量。 |
| <b>Y数量</b> *整数* | 在Y轴上生成的顶点的数量。 |
| <b>随机位置乘数</b> *浮动* | 调整主变形效果的强度。 |
| <b>随机位置</b> *浮点2* | 调整应用于每个顶点的X和Y位置的随机偏移的强度，相对于网格中其单元格&#x200B;*的*&#x200B;大小。   此偏移量&#x200B;*栈叠*&#x200B;具有<b>Quincux偏移量</b>和<b>矢量映射位移</b>参数。 |
| <b>矢量图位移</b> *浮动* | 使用从<b>矢量映射</b>输入值&#x200B;*采样*&#x200B;调整应用于每个顶点的&#x200B;*全局*&#x200B;位移量。    此偏移量&#x200B;*栈叠*&#x200B;具有<b>随机位置</b>和<b>双色偏移</b>参数。 |
| <b>双色偏移X</b> *浮动* | 将指定的偏移量应用于顶点的&#x200B;*每隔一行*，相对于网格中其单元格的&#x200B;*大小*。   此偏移量&#x200B;*栈叠*&#x200B;具有<b>随机位置</b>和<b>矢量映射位移</b>参数。 |
| <b>昆曲位移Y</b> *浮动* | 将指定的偏移量应用于顶点的&#x200B;*其他每列*，相对于网格中其单元格的&#x200B;*大小*。    此偏移量&#x200B;*栈叠*&#x200B;具有<b>随机位置</b>和<b>矢量映射位移</b>参数。 |
| <b>旋转</b> *浮动* | 围绕每个顶点的&#x200B;*基位置*&#x200B;应用&#x200B;*指定的*&#x200B;旋转量 — 即，应用随机偏移和位移之前&#x200B;*的位置*。    此旋转&#x200B;*用<b>旋转无序</b>参数栈叠*。 |
| <b>旋转无序</b> *浮动* | 围绕每个顶点的&#x200B;*基位置*&#x200B;应用&#x200B;*随机*&#x200B;旋转量 — 即应用随机偏移和位移之前&#x200B;*的位置*。    此旋转&#x200B;*用<b>旋转</b>参数栈叠*。 |
| <b>输入乘数</b>Height *浮动* | 使用从<b>Height</b>输入值&#x200B;*采样*&#x200B;调整每个顶点的Z位置。    此偏移量&#x200B;*栈叠*&#x200B;具有<b>Height随机</b>参数。 |
| <b>Height随机</b> *浮动* | 将随机偏移应用于每个顶点的Z位置。  此偏移量&#x200B;*栈叠*&#x200B;与<b>输入乘数</b>参数Height。 |
| <b>混合模式</b> *整数* | 设置&#x200B;*重叠三角形*&#x200B;值的混合方法。 使用该模式，您可以有效地选择&#x200B;*应显示哪些*&#x200B;三角形： <ul data-preserve-html="true"> <li data-preserve-html="true"><b>分钟：</b>个文本</li> <li data-preserve-html="true"><b>最大：</b>个文本</li> <li data-preserve-html="true"><b>深度测试</b>：文本</li> <li data-preserve-html="true"><b>Alpha混合：</b>文本</li> </ul>注意：可用的混合模式取决于<b>颜色输出</b>参数的值。 |
| <b>颜色源</b> *整数* *在“颜色输出”参数设置为“每个顶点”、“每个三角形”或“细线”时可用。* | 设置&#x200B;*获取颜色*&#x200B;的方法 — 即明亮度，应根据选定的<b>颜色输出</b>模式分配给顶点、三角形或线段：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Height</b><b>：</b>将顶点的Height用作明亮度</li> <li data-preserve-html="true"><b>随机</b><b>：</b>使用随机明亮度值</li> <li data-preserve-html="true"><b>颜色输入</b><b>：</b>使用从<b style="">颜色输入</b>输入取样的值</li> </ul> |
| <b>颜色源不透明度</b> *浮点* *在“颜色输出”参数设置为“细线”时可用。* | 使用从所选<b>颜色源</b>生成的值控制<b>线条颜色</b>值的&#x200B;*覆盖*。   注意：当此值设置为1时，<b>线条颜色</b>参数没有影响。 |
| <b>到边缘Thickness的距离</b> *浮点* *在“颜色输出”参数设置为“到边缘的距离”时可用。* | 设置距离渐变的Thickness。 较低的值会生成&#x200B;*更短的*&#x200B;渐变。 |
| <b>线条颜色</b> *浮点/浮点4* *在“颜色输出”参数设置为“细线”时可用。* | 线段的明亮度值。   注意：当<b>颜色源不透明度</b>值设置为1时，此参数没有影响。 |
| <b>背景颜色</b> *浮点/浮点4* *在“颜色输出”参数设置为“细线”时可用。* | 段之间可见的背景的明亮度值。   注意：当<b>混合模式</b>设置为&#x200B;*最大值*&#x200B;时，背景将覆盖其亮度&#x200B;*较亮*&#x200B;的段（如预期的那样）。 |
| <b>随机颜色种子模式</b> *整数* *在“颜色输出”参数设置为“按顶点”、“按三角形”或“细线”并且“颜色源”参数设置为“随机”时可用。* | 获得用于伪随机色彩分布的种子的方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>全局随机植入</b><b>：</b>继承节点图表的植入</li> <li data-preserve-html="true"><b>手动种子</b><b>：</b>使用自定义离散种子</li> </ul> |
| <b>随机颜色种子</b> *整数* *在“随机颜色种子模式”参数设置为“手动种子”并且“颜色源”参数设置为“随机”时可用。* | 在伪随机颜色分布中使用的离散种子值。 |
| <b>非正方形扩展</b> *布尔值* | 启用以非方形比例补偿挤压和拉伸。 |

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid：示例1](../../../../../../assets/triangle_grid_color_example_1.jpg "Triangle Grid：示例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：示例2](../../../../../../assets/trianglegrid-variant2.png "Triangle Grid：示例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：示例3](../../../../../../assets/trianglegridcolor-variant2.jpg "Triangle Grid：示例3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid：示例4](../../../../../../assets/triangle_grid_color_example_2.jpg "Triangle Grid：示例4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：示例5](../../../../../../assets/trianglegridcolor-variant4.jpg "Triangle Grid：示例5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：示例6](../../../../../../assets/trianglegridcolor-variant3.jpg "Triangle Grid：示例6"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid：皮革](../../../../../../assets/trianglegrid-demo.png "Triangle Grid：皮革"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：图形](../../../../../../assets/trianglegrid-node.png "Triangle Grid：图形"){zoomable="yes"}

</td>
</tr>
</table>
