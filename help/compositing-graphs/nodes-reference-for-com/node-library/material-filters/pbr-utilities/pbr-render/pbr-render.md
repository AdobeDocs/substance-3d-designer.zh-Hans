---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: 使用PBR 渲染节点以真实的光照渲染基于物理的材质，从而预览材质外观。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 渲染
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 6%

---


# PBR 渲染

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render.resources/pbr-render.png){width="250px"}

<b>进入：</b>材质过滤器> PBR实用工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用基于图像的光照(IBL)将PBR素材渲染到球体、平面或圆柱体上。这是节点内的渲染引擎，对于生成缩览图、预览或2D资源非常有用。 它不是如3D视图那样进行渲染，而是图形中生成的实际纹理。

此节点要求至少插入一个完整的PBR材料。 理想情况下，可使用“链接创建模式”将材料连接到PBR 渲染。 此外，您还需要一个球面展开的HDRI环境，以便渲染从中计算光照。 可以在PBR Materials下找到用于测试的材质，也可以在库中的[ 3D View下找到环境地图。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **CPU (SSE2)引擎**
> 
> PBR 渲染节点非常重，无法与SSE2 CPU引擎配合使用。 如果节点性能极差，则按F9切换到另一个引擎。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>材料频道输入</b> | 使用多个材料输入渲染几何上的材料： <br><br>-Base color<br> — 正常<br>-Emissive<br>-粗糙度<br>-金属<br>-Specular level<br>-Height<br>-Ambient occlusion<br> — 不透明度蒙版<br>-Anisotropy level<br>-Anisotropy angle<br>-Translucency<br> — 散射距离比例 |
| <b>镜头Dirt映射</b> <i>灰度输入</i> | 镜头上Dirt的自定映射，当镜头眩光可见时显示。 |
| <b>镜头光圈映射</b> <i>灰度输入</i> | 可用于覆盖散景、离焦形状。 对比越明显，它就越明显。 请记住，只对纹理中的一个圆圈进行取样，因此任何形状都必须适合一个圆圈。 |
| <b>背景输入</b> <i>颜色输入</i> | 将<b>背景模式</b>参数设置为<i>背景输入</i>时用作背景的自定义映射 |
| <b>环境图</b> <i>颜色输入</i> | 用于计算光照的环境图。 必须球面映射且在HDR中。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>美丽</b> | 最终渲染 |
| <b>原始辐照度</b> | 最终渲染<br><br><i>Alpha</i>不透明度映射的辐照度数据 |
| <b>原始Specular</b> | 最终渲染<br><br><i>Alpha</i>Specular阴影映射的Specular数据 |
| <b>正常世界空间</b> | 最终渲染<br><br><i>Alpha的世界空间法线数据： </i>世界空间高度图 |
| <b>法向切空间</b> | 正切空间法线最终渲染<br><br><i>Alpha：</i>正切空间高度图的数据 |
| <b>UV</b> | 最终渲染<br><br><i>Alpha的UV数据： </i>不透明度映射 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>形状</b> <i>球面、平面、圆柱体</i> | 设置用于渲染的形状。 无法自定义形状。 |
| <b>位移强度</b> <i>0.0 - 0.5</i> | 设置来自Height的位移强度。 |
| <b>环境轮换</b> <i>0.0 - 1.0</i> | 旋转光照环境。 与移动相机时相比预旋转。 |
| <b>背景模式</b> <i>颜色、环境、环境、背景输入</i> | 设置背景中显示的内容。 颜色是纯色，环境是使用可选模糊插入的地图。 “环境”是一种非常模糊的环境。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 仅在“背景”模式设置为“颜色”时可用。 |
| <b>环境背景模糊</b> <i>0.0 - 1.0</i> | 仅在“背景”模式设置为“环境”时可用。 |
| <b>形状</b> |  |
| <b>缩放</b> <i>0.0 - 2.0</i> | 设置球体的比例。 |
| <b>平面大小</b> <i>0.0 - 1.0</i> | 设置平面的比例。 |
| <b>圆柱半径</b> <i>0.0 - 1.0</i> | 设置圆柱的半径。 |
| <b>圆柱体长度</b> <i>0.0 - 1.0</i> | 设置圆柱的长度。 |
| <b>旋转</b> <i>0.0 - 1.0</i> | 旋转形状，而不旋转光照。 |
| <b>旋转方向</b> <i>0.0 - 1.0</i> | 在2D中设置旋转轴。 |
| <b>围绕方向</b>旋转 <i>0.0 - 1.0</i> | 在旋转轴上旋转形状。 |
| <b>形状位置</b> <i>-1.0 - 1.0</i> | 移动形状。 |
| <b>拼贴</b> <i>1.0 - 6.0</i> | 设置UV拼贴的量。 |
| <b>球体UV 缩放</b> <i>0.0 - 4.0</i> | 设置UV在球面上的比例。 |
| <b>平面UV 缩放</b> <i>1.0 - 4.0</i> | 设置UV在平面上的比例。 |
| <b>圆柱体UV 缩放</b> <i>1.0 - 6.0</i> | 设置UV在圆柱上的比例。 |
| <b>UV 偏移</b> <i>0.0 - 1.0</i> | 偏移UV |
| <b>倾斜UV</b> <i>False/True</i> | 将球体的UV倾斜45度。 |
| <b>相机</b> |  |
| <b>曝光</b> <i>-4.0 - 4.0</i> | 设置相机曝光。 |
| <b>色调映射器</b> <i>线性， ACE， Filmic Hejl</i> | 设置用于最终图像的色调映射解决方案。 |
| <b>相机模式</b> <i>透视，正交</i> | 在两个投影模式之间切换相机。 |
| <b>视角</b> <i>0.01 - 100.0</i> | 设置相机视场角度。 |
| <b>距离</b> <i>0.0 - 4.0</i> | 设置相机到对象中心的距离。 |
| <b>晕影强度</b> <i>0.0 - 1.0</i> | 设置晕影效果的强度。 |
| <b>晕影半径</b> <i>0.0 - 1.0</i> | 设置晕影效果的半径。 |
| <b>屏幕位置</b> | 围绕对象移动相机，也可以在2D视图中使用线框进行更改。 |
| <b>字段深度</b> |  |
| <b>光圈半径</b> <i>0.0 - 0.1</i> | 设置光圈的半径。 值越高，离焦区域越模糊（散景）。 |
| <b>光圈刀片</b> <i>3 - 9</i> | 设置散景模糊的形状。 |
| <b>光圈环</b> <i>0.0 - 1.0</i> | 向散景形状添加内部渐变。 |
| <b>光圈分数</b> <i>0.0 - 2.0</i> | 向散景图添加色差。 |
| <b>旋转散景</b> <i>0.0 - 1.0</i> | 向离焦散景模糊区域添加涡旋或旋转类型的效果。 |
| <b>焦点模式</b> <i>自动，点</i> | 设置焦点是预先确定的还是用户设置的。 点焦点允许您在2D视图中移动一个点以确定焦距。 |
| <b>焦点</b> | 如果焦点设置为“点”，则可以移动该点。 有一个二维视图小工具。 |
| <b>焦点偏移</b> <i>-0.5 - 0.5</i> | 如果焦点设置为“自动”，则允许您来回移动它。 |
| <b>使用自定义光圈映射</b> <i>False/True</i> | 覆盖上面的Aperture设置，并使用Aperture映射输入来确定散景形状。 需要输入。 |
| <b>后期效果</b> |  |
| <b>启用后期效果</b> <i>False/True</i> | 在最终渲染中切换<i>所有</i>后期效果。 |
| <b>开花强度</b> <i>0.0 - 2.0</i> | 设置开花效果的强度。 |
| <b>开花阈值</b> <i>0.0 - 2.0</i> | 设置开花的低阈值。 |
| <b>开花色度偏移</b> <i>0.0 - 1.0</i> |  |
| <b>镜头光晕强度</b> <i>0.0 - 1.0</i> | 设置镜头光晕效果的强度。 |
| <b>镜头眩光强度</b> <i>0.0 - 1.0</i> | 设置镜头眩光的强度。 确保环境背景中的光线处于查看状态，以便正确查看此效果。 |
| <b>镜头Dirt强度</b> <i>0.0 - 1.0</i> | 在镜头眩光上设置镜头Dirt映射的效果。 |
| <b>渲染设置</b> |  |
| <b>Diffuse质量</b> <i>16个样本，32个样本，64个样本，128个样本</i> | 在漫射图的品质级别之间切换。 |
| <b>Diffuse的Emissive乘数</b> <i>0.0 - 1.0</i> | 控制emissive部分对辐照度的贡献程度。 |
| <b>Diffuse阴影强度</b> <i>0.0 - 1.0</i> | 控制漫射阴影的强度。 |
| <b>仿色</b> <i>0.0 - 1.0</i> | 设置Specular的仿色量。 |
| <b>Specular阴影乘数</b> <i>0.0 - 1.0</i> | 控制Specular反射中的阴影强度。 |
| <b>不透明度模式</b> <i>抖动Alpha测试，简单Alpha混合</i> | 控制应用透明度的方法。 <i>简单混合</i>模式在统一背景上最明显。 |
| <b>Ambient occlusion强度</b> <i>0.0 - 1.0</i> | 设置ambient occlusion阴影的强度。 |
| <b>材料调整</b> |  |
| <b>重新计算法线</b> <i>False/True</i> | 将根据位移强度从高度图中重新计算法线。 |
| <b>正常格式</b> <i>DirectX， OpenGL</i> | 在不同的法线贴图格式之间切换（反转绿色通道） |
| <b>介电F0输入</b> <i>常量值，输入Specular level</i> | 设置什么驱动F0值。 Specular level输入表示它将由输入图驱动。 |
| <b>电介质F0</b> <i>0.0 - 0.08</i> | 如果为“电介质F0输入”选择了“常量值”，则此滑块允许您设置全局值。 |
| <b>透明外套</b> |  |
| <b>启用透明涂层</b> <i>False/True</i> | 在输入材料顶部启用另一个简单的透明涂层。 |
| <b>透明外套重量</b> <i>0.0 - 1.0</i> | 设置透明涂层图层的强度或强度。 |
| <b>清除Coat specular level</b> <i>0.0 - 1.0</i> | 设置透明涂层的粗糙度。 |
| <b>从基底图层继承普通</b> <i>False/True</i> | 设置clearcoat是否忽略或使用来自基础材质的法线。 |
| <b>Emissive</b> |  |
| <b>启用Emissive光照</b> <i>True/False</i> | 切换emissive光照的扩散作用。 |
| <b>Emissive强度</b> <i>0.0 - 10.0</i> | 设置emissive映射的全局乘数。 |
| <b>次表面散射</b> |  |
| <b>启用次表面散射</b> <i>True/False</i> | 在最终渲染中切换次表面散射。<br><br><i>注意：</i>次表面散射要求<b>Translucency</b>输入值为<i>大于0.0</i> |
| <b>散射距离</b> <i>0.0 - 1.0</i> | 调整散射效果的最大距离。<br><br><i>注意：</i>此值与<b>散射距离刻度</b>输入值<i>每个颜色通道</i>相乘。 |
| <b>红移</b> <i>0.0 - 1.0</i> | 调整散射中红移效果的强度。 |
| <b>瑞利</b> <i>0.0 - 1.0</i> | 调整散射中的瑞利效果强度。 |

## 示例

所有图像都是使用[Substance 3D资源](https://substance3d.adobe.com/assets)库中的材料，直接在Designer内部以2D视口生成的。

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/pbr-render-v2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-thermal-insulation-panel.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-ominous-obsidian.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-forest-gravel-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-chesterfield-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-carbon-fiber.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/plane-inclined-lumber-tiles.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/cylinder-medieval-leaded-glass-window.jpg" />
        </td>
    </tr>
</table>
