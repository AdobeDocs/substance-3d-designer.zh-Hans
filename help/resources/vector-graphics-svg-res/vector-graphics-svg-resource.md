---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: 在Substance 3D Designer中导入SVG矢量图形并将其用作创建程序性素材的资源。
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 矢量图形 (SVG) 资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 2%

---


# 矢量图形 (SVG) 资源

Substance 3D Designer通过可缩放矢量图形格式支持有限形式的矢量图形。 SVG文件可按不同方式作为资源引入，以用作图表的资源。

SVG文件[可以通过原子SVG节点创建或编辑，](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)它们也可以由[UV到SVG烘焙器创建。](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)

>[!NOTE]
>
> 当前不支持Adobe Illustrator (**.ai**)文件&#x200B;*不*。

## SVG存储

SVG存储空间取决于它们是链接的还是导入的。 导入的SVG文件将嵌入到SBS文件中，要求[没有外部文件（如位图）](../../resources/bitmap-resource/bitmap-resource.md)，并且可以使用[矢量编辑工具](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)进行编辑。

## SVG属性

包中的SVG资源具有许多可以自定义的属性。 大多数属性没有主要用途，用于库滤镜，但少数会影响渲染质量。

| 属性名称 | 目的 |
| --- | --- |
| 标识符 | 用于引用包中的SVG资源，必须是唯一的。 |
| 文件路径 | 资源引用的SVG文件的磁盘路径。 |
| 描述 | 此资源的[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)和[库](../../interface/the-library/the-library.md)工具提示中显示的说明。 |
| 类别 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 标签 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 作者 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 作者 URL | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 标记 | 用于[&#128279;](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)排序和整理[库](../../interface/the-library/the-library.md)中的资源。 |
| 用户数据 | 可选的额外数据，不适用于矢量图形。 |
| 在图库中显示 | 确定SVG资源是否应在[库视图](../../interface/the-library/the-library.md)中隐藏。 |
| 矢量图形质量 | 影响渲染品质。 此范围不是线性的，在0.5时达到最佳质量。 |

## SVG创作

由于仅支持一组有限的功能，因此创作SVG受到限制。

一般来说，以下条件成立：

* 仅保证简单的原始形状和路径能够正确绘制；
* 支持描边，但仅会导致1像素宽的描边，并且忽略描边样式；
* 虚线样式一定会断开；
* 文本需要转换为要渲染的路径/轮廓；
* 不支持[复合路径](https://helpx.adobe.com/ie/illustrator/using/combining-objects.html#compound_paths)；
* 不支持渐变等高级功能；
* 不支持CSS属性的样式元素。

## 建议的导出选项

每个应用程序的导出选项略有不同：

### Adobe Illustrator

如果您注意以下选项，[Illustrator](https://www.adobe.com/products/illustrator.html)允许对您的SVG导出进行最大程度的控制。

* 仅使用<b>“另存为”</b>，*“不”*“导出为”！
* <b>SVG配置文件</b>无关紧要，但Tiny配置文件将（大部分）默认为绝对正确的设置；
* <b>字体</b>必须设置为<b>转换为轮廓</b>才能生效；
* <b>CSS属性</b>应&#x200B;*不*&#x200B;设置为样式元素，所有其他选项都将有效；
* 取消选中<b>保留Illustrator编辑功能</b>；
* 取消选中<b>响应</b>；
* 描边将无法正常工作，请使用<b>对象>路径>轮廓化描边</b>来显示它们。

右侧的图像演示了推荐的导出选项，单击它可显示全尺寸。

>[!IMPORTANT]
>
> 画板可能会影响生成的SVG文件的结果。 某些Illustrator文件模板引入了多个画板。\
> 尝试仅保留一个已正确裁剪的画板，并在另存为SVG时在“画板”窗口中选择它。

![SVG导出选项](../../assets/svg-export-options-ai.jpg "IllustratorSVG导出选项"){width="512px"}

### Inkscape

Inkscape可本机存储为SVG，但对文件格式的控制较少。 Inkscape文件将主要在应用程序中本地运行，但存在一些限制：

* 在Substance 3D Designer中，描边仅以1px宽度显示，使用<b>路径>描边到路径</b>可使描边正常工作，
* 文本将不起作用，请使用<b>路径>对象到路径</b>来获取要使用的文本。

### Adobe Photoshop

Photoshop的SVG导出器非常有限（<b>文件>导出>导出为……</b>） 当前无法为Substance 3D Designer生成正确的结果。 您可以获取形状和路径信息，但样式始终保存为Elements，这样不兼容。

它可用于简单的黑白形状蒙版，解决方法是使用[Alpha拆分](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)从SVG提取Alpha。

或者，也可以将Photoshop导出的SVG[导入](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)，这样您就可以[在应用程序内本地编辑样式信息。](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)
