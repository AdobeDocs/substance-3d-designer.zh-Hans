---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: 使用Brick Generator节点创建具有可自定义的大小、偏移和砂浆属性的程序化砖图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 砖块生成器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# 砖块生成器

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## 砖块生成器

**英寸：** *纹理生成器**/Patterns*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

高级砖形图案生成器。 有很多选项可用来专门生成人造砖纹图案

有关更多选项，请参阅[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。

## 参数

* **砖块**： *1 - 64*&#x200B;设置X轴和Y轴中的砖块数量。
* **斜面**： *0.0 - 1.0*&#x200B;更改砖块的斜面配置文件，允许在两个方向更改以及设置衰减配置文件和圆角化。
* **保持比例**： *False/True*&#x200B;使斜面配置文件与砖块大小是否绑定。
* **间隙**： *0.0 - 1.0*&#x200B;砖块之间要留下的间隙。 请记住，斜面还会引入间隙，因此设置斜面意味着您必须对此参数进行补偿。
* **中等大小**： *0.0 - 1.0*&#x200B;砖块图案偏移，每隔一列或一行更改其大小。
* **Height**： *-1.0 - 1.0*&#x200B;修改Height配置文件。 允许引入明亮度变化和各种随机化。
* **斜率**： *-1.0 - 1.0*&#x200B;以每个砖为单位引入斜率，就像某些砖块是倾斜的。
* **偏移**： *0.0 - 1.0*\
  基于行偏移砖块，影响每行的间距。
* **非正方形扩展**： *False/True*\
  启用以非方形比例补偿挤压和拉伸。

## 示例图像

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
