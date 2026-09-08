---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: 使用“皮革风化”节点，根据网格曲率为皮革材料添加磨损图案和老化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 皮革风化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 9%

---


# 皮革风化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

<b>在</b>中基于网格的生成器>风化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这是一种同时适用于多个通道的完全素材效果。 它增加了皮革的随机磨损效果，同时控制了年龄和污浊度。 它类似于[织物风化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)，但专门针对皮革进行调整。<br>除非插入适当的烘焙AO和世界空间正常映射，否则此效果不会非常好，因为它需要这些组件来充分计算和生成所有内容。

在使用完整素材时，请确保完全了解[链接创建模式](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 |
| <b>普通Wold空间</b> <i>颜色输入</i> |  |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“Mask”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>频道</b> | 在此组中打开和关闭素材通道，例如，在使用“Specular/光泽度”映射而非“金属/粗糙度”时。 |
| <b>高级</b> |  |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同正常映射格式之间切换（反转绿色通道）。 |
| <b>蒙版</b> <i>False/True</i> | 启用或禁用蒙版图。 |
| <b>效果</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> | 根据世界空间正常映射中朝上的区域，混合在较暗的Dust效果中。 |
| <b>污迹</b> <i>0.0 - 1.0</i> | 全球Dirt/涂抹效果中的混合，主要基于AO中遮挡的（深色）区域。 |
| <b>边缘磨损</b> <i>0.0 - 1.0</i> | 根据“材料正常”为边缘添加锐化/增强效果。 |
| <b>已使用</b> <i>0.0 - 1.0</i> | 混合在全球各地都穿着破旧的皮革外表。 |
| <b>年龄</b> <i>0.0 - 1.0</i> | 穿着破旧的皮革外表的混合会根据AO而折叠。 职位安排受年龄限制的影响很大。 |
| <b>年龄阈值</b> <i>0.0 - 1.0</i> | 设置年龄效果的外观阈值。 |
| <b>裂缝比例</b> <i>1.0 - 16.0</i> | 设置旧皮革和旧皮革效果中的深度。 |
| <b>裂缝变形强度</b> <i>0.0 - 1.0</i> | 从“已使用”和“年龄”效果中设置磨损皮革的强度。 |
| <b>锐边Scratches缩放</b> <i>1.0 - 32.0</i> |  |
| <b>锐边Scratches变形强度</b> <i>0.0 - 1.0</i> |  |
| <b>使用的皮革去饱和度</b> <i>0.0 - 1.0</i> | 设置旧皮革外观和“已使用”效果的饱和度。 |
| <b>使用的皮革亮度</b> <i>0.0 - 1.0</i> | 设置旧皮革外观和“已使用”效果的亮度。 |
| <b>混合</b> |  |
| <b>Diffuse强度</b> <i>0.0 - 1.0</i> | 扩散的混合强度。 |
| <b>Base color强度</b> <i>0.0 - 1.0</i> | 混合基色的强度。 |
| <b>正常强度</b> <i>0.0 - 1.0</i> | 混合“正常”的强度。 |
| <b>Specular强度</b> <i>0.0 - 1.0</i> | 混合Specular的强度。 |
| <b>光泽度强度</b> <i>0.0 - 1.0</i> | 混合光泽度的强度。 |
| <b>粗糙度强度</b> <i>0.0 - 1.0</i> | 混合粗糙度的强度。 |
| <b>Ambient occlusion强度</b> <i>0.0 - 1.0</i> | 混合环境遮蔽的强度。 |
| <b>Height强度</b> <i>0.0 - 1.0</i> | 混合Height的强度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-ex2.png" />
        </td>
    </tr>
</table>
