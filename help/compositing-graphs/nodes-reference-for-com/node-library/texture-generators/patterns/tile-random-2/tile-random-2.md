---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: 使用“拼贴随机2”节点，在Substance 3D Designer中使用高级变化控件创建随机拼贴图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 平铺随机2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---


# 平铺随机2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random-2.resources/tilerandom2.jpg){width="200px"}

<b>英寸：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

**拼贴随机2**&#x200B;节点生成随机大小和Height与宽度比的相邻拼贴。

网格可以通过随机&#x200B;*倾斜*&#x200B;形状的两侧来调整以断开角度。

可以使用&#x200B;*缩放*、*斜切*、*圆角化*&#x200B;以及&#x200B;*扭曲旋转*&#x200B;的选项调整形状。

这些调整可以由&#x200B;*输入映射*&#x200B;控制。

专用输出允许您将形状的&#x200B;**UV**&#x200B;输入到&#x200B;**Flood Fill(...)**&#x200B;中 用于应用其他变体的节点。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>随机大小映射</b> <i>灰度</i> | 灰度输入图像，控制形状的随机比例。<br><br>其影响由<b>随机大小输入图乘数</b>参数控制。 |
| <b>随机倾斜映射</b> <i>灰度</i> | 控制形状随机倾斜的灰度输入图像。<br><br>其影响由<b>随机倾斜输入图乘数</b>参数控制。 |
| <b>圆角半径映射</b> <i>灰度</i> | 灰度输入图像，用于控制形状的圆角半径。<br><br>其影响由<b>圆角半径输入图Mult</b>控制。 参数。 |
| <b>斜角距离图</b> <i>灰度</i> | 控制形状斜角的灰度输入图像。<br><br>其影响由<b>斜面距离输入图Mult控制。</b> 参数。 |
| <b>蒙版图</b> <i>灰度</i> | 控制形状蒙版的灰度输入图像。<br><br>其影响由<b>蒙版映射输入开始</b>和<b>蒙版映射输入结束</b>参数控制。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>数量X</b> <i>整数</i> | <b>X</b>轴上的单元格数。 |
| <b>数量Y</b> <i>整数</i> | <b>Y</b>轴上的单元格数。 |
| <b>大小</b> |  |
| <b>随机大小乘数</b> <i>浮动</i> | 将<i>全局</i>调整应用于随机缩放的强度。 |
| <b>随机大小输入图乘数</b> <i>浮动</i> | 使用从<b>随机大小映射</b>输入值<i>采样</i>调整随机缩放的强度。 |
| <b>随机大小X</b> <i>浮动</i> | 调整<b>X</b>轴<i>仅</i>上的随机缩放强度。 |
| <b>随机大小Y</b> <i>浮动</i> | 调整<b>Y</b>轴<i>仅</i>上的随机缩放强度。 |
| <b>随机大小分布</b> <i>整数</i> | 控制分布随机缩放值的方法： <br><br>- <i>一致</i>：对所有单元格以<i>相同方式</i>应用随机缩放<br>- <i>蓝色噪声</i>：使用蓝色噪声模式<i>调整随机缩放</i> |
| <b>形状长宽比 — 变换</b> |  |
| <b>间隙Thickness</b> <i>浮动</i> | 调整形状之间间隙的Thickness。 所有</i>形状的<i>相等。 |
| <b>随机位置乘数</b> <i>浮动</i> | 将随机位置偏移应用于形状，直至<i>符合其单元格的边框</i>。 |
| <b>圆角半径</b> <i>浮动</i> | 调整形状圆角的<i>半径</i>。 值<b>0</b>表示不应用舍入。<br><br><i>注意</i>：当<b>启用每个轴斜角控制</b>参数设置为<i>True</i>时，无法应用此效果。 |
| <b>圆角半径输入映射多项式。</b> <i>浮动</i> | 调整<b>圆角半径映射</b>输入图影响圆角半径的强度。<br><br>映射作为<b>圆角半径</b>参数的<i>每像素</i>乘数。<br><br><i>注意</i>：当<b>启用每轴斜角控制</b>参数设置为<i>True</i>时，无法应用此效果。 |
| <b>缩放乘数</b> <i>浮动</i> | 按其单元格</i>的<i>区域比例调整每个形状的大小。 |
| <b>随机缩放</b> <i>浮动</i> | 调整将随机缩放应用于<i>每个</i>形状的强度。 |
| <b>旋转</b> <i>浮动</i> | 通过沿单元格边框将每个<i>角</i>移动到其<i>邻居</i>，旋转单元格中的形状。<br><br>此方法导致对旋转处的形状应用某些<i>扭曲</i>和<i>缩放</i>。 |
| <b>旋转随机</b> <i>浮动</i> | 调整将随机数量的旋转应用于每个形状的强度。<br><br>旋转方法在<b>旋转</b>参数中描述。 |
| <b>角位置随机</b> <i>浮动</i> | 通过在单元格边框上对其每个<i>角</i>应用随机数量<i>偏移</i>来扭曲形状。 |
| <b>倾斜</b> |  |
| <b>随机倾斜乘数</b> <i>浮动</i> | 将<i>全局</i>调整应用于随机倾斜的强度。 |
| <b>随机倾斜输入图乘数</b> <i>浮动</i> | 使用从<b>随机倾斜映射</b>输入值<i>取样</i>调整随机倾斜的强度。 |
| <b>随机倾斜X</b> <i>浮动</i> | 调整<b>X</b>轴<i>仅</i>上的随机倾斜强度。 |
| <b>随机倾斜Y</b> <i>浮动</i> | 调整<b>Y</b>轴<i>仅</i>上的随机倾斜强度。 |
| <b>随机倾斜分布</b> <i>整数</i> | 控制分布随机倾斜值的方法： <br><br>- <i>一致</i>：随机倾斜以<i>相同方式</i>应用于所有单元格<br>- <i>蓝色噪声</i>：随机倾斜是使用蓝色噪声模式<i>调整的</i> |
| <b>斜面</b> |  |
| <b>斜面距离模式</b> <i>整数</i> | 设置<i>获取形状应有斜角的距离</i>的方法：<br><br>-<i>相对于网格大小</i>：形状按指定的<i>网格大小比例进行斜角</i><br>-<i>相对于形状大小</i>：形状按指定的<i>大小比例进行斜角</i><br>-<i>相对于图像大小</i>：形状按指定的<i>图像比例</i>进行斜角 |
| <b>斜距乘数</b> <i>浮动</i> | 将<i>全局</i>调整应用于斜面距离。 |
| <b>斜距输入映射多项式。</b> <i>浮动</i> | 使用<b>斜角距离图</b>输入映射作为<i>每像素</i>乘数调整斜角的距离。 |
| <b>斜角圆曲线</b> <i>浮动</i> | 调整应用于斜角的圆角强度，使其更为<i>凸起</i>。 |
| <b>启用每个轴斜角控件</b> <i>布尔值</i> | 当<i>True</i>时，可以在<b>X</b>和<b>Y</b>轴上<i>分别</i>应用和调整斜角。<br><br><i>注意</i>：此<i>取消</i><b>圆角</b>效果。 |
| <b>斜面距离X</b> <i>浮动</i> | 仅调整<b>X</b>轴<i></i>上的斜面距离。 此距离取决于<b>斜面距离模式</b>参数的值。<br><br><i>注意</i>：仅当<b>启用每轴斜面控制</b>参数设置为<i>True</i>时，此参数才可用。 |
| <b>斜面距离Y</b> <i>浮动</i> | 调整<b>Y</b>轴<i>仅</i>上的斜面距离。 此距离取决于<b>斜面距离模式</b>参数的值。<br><br><i>注意</i>：仅当<b>启用每轴斜面控制</b>参数设置为<i>True</i>时，此参数才可用。 |
| <b>蒙版</b> |  |
| <b>蒙版随机反转</b> <i>布尔值</i> | 反转形状的随机蒙版。 |
| <b>蒙版随机起始</b> <i>浮动</i> | 对于给定的<b>随机植入</b>，伪随机蒙版按照从起始形状到结束形状的<i>特定顺序</i>应用。 此参数允许您<i>偏移<i>起始</i>形状的索引</i>。<br><br><i>注意</i>：此参数确定蒙版的<i>值范围</i>的一个限制。 因此，该值可能比<b>掩码随机结束</b>值<i>大</i>。 |
| <b>蒙版随机结束</b> <i>浮动</i> | 对于给定的<b>随机植入</b>，伪随机蒙版按照从起始形状到结束形状的<i>特定顺序</i>应用。 此参数允许您<i>偏移<i>结束</i>形状的索引</i>。<br><br><i>注意</i>：此参数确定蒙版的<i>值范围</i>的一个限制。 因此，该值可能比<b>掩码随机起始</b>值<i>大</i>。 |
| <b>按单元格区域进行蒙版反转</b> <i>布尔值</i> | 按形状单元格的区域反转形状蒙版。 |
| <b>按单元格区域开始蒙版</b> <i>浮动</i> | 调整蒙版形状的<i>最小值</i>单元格的区域阈值。<br><br><i>注意</i>：这将确定蒙版的<i>值范围</i>的一个限制。 因此，该值可能比<b>按单元格区域结束蒙版</b>的值大<i></i>。 |
| <b>按单元格区域结束设置蒙版</b> <i>浮动</i> | 调整蒙版形状的<i>最大</i>单元格的区域阈值。<br><br><i>注意</i>：这确定了蒙版的<i>值范围</i>的一个限制。 因此，该值可能比<b>按单元格区域蒙版起始</b>值<i>低</i>。 |
| <b>蒙版映射输入反转</b> <i>布尔值</i> | 通过<b>蒙版映射</b>输入图反转形状的蒙版。 |
| <b>蒙版映射输入开始</b> <i>浮动</i> | 调整蒙版形状在<b>蒙版映射</b>输入图中的<i>最小灰度值</i>阈值。<br><br><i>注意</i>：这将确定蒙版的<i>值范围</i>的一个限制。 因此，该值可能比<b>掩码映射输入端</b>值<i>大</i>。 |
| <b>蒙版映射输入端</b> <i>浮动</i> | 调整蒙版形状在<b>蒙版映射</b>输入图中的<i>最大灰度值</i>阈值。<br><br><i>注意</i>：这将确定蒙版的<i>值范围</i>的一个限制。 因此，该值可能比<b>蒙版映射输入开始</b>值<i>低</i>。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-inputs.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-demo.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-demo2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-node.png" />
        </td>
    </tr>
</table>
