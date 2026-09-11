---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: 了解减小Substance图形文件大小以优化性能和存储要求的准则。
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 文件大小减少准则
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# 概述

在某些情况下，[Substance 3D资源(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)的总文件大小可能是一个重要因素。 此页面介绍了在尝试减小文件大小时要牢记的一些关键区域和设置。

文件大小主要由[嵌入的位图](../../resources/bitmap-resource/bitmap-resource.md)决定。 它们是链接、嵌入或烘焙的文件，并作为资源添加到[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)文件(SBS)中。 只有图形中使用的位图（即直接或通过节点链连接到输出）才会发布在Substance 3D资源中。 在Substance 3D文件中，位图对文件大小没有影响，因为所有位图资源仍存储在文件之外。

>[!IMPORTANT]
>
> 确保所有[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点的[输出大小](../../compositing-graphs/output-size/output-size.md)属性都设置为&#x200B;*绝对* [继承方法](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)。 否则，它们引用的[位图资源](../../resources/bitmap-resource/bitmap-resource.md)将以默认的256\*256分辨率保存在已发布的Substance 3D资源文件中，这将会*&#x200B;影响一个或多个输出的质量*。

## 文件大小因子

影响SBSAR总文件大小的因素有很多。 下面列出了它们的简要说明。

+++解决方法
显然效果很大。 请尽可能使用最小的分辨率，同时记住，您可能也希望Substance文件能够以大分辨率工作。 您可以使用标准分辨率蒙版技巧来使较小的位图看起来更大。

*在以下位置找到：外部软件，或在Designer中导入/重新导出位图。*

+++

+++文件颜色模式
如果在导出之前在“图像编辑器”中进行设置，则颜色模式在使用Raw位图格式时也会影响文件大小。 仅灰度位图比RGB(A)图像小。

*在以下位置找到：外部软件，或者在正确设置[输出节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)时在Designer中导入/重新导出位图。*

+++

+++文件格式
图像的文件格式不同，但有些情况下可以忽略它。 像Photoshop这样的程序可以对JPG压缩实现略微更多的控制，并且有时可以提供一条不错的中间道路。

*在以下位置找到：外部软件，或在Designer中导入/重新导出位图。*

+++

+++图形中的使用情况
将“位图”节点设置为哪种模式也会影响Designer压缩文件的方式，因为在图形中使用灰度模式文件作为彩色位图会产生更大的文件。 确保正确设置这些项！

*在以下位置找到：[位图节点属性。](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++包中的位图格式
在“资源”属性上，您可以在“Raw”和“Jpeg”压缩之间进行选择。 这可能对最终结果产生相当大的影响。

*在：通过资源管理器窗口找到的位图资源属性。*

+++

+++包中的位图压缩品质
使用“Jpeg”位图格式时，下面的滑块可能会影响品质和文件大小。 此滑块的行为不是非常可预测，但1通常对应于最高质量的JPG压缩，0.5通常提供最小的大小。

*在：通过资源管理器窗口找到的位图资源属性。*

+++

+++发布时的压缩模式
在发布到SBSAR时，可以在压缩时选择“自动”、“最佳”和“无”，如果使用“原始”位图格式，这些选项可能会产生相当大的差异。 对出口速度也有很大影响。 通常不建议使用“无”，因为它不能提高质量。

*在以下位置找到： SBSAR包的最终发布设置。*

+++

## 文件大小比较

下表显示了所有设置彼此的影响。 使用的位图是生成的噪声的4096x4096图像，从Photoshop导出为24位TGA或JPG，品质为8。 TGA也导出为灰度和RGBA模式。

该图形仅放置连接到单个输出的单个位图节点。 位图模式根据源文件模式进行设置。

虽然右侧的表格不能提供完整的结论，但在比较视觉结果和文件大小时可以了解以下内容：

* “原始位图+压缩”能够以可接受的文件大小提供最佳的品质。
* 预压缩的源文件在大多数情况下可以减小文件大小，但代价是高质量的。
* 使用JPG包格式时，文件大小最小，但质量最差，为0.5。
* 灰度并非总是小于文件大小，但在类似设置下将具有比颜色更高的品质。

>[!NOTE]
>
> **Jpeg位图格式**
> 
> 请务必注意，要求高精确度的特殊地图（如法线图、矢量地图等）可能不应设置为Jpeg压缩，因为这会导致更明显的伪影！

| 源图像 | 彩色TGA | 彩色JPG | 灰度TGA | 灰度JPG |
| --- | --- | --- | --- | --- |
| <b>原始位图格式</b>压缩模式： *无* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>原始位图格式</b>压缩模式： *最佳* | 9.11 MB | 3.37 MB | 5.06 MB | 4.75 MB |
| <b>Jpeg位图格式</b>压缩质量： *1* | 5.09 MB | 1.94 MB | 6.30 MB | 2.49 MB |
| <b>Jpeg位图格式</b>压缩质量： *0.5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>Jpeg位图格式</b>压缩质量： *0* | 407 KB | 433 KB | 990 KB | 808 KB |
