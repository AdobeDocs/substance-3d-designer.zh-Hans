---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/output-size.html"
breadcrumb-title: ''
description: 配置Substance合成图形的输出大小设置以控制纹理分辨率和质量。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Output size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 输出大小
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 5%

---


# 输出大小

它是图形的<b>基本参数</b>中的第一个，与<b>输出格式</b>（或位深度）一起使用对于理解至关重要，因为它在Designer中以及作为[已发布的Substance 3D资源(SBSAR)](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)文件在其他图形中对SBSAR的输出都有很大影响。

>[!TIP]
>
> 我们强烈建议更好地了解Substance图中的[继承](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)，作为有效使用“输出大小”属性的基础。

>[!NOTE]
>
> 使用“![](output-size.resources/output-size-01.jpg)”锁定按钮使Height值&#x200B;*匹配*&#x200B;宽度值。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## 2个值的幂

输出大小参数确定图形或节点输出的&#x200B;*纹理*&#x200B;的分辨率。

一种纹理，它是图形计算中的对象，受图形处理硬件执行其计算的方式所施加的一些限制的约束。 这些限制之一是，纹理应该表示一个图像，其X和Y的像素数是&#x200B;*二的次方*。

</td>
<td width="33.33%" style="border: 0;" valign="top">

| 二的次方 | 像素 |
| --- | --- |
| 7 | 128 |
| 8 | 256 |
| 9 | 512 |
| 10 | 1024 |
| 11 | 2048 |
| 12 | 4096 |
| 13 | 8192 |

</td>
</tr>
</table>

“输出大小”属性使用&#x200B;*对数步骤*&#x200B;轻松映射2的幂次增加（例如，256、512、1024...） 到&#x200B;*线性比例*（例如8， 9， 10，...）。 这意味着将X或Y中的输出大小值增大或减小1相当于将当前分辨率乘以或除以2。

当“输出大小”值由[函数](../../function-graphs/function-graphs.md)控制时，此情况也适用，函数应输出目标对数值（相对或绝对）而不是目标分辨率。

>[!IMPORTANT]
>
> X和Y的分辨率增大或减小会将像素计数乘以或除以&#x200B;*4*，这将对图形的&#x200B;*性能*&#x200B;和&#x200B;*内存空间*&#x200B;产生重大影响。\
> 因此，我们强烈建议使用实际需要的&#x200B;*最低分辨率*&#x200B;来获得所需的结果。 将分辨率置于控制之下是我们的[性能优化准则](../../best-practices/performance-optimization/performance-optimization-guidelines.md)之一。

>[!NOTE]
>
> 在[函数图表](../../function-graphs/function-graphs.md)中，`$size`和`$sizelog2` [系统变量](../../function-graphs/variables/system-variables/system-variables.md)分别返回与节点或图表的当前分辨率匹配的Float2值作为两个的原始像素计数或幂数。\
> 例如，对于1024\*512图像，`$size`返回`(1024,512)`，而`$sizelog2`返回`(10,9)`。

## 相对大小

当Output Size属性使用&#x200B;*“相对于……”*[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)时，其值表示为修饰符&#x200B;*，相对于继承的对数值*。

在对数范围内，相对于继承分辨率的修饰符范围为–12至+12，默认值为0。 这意味着上述或以下每一步都会导致分辨率增加一倍或减半。 右侧的表格提供了继承值9（即，512 = 2^9）和11（即，2048 = 2^11）在一个维中相对分辨率如何变化的示例：

请注意，高于8196时，大小为&#x200B;*上限*。 此端点受[首选项](../../interface/preferences-window/preferences-window.md)的<b>常规</b>部分中的<b>烹饪大小限制</b>设置控制。 请注意，如果分辨率非常大，则性能成本成比例，内存占用也呈指数级增长。 此外，图形处理中的限制会对纹理的最大大小施加硬限制。

| -5 | -4 | -3 | -2 | -1 | 0 | +1 | +2 | +3 | +4 | +5 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 16 | 32 | 64 | 128 | 256 | <b>512</b> | 1024 | 2048 | 4096 | 8196 | 8196 |
| 64 | 128 | 256 | 512 | 1024 | <b>2048</b> | 4096 | 8196 | 8196 | 8196 | 8196 |

>[!NOTE]
>
> 低于16的分辨率&#x200B;*未*&#x200B;受限制，但建议不要降低，因为低于该阈值没有性能提升。 相反，由于<b>Substance引擎</b>的特定实现，性能实际上会&#x200B;*下降*。 因此，在Substance图中使用16x16作为一般的最小分辨率。

## 更改继承方法

大多数情况下，输出大小属性的默认[继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)如下所示，具体取决于项目：

* 图形： *相对于主页*
* 节点： *相对于输入* — 在此情况下使用由节点的[主输入](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)继承的值
* [位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点： *绝对* — 请参阅[位图资源](../../resources/bitmap-resource/bitmap-resource.md)页面和[性能优化准则](../../best-practices/performance-optimization/performance-optimization-guidelines.md)以了解原因

单击节点或图形的属性，然后在[属性](../../interface/properties/properties.md)面板中的<b>基本参数</b>部分中找到<b>输出大小</b>属性。 单击继承方法下拉菜单，选择所需的继承方法。

![输出大小继承方法](output-size.resources/output-size-02.gif "输出大小继承方法"){width="512px"}

## 示例问题

如果您是新的[Adobe Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)用户，则可能会遇到一些常见问题。 我们将在下面列出一些示例以及解决方案。

+++问题1
**![（错误）](output-size.resources/error.svg)问题**

![示例问题1](output-size.resources/output-size-03.png "示例问题1")



**主页大小**&#x200B;设置为&#x200B;*灰显*，图形以不需要的256\*256分辨率使用。

在图表的属性中，输出大小属性的继承方法设置为&#x200B;*绝对*，这将停止继承，而采用任意值。

**![（刻度）](output-size.resources/check.svg)解决方案**

![示例问题1解决方案](output-size.resources/output-size-04.png "示例问题1解决方案")



将图形输出大小的继承方法设置为&#x200B;*相对于父级*。

+++

+++问题2
**![（错误）](output-size.resources/error.svg)问题**

![示例问题2](output-size.resources/output-size-05.png "示例问题2")



在上面您看到的情况是，尽管图形被设置为&#x200B;*相对于主页*，但图形的输出导致的分辨率(512\*512)不同于主页中的设置(1024\*1024)。

此问题源于[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点。 它默认为&#x200B;*Absolute*&#x200B;继承方法，并基于[位图资源](../../resources/bitmap-resource/bitmap-resource.md)选择512\*512作为分辨率。 与其连接的节点设置为&#x200B;*相对于输入*，因此从Bitmap节点继承其“输出大小”。

**![（刻度）](output-size.resources/check.svg)解决方案**

![示例问题2解决方案](output-size.resources/output-size-06.png "示例问题2解决方案")



将Bitmap节点的输出大小的继承方法设置为&#x200B;*相对于父级*，从而进一步解决链中下游的问题。

+++

+++问题3
**![（错误）](output-size.resources/error.svg)问题**

![示例问题3](output-size.resources/output-size-07.png "示例问题3")



在上面您会看到一个问题，即分辨率在链的中间跳跃得很高，导致输出分辨率比父级定义的分辨率高得多。

此问题是由[变换2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)节点上的相对修饰符3引起的，使输出增大8倍。

**![（刻度）](output-size.resources/check.svg)解决方案**

![示例问题3解决方案](output-size.resources/output-size-08.png "示例问题3解决方案")



将“宽度”和“Height”的相对修饰符设置为0，以便不进行放大。

+++
