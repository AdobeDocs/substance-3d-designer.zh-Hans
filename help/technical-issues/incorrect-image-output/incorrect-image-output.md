---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/incorrect-image-output.html"
breadcrumb-title: ''
description: 对Substance 3D Designer中的图像输出错误问题进行故障诊断，并了解如何修复渲染问题。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Incorrect image output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图像输出不正确
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 0%

---


# 图像输出不正确

本页列出了Substance 3D Designer中导致图像输出意外错误的技术问题，并提供了相应的故障排除步骤。

## 可见步进/条带

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（错误）](incorrect-image-output.resources/error.svg)问题**

图像输出中的渐变是阶梯式的，而不是平滑的。 步进是由图像使用的&#x200B;*值范围太窄引起的*。\
这意味着没有足够的值来平滑地从渐变的一个步骤过渡到下一个步骤。

可使用整数或浮点值对明亮度/RGBA值进行编码，这会影响其&#x200B;*精度*：

* **整数**&#x200B;提供8位精度（0-255，因此256个可能的值）和16位精度（0-65535，因此65536可能的值）来存储0-1范围内的值。
* **浮点**&#x200B;提供16位(HDR 16F)和32位(HDR 32F)精度，能够存储0-1范围之外的值（包括负值）。 这样，您就可以处理高动态范围(HDR)图像，其中明亮度值可能远远高于1.0。

如果您不需要专门处理HDR图像，则您的大多数节点可能都使用整数编码输出0-1范围内的值。 如果图像的输出格式为8位，则图像只能使用256值，这通常会导致出现明显的渐变阶梯。 这尤其可能会影响“正常”节点的输出。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/incorrect-image-output-01.png){width="256px"}![](incorrect-image-output.resources/incorrect-image-output-02.png){width="256px"}![](incorrect-image-output.resources/incorrect-image-output-03.png){width="256px"}

</td>
</tr>
</table>

**![（刻度）](incorrect-image-output.resources/check.svg)建议的步骤**

检查该节点及上游所有节点的&#x200B;**输出格式**（即，位深度），并确保这些节点使用至少&#x200B;*16位整数精度*。

Output format参数通常设置为&#x200B;*相对于输入* [继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，这样可以在整个图形中传播低精度。 理想情况下，在图形中向上游走，即可找到问题的根源。

通过查看节点下显示的文本信息，可以快速确定节点输出的精度：

* **L/C**&#x200B;表示图像是灰度（即明亮度）或彩色
* **8/16**&#x200B;表示整数编码
* **16F/32F**&#x200B;表示浮点编码

例如：

* L8：灰度8位整数
* C16：彩色16位整数
* C32F：颜色32位浮点(HDR)

## 已发布的SBSAR中的质量损失

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

<b>![（错误）](incorrect-image-output.resources/error.svg)问题</b>

Substance 3D档案(SBSAR)输出的图像质量明显低于其发布来源Substance 3D文件的图形，如右侧的图像所示。\
输出显示低分辨率。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/incorrect-image-output-04.jpg){width="256px"}

</td>
</tr>
</table>

<b>![（刻度）](incorrect-image-output.resources/check.svg)建议的步骤</b>

确保所有[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点的[输出大小](../../compositing-graphs/output-size/output-size.md)属性都设置为&#x200B;*绝对* [继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。

否则，它们引用的[位图资源](../../resources/bitmap-resource/bitmap-resource.md)将以默认的256\*256分辨率保存在已发布的Substance 3D存档中，这将*&#x200B;影响一个或多个输出的质量*。

## 图像模糊

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（错误）](incorrect-image-output.resources/error.svg)问题**

使用某些节点后，形状略微模糊，如[变换2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)或[混合](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/incorrect-image-output-05.jpg){width="256px"}

</td>
</tr>
</table>

**![（刻度）](incorrect-image-output.resources/check.svg)建议的步骤**

在重新排列图像中的像素时（例如，在调整形状大小或更改图像分辨率时），有两种方法可确定应如何&#x200B;*将源中的像素*&#x200B;映射到目标：

* **最接近**：像素将被映射到匹配坐标处的目标&#x200B;*原样*。 如果目标的分辨率较低，则可以完全忽略像素。 如果目标具有更高分辨率，则将映射到覆盖其范围的所有像素。 输出更清晰&#x200B;**，看起来略有&#x200B;*锯齿*。
* **双线性滤波**：对源图像应用滤波过程，以便其像素以&#x200B;*平滑*&#x200B;像素之间过渡的方式映射到目标分辨率。 输出为&#x200B;*更平滑*，看起来略有&#x200B;*模糊*。

[变换2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)节点提供了&#x200B;**筛选方法**&#x200B;选项，以选择应使用的这两种映射方法中的哪一种。

在对不同分辨率的输入纹理进行采样时，大多数节点（例如，[混合](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)）默认为&#x200B;*双线性滤波*，这可能会引入不需要的模糊。\
由于Transformation 2D节点为&#x200B;*原子*，因此非常轻量级，因此&#x200B;*即使不需要变换*，也可以在将纹理发送到另一个节点之前，使用其[输出大小](../../compositing-graphs/output-size/output-size.md)属性更改纹理分辨率，这样您就可以&#x200B;*控制此调整大小的影响*。

在[像素处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)节点的[函数图形](../../function-graphs/function-graphs.md)中，**示例**&#x200B;节点包含&#x200B;*相同选项*，以控制应如何将采样纹理映射到节点分辨率。
