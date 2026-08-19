---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: 使用“RT辐照度”节点从几何计算实时辐照度信息，以进行真实光照计算。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT辐照度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# RT辐照度

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**范围：** *滤镜/效果*

**复杂**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

在从环境地图和发射地图生成的Height地图输入上生成光线跟踪照度。 可用于将光线“烘焙”到图表内的纹理中。 用于模拟全局照明和光晕。由于计算时间的原因，不应将此节点与CPU (SSE)引擎结合使用。 返回两个映射：一个是辐照度输出，其中辐照度应用于材料输入；一个是仅包含计算出的辐照度值的原始辐照度映射。

</td>
</tr>
</table>

## 参数

### 输入

* **Height：** *灰度输入* Height是素材槽中唯一必需的输入。 没有它，节点将无法正常工作。
* **发射性：***颜色输入*&#x200B;发射性应采用以下格式：纯黑色不发射光，任何其他彩色值发射光。 Alpha将被忽略。 需要连接到此插槽或环境插槽才能看到任何结果。
* **环境**： *颜色输入*\
  用于计算辐照度的HDR光照环境。 需要连接到此插槽或发射插槽才能看到任何结果。

### 参数

* **Height比例**： *0.0 - 1.0*\
  缩放以解释Height。 影响整个场景外观。
* **质量**：*32光线、64光线、128光线*\
  决定结果质量，但也影响性能。 光线越少，噪音越大。
* **计算回弹**： *False/True*\
  切换弹跳计算。 影响质量和速度。
* **环境旋转**： *0.0 - 1.0*\
  围绕旋转环境。
* **环境曝光(EV)**： *-4.0 - 4.0*\
  要用于环境的曝光度值，会影响效果的总亮度。
* **发射强度**： *0.0 - 20.0*\
  发射输入的乘数影响来自发射体的辐射强度。
* **发射色彩空间**： *sRGB，线性*\
  用于解释敏感输入的色彩空间。
* **原始照度Alpha中的IBL阴影**： *False/True*\
  切换是否向照片中添加阴影
* **发射LOD偏差**： *-1.0 - 1.0*&#x200B;调整发射辐照度的质量。 值越低，噪音越大。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
