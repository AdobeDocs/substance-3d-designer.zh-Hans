---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: 使用“蒙版到路径”节点将蒙版纹理转换为路径数据，以便生成程序化的路径。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# 路径蒙版

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](mask-to-paths.resources/mask-to-paths-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

将灰度输入图案<b>蒙版</b>转换为在输出<b>路径</b>中编码的路径段列表。

控制所生成路径的开始位置及其在列表中的顺序可用。

可以使用专用节点（例如，[路径2D变换](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md)、[路径变形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md)）进一步处理生成的路径，也可以使用[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)节点将形状映射或沿其进行散点转换为样条。

</td>
</tr>
</table>

>[!NOTE]
>
> [路径格式规范](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)页面中介绍了用于对路径进行编码的方法。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>蒙版</b> <i>灰度</i> | 应转换为路径列表的输入模式。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>预览</b> <i>颜色</i> | 在蒙版顶部合成的预览有助于可视化参数的效果。 |
| <b>路径</b> <i>颜色</i> | 以彩色图像编码的路径列表。 每条路径描述一个已编码区段的列表。<br>可以使用其他路径处理节点处理结果，或将其发送到[路径到样条](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)节点以进一步将其处理为样条。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>平滑蒙版</b> <i>浮动</i> | 对输入蒙版应用平滑。<br>当输入图案具有非常锐利的边缘（通常会导致伪影）时非常有用。 |
| <b>蒙版阈值</b> <i>浮动</i> | <b>蒙版</b>的灰度值，将用来分离形状的外部（值&lt;蒙版阈值）和内部（值>蒙版阈值）。 |
| <b>抽取路径</b> <i>浮动</i> | 隐式控制将生成的线段数量。<br>大量抽取会使圆形呈现多边形，但没有任何抽取操作会生成几乎一条线段一个像素。<br>合理的抽取量会更好地匹配直线和曲线的形状，而不会为直线创建大量中间点。 |
| <b>关闭打开的路径</b> <i>布尔值</i> | 在开放路径的起始路径和结束顶点之间创建一个段。<br>禁用此项可能会以意想不到的方式修复图案上不希望出现的线条，但路径可能不会再关闭。 |
| <b>角阈值</b> <i>浮动</i> | 在路径中编码的每个顶点都可以包含一个标志，指示它是硬（即角）还是平滑。<br>此参数允许您根据相邻段之间的角度标记更多或更少的角。<br><i>注意：</i>此“角”标志当前不受任何现有节点支持，但可在[路径顶点处理器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)节点中使用。 您也可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)节点来可视化转角。 |
| <b>路径启动模式</b> <i>整数</i> | 选择哪个顶点应作为蒙版中形状周围每个已生成Path的开头的方法。<br>使用专用顶点将生成的<b>路径转换为样条</b>时，这会产生显着影响，因为多个样条节点使用样条的起始和结束。<br>*— 最锐化顶点：*&#x200B;与前两个节点形成最小角度的顶点&#x200B;<br>*— 在指定方向的极端顶点：*&#x200B;指定方向的最后一个顶点&#x200B;<br>*— 距离指定位置最近的顶点<br>*&#x200B;顶点距指定位置最远<br>*自定义启动函数：*使用自定义函数选择应用作每条顶点起点的path |
| <b>启动方向</b> <i>浮动</i> | 描述用于选择启动顶点的方向的角度。 对于每条路径，都选择了该方向的最后一个顶点。<br>该值是用来旋转X向左矢量的&#x200B;*匝数*。 这意味着0设置方向矢量(-1， 0)，0.25 （90度）设置方向矢量(0， 1)。<br><i>注意：</i>当<b>顶点启动模式</b>设置为“在指定方向的极端路径”时，此参数可用 |
| <b>启动目标位置</b> <i>浮点2</i> | 图像中用于选择启动顶点的位置。<br>根据所选的<b>顶点启动模式</b>，为每个路径选择最接近或最远离此位置的顶点。<br><i>注意：</i>当<b>路径启动模式</b>设置为“最接近指定位置的顶点”或“最远离指定位置的路径”时，此参数可用 |
| <b>启动函数</b> <i>浮动</i> | 用于选择启动顶点的函数。 它将返回浮点值。<br>对于每个顶点，将执行函数并选择函数为其返回&#x200B;*最高结果*&#x200B;的顶点。<br>可用变量：<br>*-*&#x200B;顶点.cornerness(Float)*：*&#x200B;顶点作为角候选者的分数&#x200B;<br>*-*&#x200B;顶点.pos(Float2)*：*&#x200B;顶点在图像空间中的位置<br><i>注意：</i>当顶点启动模式设置为“路径最接近指定位置”或“自定义启动函数”时，此参数可用 |
| <b>订购模式</b> <i>整数</i> | 生成路径的排序方法。<br>路径的位置或大小&#x200B;*定界框* (Bbox)可用作路径排序的标准。<br>使用专用节点将生成的<b>路径转换为样条</b>时，这会产生显着影响，因为多个样条节点使用样条的顺序。<br>*— 旧版（快速）：*&#x200B;此节点的上一版本中使用的方法，提供了显着更好的性能。<br>*— 沿方向Bbox的中心位置：*&#x200B;路径按其Bbox的中心位置从头到尾排序指定方向&#x200B;<br>*— 按Bbox Bbox沿方向的左上位置：*&#x200B;路径根据其Bbox的左上角位置按指定方向从第一个到最后一个进行排序&#x200B;<br>*— 按Bbox大小 — 从大到小：*&#x200B;路径根据其Bbox的大小排序，从大到小&#x200B;<br>*— 按Bbox大小 — 从小到大：*&#x200B;路径根据其Bbox的大小排序，从小到大&#x200B;<br>*— 自定义排序函数：*&#x200B;使用自定义函数订购路径 |
| <b>排序方向</b> <i>浮动</i> | 该角度描述了用于沿该方向从第一个路径排列到最后一个路径的方向。<br>该值是用来旋转X向左方向矢量的&#x200B;*匝数*。 这表示0设置方向矢量(-1,0)，0.25（90度）设置方向矢量(0,1)。 |
| <b>排序函数</b> <i>浮动</i> | 用于对路径进行排序的函数。 它将返回浮点值。<br>路径根据此函数的值按&#x200B;*升序*&#x200B;排序。 换句话说，每个Path的函数的结果是用于对路径排序的&#x200B;*排序键*。<br>可用变量：<br>* bbox.center (Float2)：路径Bbox的中心位置<br>* bbox.topleft (Float2)：路径Bbox的左上角位置<br>* bbox.size (Float2)：路径Bbox的大小（X：宽度，Y：Height） |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-After.jpg" alt="masktopaths-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
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

![节点示例2](mask-to-paths.resources/MaskToPaths-Demo2.gif "节点示例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![节点示例1](mask-to-paths.resources/MaskToPaths-Demo1.gif "节点示例1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例3：启动模式](mask-to-paths.resources/MaskToPaths-Demo3.gif "节点示例3：启动模式"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![节点示例3：排序模式](mask-to-paths.resources/MaskToPaths-Demo4.gif "节点示例3：排序模式"){zoomable="yes"}

</td>
</tr>
</table>
