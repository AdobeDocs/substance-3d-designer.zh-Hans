---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: 使用“MLV灰度模糊”滤镜将运动模糊效果应用于灰度纹理以获得动态外观。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLV灰度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# MLV灰度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV灰度：图标](../../../../../../assets/MLV_Grayscale_Icon.png "MLV灰度：图标")

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

MLV表示<b>“最小方差平均值”</b>。 此滤镜增强图像的边缘并使噪声变得平滑。

此滤镜查找图像中的结构区域，并使用它们来锐化和拼合图像。 在某些情况下，这可能会导致沿比结构区域宽的渐变执行步骤。

</td>
</tr>
</table>

>[!NOTE]
>
> 另请参阅[MLV颜色](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md)。

## 输入连接器

<b>输入&#x200B;</b>*灰度*&#x200B;应处理的灰度图像。

## 输出连接器

<b>输出&#x200B;</b>*灰度*&#x200B;已筛选的灰度图像。

## 参数

<b>强度</b> *Float*&#x200B;应用于图像的筛选强度。\
值越高，细节的平滑程度越高，噪声越平坦。

<b>Smoothness</b> *Float*&#x200B;应用于结构区域的平滑强度，这将使区域变圆，并减小在更高筛选强度下可能出现的步进效果。

<b>条件</b> *整数*&#x200B;用于选择定义图像中结构区域的值的条件。\
换句话说，像素应如何&#x200B;*分组*&#x200B;到应进行平滑处理的区域。\
*— 方差：*&#x200B;选择在平均值周围具有最低色散的值，这将导致像素群集彼此相似\
*— 变异系数：*&#x200B;在考虑到平均值的情况下选择值，这会导致在较亮区域反差较小

<b>高斯</b> *布尔值*&#x200B;使用高斯分布将像素分组到结构区域。\
如果为“True”，则生成更平滑的区域且减少拼合效果。

<b>迭代</b> *整数*&#x200B;筛选器运行的次数，其中每个迭代都应用于前一个规则的结果。\
更多的迭代会产生更平坦、更清晰的区域。

## 示例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant1A.png" alt="mlv_Variant1A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="mlv_Variant2A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>之后</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="mlv_Variant2A">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>之后</i>
    </td>
  </tr>
</table>
