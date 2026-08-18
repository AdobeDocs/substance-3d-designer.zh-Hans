---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-color.html"
breadcrumb-title: ''
description: 使用“扩散颜色”节点可应用颜色扩散效果，以创建平滑的颜色混合和过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 扩散颜色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 3%

---


# 扩散颜色

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-icon.png){width="200px"}

**范围：** *滤镜/效果*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

根据提供的&#x200B;**蒙版**&#x200B;图像输入对&#x200B;**源**&#x200B;图像输入中的颜色应用扩散过程，在使用[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)时创建平滑的颜色渐变。

只有来自与蒙版匹配的像素的颜色会被扩散；其他像素不会参与结果。

</td>
</tr>
</table>

## 参数

* **迭代**： *0.0 - 64.0*&#x200B;要执行的扩散迭代次数（越高越好，但速度越慢）。 有用的值在[8， 48]范围内。\
  请注意，如果您不寻求数学正确性，则低值会更优秀。\
  **距离**： **0.0 - 1.0**&#x200B;调整扩散的最大距离。
* **启用抖动**： *True/False*&#x200B;控制每个传递的采样方法。 抖动允许以较少的次数收敛，但会引入杂色。\
  没有它，每个刀路速度更快，但需要更多刀路才能获得平滑的结果而不会出现带状伪影。
* **是正常映射**： *True/False*&#x200B;在每个步骤对值添加规范化。
* **将Alpha用作蒙版**： *True/False*&#x200B;将&#x200B;*源*&#x200B;输入的Alpha通道用作扩散蒙版，而不是&#x200B;*蒙版*&#x200B;输入。

## 输入

* **源** *颜色*\
  要扩散的图像。
* **蒙版** *灰度*\
  扩散蒙版：白色像素在&#x200B;*源*&#x200B;中取样，并以黑色像素扩散。 图像应该是黑白的。 如果蒙版包含渐变，则截止值为0.5。
* **强度** *灰度*\
  局部定义扩散过程应用的强度。 此地图应该为&#x200B;*对比图*，才能产生显着的效果。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-02a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-02b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after-1.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after-1.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-normal.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-normal-render.jpg){width="512px"}

</td>
</tr>
</table>
