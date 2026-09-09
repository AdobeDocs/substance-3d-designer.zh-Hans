---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: 使用Extend Shape节点将形状扩展至其边界之外，以创建扩展的蒙版和图案效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>Extend Shape</b>节点将<b>输入</b>的<i>节</i>延伸至设定的方向和距离。

使用<b>Show helper</b>参数可以可视化扩展部分和扩展方向。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>模式</b> <i>整数</i> | 定义用于应用扩展的<i>参数</i>： <b>扩展位置</b>和<b>扩展角度</b>指定的<b>输入</b>部分在<b>扩展距离</b>上沿<i>相反方向</i><br>- <i>单向</i>延伸： <b>扩展位置</b>和<b>扩展指定的<b>输入</b>部分角度</b>沿<i>单向</i><br>- <i>开始/结束位置</i>延伸<b>延伸距离</b>：延伸<i>矢量</i>由<b>开始位置</b>和<b>结束位置</b>定义。 <br><br><i></i><b>开始位置</b>处<b>输入</b>的<i>垂直</i>部分在<i>上在此矢量</i>上扩展到<b>结束位置</b> |
| <b>扩展距离</b> <i>浮动</i> | 由<b>扩展位置</b>和<b>扩展角度</b>指定的部分应扩展到的距离。 距离以图像范围的<i>比例</i>表示。 |
| <b>扩展位置</b> <i>浮动</i> | 应延伸的截面在图像中的位置。 该值表示为距中心</i>的<i>偏移。 |
| <b>扩展角度</b> <i>浮动</i> | 考虑到起始点为<i>垂直截面</i>，应扩展的截面的角度。 |
| <b>起始位置</b> <i>浮点2</i> | <i>扩展矢量</i>的开始位置。 |
| <b>结束位置</b> <i>浮点2</i> | <i>扩展矢量</i>的结束位置。 |
| <b>开始明亮度偏移</b> <i>浮动</i> | 将明亮度偏移应用于扩展部分<i></i>之前的图像区域。 此明亮度偏移是沿节</i>向节之后的图像区域明亮度插入的<i>。<br><br><i>注意</i>：此参数仅在节点的<b>灰度</b>版本中可用。 |
| <b>结束明亮度偏移</b> <i>浮动</i> | 将明亮度偏移应用于扩展部分<i>之后</i>的图像区域。 此明亮度偏移是沿节</i>向节前图像区域的明亮度插入的<i>。<br><br><i>注意</i>：此参数仅在节点的<b>灰度</b>版本中可用。 |
| <b>亮度。 偏移忽略黑色像素</b> <i>布尔值</i> | 设置为<i>True</i>时，在<i>both</i>中指定的明亮度偏移 <b>开始明亮度偏移</b>和<b>结束明亮度偏移</b>仅应用于<i>非黑色</i>像素，即值大于0的像素。<br><br><i>注意</i>：此参数仅在节点的<b>灰度</b>版本中可用。 |
| <b>筛选模式</b> <i>整数</i> | 定义在像素<br><br>- <i>最近的</i>：之间<i>插值</i>时如何处理采样结果：将对完全相同的<i>相同</i>值（更快）<br>- <i>双线性</i>：对结果应用双线性的滤镜以获得<i>更平滑</i>的外观 |
| <b>显示助手</b> <i>布尔值</i> | 将<i>扩展部分</i>显示为叠加，箭头显示扩展的<i>方向</i>。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-node.png" />
        </td>
    </tr>
</table>
