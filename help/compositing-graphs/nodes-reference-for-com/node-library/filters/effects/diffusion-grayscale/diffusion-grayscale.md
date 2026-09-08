---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: 使用“漫射灰度”节点可应用灰度漫射效果，以创建平滑的颜色过渡和混合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 漫射灰度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# 漫射灰度

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-icon.png){width="200px"}

**范围：** *滤镜/效果*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

根据提供的&#x200B;**蒙版**&#x200B;图像输入，将漫射过程应用于&#x200B;**源**&#x200B;图像输入中的值，在值之间创建平滑渐变。

只有来自与蒙版匹配的像素的值会被扩散；其他像素不会参与结果。

</td>
</tr>
</table>

## 参数

* **迭代**： *0.0 - 64.0*&#x200B;要执行的漫射迭代数（越高越好，但速度越慢）。 有用的值在[8， 48]范围内。\
  请注意，如果您不寻求数学正确性，则低值会更优秀。\
  **距离**： **0.0 - 1.0**&#x200B;调整漫射的最大距离。
* **启用仿色**： *True/False*&#x200B;控制每个传递的采样方法。 仿色允许以较少的遍数收敛，但引入了噪声。\
  没有它，每个刀路速度更快，但需要更多刀路才能获得平滑的结果而不会出现带状伪影。

## 输入

* **源** *灰度*\
  要扩散的图像。
* **蒙版** *灰度*\
  漫射蒙版：白色像素在&#x200B;*源*&#x200B;中取样，并以黑色像素扩散。 图像应该是黑白的。 如果蒙版包含渐变，则截止值为0.5。
* **强度** *灰度*\
  在本地定义漫射过程应用的强度。 此地图应该为&#x200B;*对比图*，才能产生显着的效果。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-render.jpg){width="512px"}

</td>
</tr>
</table>
