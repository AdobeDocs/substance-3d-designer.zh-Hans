---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: 使用Voronoi节点生成Voronoi图案，用于创建细胞纹理和有机材料效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

**Voronoi**&#x200B;节点使用&#x200B;*Z-down噪声*&#x200B;生成映射到2D图像的3D Voronoi投影。

此节点可以使用[Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

>[!WARNING]
>
> 此噪声仅适用于&#x200B;*GPU引擎*（即&#x200B;**Direct**&#x200B;或&#x200B;**OpenGL**）。 转到&#x200B;**工具>切换引擎……**&#x200B;或按&#x200B;**F9**&#x200B;键以选择所需的引擎。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>反转</b> <i>布尔值</i> | 反转输出图像。 |
| <b>缩放</b> <i>浮动</i> | 控制Voronoi噪声的比例。<br><br>*注意*：在&#x200B;*任何轴*&#x200B;上启用&#x200B;**拼贴**&#x200B;时，比例调整为&#x200B;*stepped*。 这是预期的。 |
| <b>大小</b> <i>浮点3</i> | 控制&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中的Voronoi噪声大小。 非均匀值导致&#x200B;*拉伸或挤压*&#x200B;效果。<br><br>*注意*：在&#x200B;*任何轴*&#x200B;上启用&#x200B;**拼贴**&#x200B;时，大小调整为&#x200B;*步进*。 这是预期的。 |
| <b>偏移</b> <i>浮点3</i> | 将偏移应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中Voronoi噪声的&#x200B;*位置*。 |
| <b>无序</b> <i>浮点3</i> | 应用于&#x200B;**X**、**Y**&#x200B;和&#x200B;**Z**&#x200B;轴中每个噪声点的&#x200B;*随机偏移*&#x200B;的强度。 |
| <b>扭曲强度</b> <i>Float</i> | 控制应用于Voronoi噪声的&#x200B;*变形效果*&#x200B;的强度。 |
| <b>扭曲比例乘数</b> <i>Float</i> | 控制变形效果中使用的&#x200B;*变形图案*&#x200B;的比例，该比例由&#x200B;**扭曲强度**&#x200B;控制。 |
| <b>圆角曲线</b> <i>Float</i> | 围绕噪声的每个点对&#x200B;*斜率*&#x200B;进行圆整，使其成为&#x200B;*凸形*。<br><br>*注意*：当&#x200B;**Style**&#x200B;参数设置为&#x200B;*Edge*&#x200B;时，此参数不可用。 |
| <b>距离刻度</b> <i>Float</i> | 围绕噪声的每个点调整渐变&#x200B;*的*&#x200B;距离。 |
| <b>距离模式</b> <i>整数</i> | 将方法设置为&#x200B;*计算噪声的每个点周围的距离渐变*：<br><br>- *欧几里德*<br>- *曼哈顿*<br>- *切比雪夫*<br>- *明科夫斯基* |
| <b>闵可夫斯基数值</b> <i>Float</i> | Minkowski距离的顺序&#x200B;*p*。 如果将距离渐变划分为几个象限，则此数值将对这些象限产生如下影响： <br><br>- p是&#x200B;*刚好* 1：笔直<br>- p是&#x200B;*低*&#x200B;比1：凹形<br>- p是&#x200B;*大*&#x200B;比1：凸形<br><br>有趣的值：<br><br>- *1.0*：曼哈顿距离<br>- *2.0*：欧几里德距离<br>- *无限远*：切比雪夫distance <br><br>*注意*：此参数仅在&#x200B;**Distance Mode**&#x200B;参数设置为&#x200B;*Minkowski*&#x200B;时可用。 |
| <b>样式</b> <i>整数</i> | 设置Voronoi噪声的方法&#x200B;*渲染数据*，考虑到噪声基于空间中的一组点：<br><br>- *F1*：到空间中&#x200B;*最近点*&#x200B;的距离<br>- *F2*：到空间中&#x200B;*秒最近点*&#x200B;的距离<br>- *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-*&#x200B;边缘&#x200B;*：空间中噪声的每个单元格*&#x200B;之间的&#x200B;*边缘<br>-*&#x200B;随机颜色&#x200B;*：为空间中噪声的每个单元格分配*&#x200B;随机平面颜色* |
| <b>边缘Thickness</b> <i>Float</i> | 调整Voronoi噪声的细胞之间检测到的边缘的Thickness。 在X、Y和Z轴中检测到边缘，因此某些厚度可能比其他厚度增加得更快，具体取决于单元格的&#x200B;*深度*。<br><br>*注意*：仅当&#x200B;**Style**&#x200B;参数设置为&#x200B;*Edge*&#x200B;时，此参数才可用。 |
| <b>随机颜色种子模式</b> <i>整数</i> | 设置&#x200B;*获取*&#x200B;每个单元格颜色选择的随机种子的方法：<br><br>- *全局随机种子*：使用节点&#x200B;*继承*- *手动种子*：使用&#x200B;*离散*&#x200B;种子&#x200B;<br><br>*注意*：仅当&#x200B;**Style**&#x200B;参数设置为&#x200B;*随机颜色*&#x200B;时，此参数才可用。<br> |
| <b>随机颜色种子</b> <i>整数</i> | 应该用于每个单元格的颜色选择的离散随机植入。<br><br>*注意*：此参数仅在&#x200B;**Style**&#x200B;参数设置为&#x200B;*Random color*&#x200B;且&#x200B;**Random Color Seed Mode**&#x200B;参数设置为&#x200B;***Manual Seed***&#x200B;时可用。 |
| <b>非正方形扩展</b> <i>布尔值</i> | 启用压缩补偿并使用非正方形比例拉伸。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/voronoi-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/voronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/voronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/voronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/voronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/voronoi-variant6.jpg" />
        </td>
    </tr>
</table>
