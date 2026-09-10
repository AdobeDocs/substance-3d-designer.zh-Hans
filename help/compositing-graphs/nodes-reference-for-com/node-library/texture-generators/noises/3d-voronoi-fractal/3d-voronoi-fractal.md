---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: 利用3D Voronoi Fractal节点生成基于三维位置的分形Voronoi图案，用于体积纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 3D Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi-fractal.resources/3dvoronoifractal.png){width="200px"}

<b>进入：</b>纹理生成器>噪声

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

<b>3D Voronoi Fractal</b>节点基于<b>位置映射</b>输入在3D空间中生成<i>分形</i>Voronoi噪声。

此节点可以使用[Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)作为输入而不是实际已烘焙贴图进行测试（如下面的示例图像所示）。

</td>
</tr>
</table>

>[!WARNING]
>
> 此噪声仅适用于<i>GPU引擎</i>（即<b>Direct3D</b>或<b>OpenGL</b>）。 转到<b>工具>切换引擎……</b>或按<b>F9</b>键以选择所需的引擎。

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>反转</b> <i>布尔值</i> | 反转输出图像。 |
| <b>缩放</b> <i>浮动</i> | 控制分形3D Voronoi噪声的比例。<br><br><i>注意</i>：在<i>任意轴</i>上启用<b>拼贴</b>时，比例调整为<i>分步</i>。 这是预期的。 |
| <b>大小</b> <i>浮点3</i> | 在<b>X</b>、<b>Y</b>和<b>Z</b>轴中控制分形3D Voronoi噪声的大小。 非均匀值导致<i>拉伸或挤压</i>效果。<br><br><i>注意</i>：在<i>任何轴</i>上启用<b>拼贴</b>时，大小调整为<i>步进</i>。 这是预期的。 |
| <b>偏移</b> <i>浮点3</i> | 将偏移应用于<b>X</b>、<b>Y</b>和<b>Z</b>轴的分形3D Voronoi噪声的<i>位置</i>。 |
| <b>无序</b> <i>浮点3</i> | 应用于<b>X</b>、<b>Y</b>和<b>Z</b>轴中每个噪声点的<i>随机偏移</i>的强度。 |
| <b>扭曲强度</b> <i>浮动</i> | 控制应用于分形3D Voronoi噪声的<i>变形效果</i>的强度。 |
| <b>扭曲比例乘数</b> <i>浮动</i> | 控制变形效果中使用的<i>变形图案</i>的比例，该比例由<b>扭曲强度</b>控制。 |
| <b>最小级别</b> <i>整数</i> | 分形图案中使用的最小<i>重复级别</i>。 更宽的最小值/最大值范围会生成<i>更丰富的图案</i>，并且随更多频率范围而变化。 |
| <b>最大级别</b> <i>整数</i> | 分形图案中使用的最大重复级别<i>为</i>。 更宽的最小值/最大值范围会生成<i>更丰富的图案</i>，并且随更多频率范围而变化。 |
| <b>粗糙度</b> <i>浮动</i> | 控制分形图案中低和高<i>重复级别</i>之间的<i>平衡</i>。<br><br><i>注意</i>：值<b>0</b>导致输出<i>与随后的其他低值不符</i>。 这是预期的。<br><br><i>注意2</i>：仅当<b>混合模式</b>参数设置为<i>添加</i>时，此参数才可用。 |
| <b>隙度</b> <i>浮动</i> | 控制应用的分形图案<i>填充空间</i>的方式。 <i>较高的</i>值会使图案中的间隙减少<i>，从而产生<i>更密</i>的杂色。</i> |
| <b>全局不透明度</b> <i>Float</i> | 将分形3D Perlin噪声值的<i>范围</i>控制为0。 |
| <b>圆角曲线</b> <i>Float</i> | 围绕噪声的每个点对<i>斜率</i>进行圆整，使其成为<i>凸形</i>。<br><br><i>注意</i>：当<b>Style</b>参数设置为<i>Edge</i>时，此参数不可用。 |
| <b>距离刻度</b> <i>Float</i> | 围绕噪声的每个点调整渐变</i>的<i>距离。 |
| <b>距离模式</b> <i>整数</i> | 将方法设置为<i>计算噪声的每个点周围的距离渐变</i>：<br><br>- <i>欧几里德</i><br>- <i>曼哈顿</i><br>- <i>切比雪夫</i><br>- <i>明科夫斯基</i> |
| <b>闵可夫斯基数值</b> <i>Float</i> | Minkowski距离的顺序<i>p</i>。 如果将距离渐变划分为几个象限，则此数值将对这些象限产生如下影响： <br><br>- p是<i>刚好</i> 1：笔直<br>- p是<i>低</i>比1：凹形<br>- p是<i>大</i>比1：凸形<br><br>有趣的值：<br>- <i>1.0</i>：曼哈顿距离<br>- <i>2.0</i>：欧几里德距离<br>- <i>无限远</i>：切比雪夫distance<br><br><i>注意</i>：此参数仅在<b>Distance Mode</b>参数设置为<i>Minkowski</i>时可用。 |
| <b>混合模式</b> <i>整数</i> | 设置将3D空间中<i>重叠单元格</i>的值混合在一起的方法：<br><br>- <i>相加</i>：相加值<br>- <i>最大值</i>：保留<i>最高</i>值<br>- <i>最小</i>：保留<i>最低</i>值 |
| <b>样式</b> <i>整数</i> | 设置分形3D Voronoi噪声的数据渲染</i>方法，考虑到噪声基于3D空间中的一组点：<br><br>- <i>F1</i>：到3D空间中<i>最近点</i>的距离<br>- <i>F2</i>：到3D空间中<i>第二个最近点</i>的距离<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F f1/F2</i><br>- <i>边缘</i>：3D空间中噪声的每个单元格之间的</i>边缘<i>- <i>随机颜色</i>：为3D空间中噪声的每个单元格分配<i>随机平色</i><i><br> |
| <b>边缘Thickness</b> <i>Float</i> | 调整分形3D Voronoi噪声在细胞之间检测到的边缘的Thickness。 在X、Y和Z轴中检测到边缘，因此某些厚度可能比其他厚度增加得更快，具体取决于单元格的<i>深度</i>。<br><br><i>注意</i>：仅当<b>Style</b>参数设置为<i>Edge</i>时，此参数才可用。 |
| <b>启用拼贴</b> <i>布尔值</i> | 调整分形3D Voronoi噪声，使其生成的图案<i>在X、Y和Z轴中重复</i>。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant6.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant4.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant3.jpg" />
        </td>
    </tr>
</table>
