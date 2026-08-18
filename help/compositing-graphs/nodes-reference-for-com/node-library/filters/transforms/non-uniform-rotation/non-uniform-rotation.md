---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: 使用“非均匀旋转”节点应用非均匀旋转变换，以创建螺旋和涡旋效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均匀旋转
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 非均匀旋转

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**英寸：**&#x200B;滤镜*/变换*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**非均匀旋转**&#x200B;节点使用&#x200B;**旋转贴图**&#x200B;输入旋转&#x200B;**输入**。

图像的值表示&#x200B;*个循环*。 围绕&#x200B;**中心点位置**&#x200B;值或&#x200B;**中心点位置映射**&#x200B;输入指定的位置执行旋转。\
**旋转贴图**&#x200B;输入中的正值导致&#x200B;*顺时针*&#x200B;旋转。

</td>
</tr>
</table>

## 参数

### 输入

* **输入** *灰度/颜色*\
  应旋转的输入灰度图像。
* **旋转贴图***灰度*&#x200B;用于控制旋转量的映射，以&#x200B;*轮转次数*&#x200B;为单位。 采样值与&#x200B;**旋转角度乘数**&#x200B;相乘。 负值会导致&#x200B;*逆时针*&#x200B;旋转。
* **旋转中心点位置映射** *颜色*\
  此图像用于指定旋转&#x200B;*透视*&#x200B;的位置。 **X/Y**&#x200B;位置映射到图像的&#x200B;**R/G**&#x200B;通道。

### 参数

* **旋转角度乘数** *浮点*\
  调整&#x200B;**旋转贴图**&#x200B;输入的强度。
* **旋转角度偏移** *浮动*\
  应用指定的额外旋转量。
* **使用中心点位置映射** *布尔值*\
  使用&#x200B;*位图输入*&#x200B;指定旋转透视点的位置。 **X/Y**&#x200B;位置映射到&#x200B;**位置映射**&#x200B;输入的&#x200B;**R/G**&#x200B;通道。
* **中心点位置** *浮点2*\
  图像围绕其旋转的枢轴的位置。
* **背景颜色** *浮动/浮动4*\
  背景色，用于在拼贴未设置为&#x200B;**H和V拼贴**&#x200B;时显示图像边界&#x200B;*外部*&#x200B;的颜色。
* **筛选模式** *整数*\
  定义在像素之间&#x200B;*插值*&#x200B;时如何处理取样结果：
  * *最接近的*：将对&#x200B;*相同的*&#x200B;值取样（较快）
  * *双线性*：将在结果上应用双线性滤镜，以实现&#x200B;*更平滑*&#x200B;的外观

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
