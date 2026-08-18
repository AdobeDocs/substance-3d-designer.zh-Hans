---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/glossary.html"
breadcrumb-title: ''
description: 访问Substance 3D Designer词汇表以查找术语、概念和技术术语的定义。
helpx_creative_field: ""
helpx_description: Designer > Glossary
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 术语表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '4459'
ht-degree: 1%

---


# 了解Designer中使用的术语和概念。

## #

|  |  |
| --- | --- |
| <b><span id="three-d-scene"></span>3D场景</b> | 表示3D空间的可视化和为其制作动画所涉及的对象和数据集合：<ul data-preserve-html="true"> <li data-preserve-html="true">[网格](#mesh)</li> <li data-preserve-html="true">[材质](#material)</li> <li data-preserve-html="true">相机</li> <li data-preserve-html="true">光源</li> <li data-preserve-html="true">动画</li> <li data-preserve-html="true">模拟</li> <li data-preserve-html="true">...</li> </ul>用于存储3D场景的[常用文件格式](https://www.adobe.com/products/substance3d/discover/3d-files-formats.html)包括Pixar的[USD](#usd)和Autodesk的FBX。 所有文件格式均不支持所有这些组件 |

## A

|  |  |
| --- | --- |
| <b><span id="alpha"></span>Alpha频道</b> | 彩色图像的第四个通道，通常用于描述不透明度。 |
| <b><span id="ambient-occlusion"></span>环境遮蔽</b> | 环境光在曝光较少因而难以到达的表面上的衰减。 |
| <b><span id="anisotropy"></span>各向异性</b> | 依赖于方向的属性。 换句话说，当在不同的轴上测量或观察时，提供不同的结果。   各向异性材料根据其从何处观看具有不同的外观，并且各向异性滤镜并非在所有方向上均匀应用。 |
| <b><span id="api"></span>API</b> | 应用程序编程接口(API)是功能和过程的集合，允许用户访问另一个应用程序的功能和过程。   API在用户与程序之间提供受控且安全的层。 它还可以使用另一种编程语言来使程序更易于交互且更易于访问。   Designer提供了一个[Python API](../scripting/scripting.md)，通过此API可轻松访问其各种功能，以便处理数据、构建自定义工具和加快工作流程。 |
| <b><span id="atomic-node"></span>原子节点</b> | 图的基本构成要素。 所有[实例节点](#instance-node)都可以分解为原子节点的图形。 每种图形类型都有自己的一组原子节点。 |

## B

|  |  |
| --- | --- |
| <b><span id="baking"></span>烘焙</b> | 从3D模型计算信息并将结果存储到[纹理](#texture)的过程。 数据根据模型的[UV](#uv)放置在纹理中。 |
| <b><span id="base-color"></span>基色</b>(反照率) | 使用PBR金属粗糙度[着色](#shader)模型定义的[材质](#material)的通道。 基色指定没有任何光照信息的曲面的颜色。   不应将其与[扩散](#diffuse)混淆。 |
| <b><span id="base-parameter"></span>基本参数</b> | 计算[位图](#bitmap)的Substance图中所有节点都通用的参数。   其中包括位图的核心方面，例如其分辨率（[输出大小](#output-size)）和[位深度](#bit-depth)（输出格式），或者位图的计算方式，例如[拼贴](#tiling)模式。   基础参数通常是[从上游的其他节点或承载该节点的图形](#inheritance)继承的。 |
| <b><span id="bilinear-filtering"></span>双线性过滤</b> | [纹理样本](#texture-sampling)在像素的中心未准确执行时，计算机成像中使用的插值过程。   例如，在放大图像时可能会发生这种情况。 |
| <b><span id="bit-depth"></span>位深度</b> | 用于存储纹理中像素值的位数。 较高的位深度允许编码更多值，从而产生更平滑的渐变。   根据值的类型，可以使用不同的位深度： — 可以使用8位（0到255）或16位（0到65,535）对整数值进行编码。  — 浮点值可以使用16位（+32767.9999到 — 32768.0 ）或32位（–3.4E+38到+3.4E+38）进行编码。低动态范围图像使用整数值来编码0到1之间的步骤。 高动态范围图像使用浮点值对原始数值进行编码。   在Substance图中，位深度由“输出格式”参数控制。 |
| <b><span id="bitmap"></span>位图</b> | 数字图像。 最常见的图像类型有两种：<ul data-preserve-html="true"> <li data-preserve-html="true">灰度图像只有一个通道：明亮度(L)；</li> <li data-preserve-html="true">彩色图像有三个通道：红色、绿色和蓝色(RGB)。 第四种可能是alpha (A)，常用于不透明度。 Designer中的彩色图像始终是RGBA。</li> </ul>  位图可以看作是值的网格。 该网格的每个单元是一个像素，它是“图片元素”的简称。 像素为每个通道存储一个值。 该值的类型取决于位图的[位深度](#bit-depth)。 |

## C

|  |  |
| --- | --- |
| <b><span id="cache"></span>缓存</b> （内存） | 数据的集合 — 例如， 节点的[基本参数](#base-parameter)和输出图像 — 存储在内存中以便重复使用。   通过让[Substance 引擎](#substance-engine)仅重新计算图形中已更改的部分，缓存可极大地加快图形计算。 调整节点连接和参数时，它前面的所有节点不受这些更改的影响，因此不需要再次[计算](#evaluation)来更新图形。 将改用其缓存。   在大型图表中处理高分辨率和位深度时，缓存可能会占用大量内存。 |
| <b><span id="channel-packing"></span>频道打包</b> | 一种优化技术，其中单独的图像被打包到单个彩色图像的RGB(A)通道中。   例如，RMA纹理是粗糙度图(R)、金属度图(M)和环境色遮蔽图(A)，所有这些都封装成单一颜色纹理。   另一种常用的技术是将灰度纹理打包到法线映射的蓝色通道中，因为蓝色通道（即法线矢量的“Up”分量）可以在运行时重新计算。   [RGBA合并](../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)节点对于实现此技术非常有用。 |
| <b><span id="color-space"></span>色彩空间</b> | 颜色范围表示方式的定义。 对特定颜色进行数字编码和解码需要这样的定义才能理解所使用的数字。   图像文件使用指定的色彩空间存储颜色值，以便能够在支持该色彩空间的显示器上忠实再现这些颜色。 显示器具有特定的色彩再现能力，使其能够完全或部分支持给定的色彩空间。   原始数据 — 例如 法线映射 — 始终在线性色彩空间中编码和解码，因为这些颜色不是为了可视化，因此不应对该数据应用任何变换。   sRGB是广泛支持的色彩空间。 其他流行的色彩空间包括Adobe RGB、Rec. 2100和ProPhotoRGB。 |
| <b><span id="cooking"></span>烹饪</b>（<span id="compilation"></span>编译） | 将数据翻译成另一种语言的过程，以便可以快速、高效地执行。 计算Substance图的结果需要首先对其进行编译。 编译是图形[评估](#evaluation)过程的一部分。   此编译是在拼合的图上执行的，这意味着所有[实例节点](#instance-node)都将被其源图“替换”，以便保留一个较大的图，该图就是编译后的图。   已编译的图形不可编辑。 如果公开的参数为[动态](#dynamic-parameter)，则这些参数仍可用，而[静态](#static-parameter)参数被锁定并隐藏。 |
| <b><span id="culling"></span>剔除</b> | 一种用于渲染3D场景的优化技术，当几何不可见时，从渲染的计算中移除几何。   这可能包括相机截取轮廓（*截取轮廓*）之外的对象或多边形，朝向相机相反方向（*背面轮廓*），或者完全被其他不透明对象（*遮蔽轮廓*）隐藏。 |

## D

|  |  |
| --- | --- |
| <b><span id="dependency"></span>依赖关系</b> | 文件A由另一个文件B使用，导致文件B在缺少文件A时无法按预期工作。   [包](#package)的依赖关系可以是另一个包，因为它引用其中的图形、图像文件、字体等。包存储其依赖关系的路径，如果在该路径上找不到依赖关系，则会引发警告。 缺少依赖关系还可能导致图形中出现[虚影实例节点](#ghost-instance-node)。 |
| <b><span id="diffuse"></span>扩散</b> | 使用PBRSpecular光泽度[着色](#shader)模型定义的[材质](../glossary/glossary.md)的通道。 漫射指定光照时的表面颜色。   不应将其与[基色(反照率)](#base-color)混淆。 |
| <b><span id="directx"></span>DirectX</b> | 用于处理多媒体内容的API集合。 其3D API Direct3D广泛应用于视频游戏开发及其他3D行业。   Direct3D将纹理的原点(即它的(0， 0)坐标)放置在&#x200B;*左上*(Y-down)处，而[OpenGL](#opengl) API将其放置在&#x200B;*左下*(Y-up)处。   这意味着DirectX法线映射与OpenGL相比具有&#x200B;*倒置的绿色通道*。 事实上，绿色通道承载了法向量的Y坐标。 |
| <b><span id="displacement"></span>位移</b> | 移动3D模型[顶点](#vertex)的过程，通常沿其[正常](#normal)移动。   位移通常与[镶嵌](#tessellation)和[法线映射](#normal-map)结合使用，以在表面上建模更精细的细节。 |
| <b><span id="dynamic-parameter"></span>动态参数</b> | 值可能更改的参数。 换句话说，任何非常量的参数都是动态的。    这包括公开参数、任何受公开参数影响的参数以及任何受[纹理取样](#texture-sampling)影响的参数值。   与[静态参数](#static-parameter)相反，将图形编译为SBSAR文件后，动态参数的值可以实时调整。 |

## E

|  |  |
| --- | --- |
| <b><span id="evaluation"></span>评估</b> | 解决图形中数据和参数传播的过程。 评估验证图表及其连接的有效性，应用[继承](#inheritance)和[烹调](#cooking)图表。   在“图形视图”中，如果连接未计算，则用虚线表示。 计算将连接转换为实线。    每次在图表中调整参数时，承载此参数的节点和下游的所有节点都处于[无效](#invalidation)状态，需要重新计算才能进行[渲染](#rendering)。 |

## F

|  |  |
| --- | --- |
| <b><span id="filter"></span>筛选器</b> （节点） | 将修改应用于图像（例如，变形）或从中提取信息（例如，蒙版）的节点。 |

## G

|  |  |
| --- | --- |
| <b><span id="ghost-instance-node"></span>Ghost实例节点</b> | 将引用找不到的子图（即缺少的[依赖关系](#dependency)）的[实例节点](#instance-node)加载为Ghost实例节点。   通过解析缺少的依赖项并重新加载[包](#package)，Ghost实例节点将恢复到其预期状态。 |
| <b><span id="glossiness"></span>光泽度</b> | 使用PBRSpecular光泽度[着色](../glossary/glossary.md)模型定义的[材质](../glossary/glossary.md)的通道。 光泽度指定表面的粗糙度 — 即Height的微小变化，也称为&#x200B;*小平面*。   高光泽度产生平滑的外观，而低光泽度产生粗糙的哑光外观。   它是[粗糙度](#roughness)的反函数。 |

## 高

|  |  |
| --- | --- |
| <b><span id="histogram"></span>直方图（图像）</b> | 在图像上下文中，直方图表示给定范围内的值的集合 — 通常为[0， 1]。   此填充是使用垂直条显示的，图像中显示的值越多，则该值的条形越大。 这些条形从低值（暗）水平分布到高值（亮）。   彩色图像的直方图通常与其每个通道的直方图重叠 — 通常为R、G、B。 |

## I

|  |  |
| --- | --- |
| <b><span id="inheritance"></span>继承</b> | 在Substance图的上下文中，继承描述从上游节点或父图获取参数值的节点的属性。   继承的参数包括[分辨率](#resolution) （[输出大小](#output-size)）、[位深度](#bit-depth) （[输出格式](#output-format)）和[拼贴](#tiling)模式。   在此[专用页面](../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)中了解有关继承的详细信息。 |
| <b><span id="instance-node"></span>实例节点</b> | 实例节点将图形A表示为另一个图形B。在这种情况下，图形A可以称为图形B的[子图](#subgraph)。图形A中的任何更改都会传播到表示它的所有实例节点。   实例节点在图形B的上下文中为图形A的输入参数应用其自己的值集。在这个意义上，图形B可以承载多个实例节点，所有参考图形A，但是每个实例节点将不同值或纹理作为输入传递到图形A。   Designer Library中不是[原子节点](#atomic-node)的所有节点都是实例节点。 |
| <b><span id="invalidation"></span>无效</b> | 声明节点结果已过时的进程。   调整参数时，承载此参数的节点和下游的所有节点都将失效，因此需要再次[计算](#evaluation)和[渲染](#rendering)。 |

## M

|  |  |
| --- | --- |
| <b><span id="material"></span>材质</b> | 空间物质属性和行为的集合，包括表面和体积。 图元在3D空间中的外观由其材料定义。   材质可以用多种方式进行定义，并且所有定义均不支持所有属性，例如折射、各向异性或光泽。 [着色器](#shader)是素材定义的特定实现。   <b>重要提示：</b>术语“材质”是一个&#x200B;*总括性术语*，用于表示各种内容，包括：<ul data-preserve-html="true"> <li data-preserve-html="true">[着色器](#shader)用于计算表面或体积的外观；</li> <li data-preserve-html="true">向着色器提供的[纹理](#texture)集；</li> <li data-preserve-html="true">材质ID，它是3D图元的属性，用于区分使用不同材质的零件。</li> </ul> |
| <b><span id="mesh"></span>网格</b> | 由[顶点](#vertex)组成的3D对象，这些顶点通过边缘连接以形成多边形（如三角形），而多边形又装配成表面。 这些曲面可以是开放的，也可以是闭合的。   这些表面的外观由分配给它们的[材质](#material)定义。 网格的细节级别也高度依赖于其[多边形计数](#polycount)。 |
| <b><span id="metadata"></span>元数据</b> | 提供有关文件本身、文件环境或任何与文件数据相关的信息的数据。   常见元数据包括文件的作者、创建和修改日期、版权和封面图稿。   在Designer中，[包](#package)的内容也可以包含元数据。 例如，生成结构材料的Substance图可以具有结构物理属性的metadata。 |
| <b><span id="mipmap"></span>Mipmap</b> | 纹理的较小版本，通常自动计算。   纹理可以有自身较小版本的金字塔，这些版本在运行时可以互换，以便使用最合适的大小来获得最佳质量和性能。   例如，以较小尺寸显示高频细节的纹理可能会产生&#x200B;*摩尔纹*&#x200B;伪影。 此外，较大的纹理可能涉及更多[纹理样本](#texture-sampling)。   “mipmap”一词源自MIP映射技术，其中MIP表示拉丁语“*parvo*&#x200B;中的多数”，这表示“许多东西在一个小地方”。 |

## N

|  |  |
| --- | --- |
| <b><span id="node"></span>节点</b> | 图形中的对象，可执行计算并输出一个或多个结果。   使用输入参数控制结果。 这些参数可以作为“属性”停放区中的控件列出，也可以作为节点本身上的输入连接器列出。   节点有两种主要类别：[原子节点](#atomic-node)和实例节点。 |
| <b><span id="noise"></span>杂色</b> | 表示形状和颜色的随机或伪随机分布的非图形图像。 噪声通常用于为表面或变形添加变化。   Designer的节点库包含大量噪声生成器，如[BnW斑点](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md)、[云彩](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md)、[Perlin噪声](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/perlin-noise/perlin-noise.md)或[Voronoi](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/voronoi/voronoi.md)。 |
| <b><span id="normal"></span>正常</b> | 在3D计算中，曲面的法线是一个垂直于该曲面的[归一化](#normalization)矢量，从该曲面向外延伸。   此矢量表示曲面在3D空间中的方向，可根据场景的光线和相机透视对该曲面进行[着色](#shader)。   可以对表面应用[法线图](#normal-map)纹理以修改其法线并添加细节。 |
| <b><span id="normal-map"></span>法线图</b> | 应用于曲面以修改其法线的纹理。   它最常用于伪装细节，这些细节在模型几何中无法有效包含。 使用这样的映射允许除了每顶点的法线之外还有每纹理法线，从而产生更多的表面信息，从而产生更多的表面细节。   将法向量的X、Y和Z坐标分别编码为地图的红、绿、蓝通道。 根据目标图形API（[DirectX](#directx)或[OpenGL](#opengl)），可能会反转绿色通道。 |
| <b><span id="normalization"></span>标准化</b> | 将一系列值重新映射到[0， 1]范围的过程，其中最高输入值重新映射到1.0，最低输入值重新映射到0.0。   对于矢量，标准化是将矢量的长度（或“模”）调整为1.0的值。 |

## O

|  |  |
| --- | --- |
| <b><span id="opengl"></span>OpenGL</b> | 一种3D图形API，广泛应用于视频游戏开发及其他3D行业。   OpenGL将纹理的原点(即其(0， 0)坐标)放置在&#x200B;*左下*(Y-up)处，而[DirectX](#directx) API将其放置在&#x200B;*左上*(Y-down)处。   这意味着OpenGL正常映射与DirectX相比具有&#x200B;*反转绿色通道*。 事实上，绿色通道承载了法向量的Y坐标。 |
| <b><span id="openusd"></span>OpenUSD</b> | 请参阅[USD](#usd)。 |
| <b><span id="output-format"></span>输出格式</b> | 描述节点[位深度](#bit-depth)的Substance图中的[基参数](#base-parameter)。 |
| <b><span id="output-size"></span>输出大小</b> | 描述节点[分辨率](#resolution)的Substance图中的[基参数](#base-parameter)。   在此[专用页面](../compositing-graphs/output-size/output-size.md)中了解有关输出大小的更多信息。 |

## P

|  |  |
| --- | --- |
| <b><span id="package"></span>包</b> | Substance 3D文件([SBS](#sbs-file))称为包，因为它是一个资源容器：图形、[位图](#bitmap)、[3D场景](#three-d-scene)等。包还存储指向其[依赖项](#dependency)以及[元数据](#metadata)的路径。 |
| <b><span id="pattern"></span>图案</b> | 应用作生成另一张图像的模型或参考的图像。   在大多数情况下，图案是指要重复的图像（例如，拼贴、随机散布或根据一组规则排列）。 |
| <b><span id="pixel-ratio"></span>像素比率</b> | 此[基本参数](#base-parameter)控制像素级图像长宽比的补偿。 换言之，在非正方形图像中，是否应补偿像素大小以节省正方形比例。   该参数由非局部滤镜（即使用相邻像素的值来计算像素值的滤镜）使用。 |
| <b><span id="pixel-size"></span>像素大小</b> | 此基本参数定义像素的水平和垂直大小。   它可以充当非局部滤镜（即使用相邻像素的值来计算像素值的滤镜）的乘数。 |
| <b><span id="polycount"></span>多边形计数</b> | 3D [网格](#mesh)的多边形数量。 实际上，多边形计数是“多边形计数”的简称。   更多多边形可以构建更精细的细节。 具有低多边形的网格被称作“低多边形”，而具有更高多边形的网格被称作“高多边形”。 |
| <b><span id="primary-input"></span>主要输入</b> | [实例节点](#instance-node)的输入连接器，该节点从该节点继承其[基参数](#base-parameter)值。   主输入在其连接器中以小点标记，并在其标签中以“（主）”后缀标记。   在使用包含多个输入的节点时，*强烈*&#x200B;建议牢记其输入中的哪些是主要输入，以及它在整个图表中如何影响[继承](#inheritance)。 |
| <b><span id="procedural"></span>程序</b> | 按照计算机算法（而不是手动算法）创建的数据或伪像的特征。   Designer使用程序化工作流程，其中算法设计为节点图。     过程工作流允许更快的迭代，因为可以通过修改算法及其参数来快速生成变化和调整。   当结果完全由算法产生时，该结果统称为“100%过程”。 程序生成有时被缩短为“proc-gen”。   Designer节点库中的大多数生成器都具有100%的程序性，因为它们无需输入图像即可生成结果。 |
| <b><span id="publishing"></span>发布(SBSAR)</b> | 在Designer中，发布是指将[包](#package)导出为SBSAR存档文件，其中包括[已编译](#compilation)版本的图表、其资源（[位图](#bitmap)、字体等）、其预设以及其[元数据](#metadata)。   随后可以通过[Substance 3D插件](https://substance3d.adobe.com/plugins/)分发生成的SBSAR文件，并在其他Substance 3D应用程序或第三方应用程序中使用。 |

## R

|  |  |
| --- | --- |
| <b><span id="renderer"></span>渲染器</b> | 一种程序，可处理3D信息（如光源、网格和材质）以创建2D图像。 |
| <b><span id="rendering"></span>正在渲染</b>（3D视图） | 使用诸如[渲染器](#renderer)的程序根据输入数据计算图像的过程。 |
| <b><span id="resolution"></span>分辨率</b> | 形成[位图](#bitmap)的水平和垂直像素的数量。 更多的像素支持呈现更精细的细节。   在Substance图中，由[node](#node)计算的位图的分辨率由节点的“[输出大小](#output-size)”[基参数](#base-parameter)控制。 |
| <b><span id="roughness"></span>粗糙度</b> | 使用PBR金属粗糙度[着色](../glossary/glossary.md)模型定义的[材质](../glossary/glossary.md)的通道。 粗糙度指定表面的粗糙度 — 即Height的微小变化，也称为&#x200B;*小平面*。   高粗糙度产生哑光外观，而低粗糙度产生光滑、光泽的外观。   它是[光泽度](#glossiness)的反函数。 |

## S

|                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>取样</b>（取样） | 获取图像或函数在特定点的值。   请参阅[纹理取样](#texture-sampling)。 |
| <b><span id="sbs-file"></span>SBS文件</b> | SBS表示“Substance 3D文件”。 此文件用于存储Substance 3D Designer项目。 其数据使用[XML](#xml)格式。 请参阅[包](#package)。 |
| <b><span id="sbsar-file"></span>SBSAR文件</b> | SBSAR表示“Substance 3D阿奇韦”。 此存档文件用于存储已编译的Substance 3D Designer图形及其所需的资源（[位图](#bitmap)、字体等）。   SBSAR是用于分发Substance图表的主要文件格式，这些图表随时可供其他Substance 3D应用程序和Substance 3D增效工具使用。   由于SBSAR文件中存储的图形经过编译，因此无法在Substance 3D Designer中加载和编辑这些图形。 但是，可以使用[7Zip](https://www.7-zip.org/)打开SBSAR文件，以便在嵌入的[XML](#xml)文件中检索其参数、预设和元数据。 |
| <span id="sdf"></span><b>SDF</b> | 请参阅[符号距离字段](#signed-distance-field)。 |
| <b><span id="shader"></span>着色器</b> | 根据表面或体积的[材质](#material)属性、接收的光线以及观看它的位置计算其外观的程序。 着色器是材料定义的特定实现。   可以为着色器提供纹理以驱动其行为。 也可以使用Raw值。 在[3D视图](../interface/3d-view/3d-view.md)中，转到“材质”菜单以查看当前场景中的材质正在使用哪个着色器。 通过菜单还可访问[着色器属性](../interface/3d-view/3d-view.md)以及着色器当前正在使用哪些纹理和值。   “着色器”有时可与“[材质](#material)”互换使用。 |
| <span id="sheen"></span><b>光泽</b> | 织物的闪亮或光泽方面。   此术语在纺织业中广泛使用，用于描述可增加微妙的彩色亮度的反射特性。 |
| <b><span id="signed-distance-field"></span>带符号的距离字段(SDF)</b> | <p>有符号距离场是一种数学函数，通过计算空间中任意点到曲面上最近点的距离来定义3D空间中的曲面。</p><p>要了解有关此概念及其在Designer中的使用方式的更多信息，请参阅： [处理SDF 函数](../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#what-is-an-sdf-function)。</p> |
| <b><span id="spline"></span>样条</b> | 通常，曲线是使用数学函数建模的，该函数允许以任何分辨率绘制干净平滑的形状。 Designer使用通过使用自定义数据格式在纹理中编码的有损近似值。   样条提供了对长度和轨迹的直观控制，包括Thickness和Height等其他数据，并提供了对沿其任何点的距离和方向的轻松访问。   这些特质使它们成为绘图和纹理工具的强大工具。 |
| <b><span id="static-parameter"></span>静态参数</b> | 值不能更改的参数。   与[动态参数](#dynamic-parameter)相反，在将图形编译为SBSAR文件时，静态参数不能动态更改。 仅当创作图形时，才能在Designer中公开和修改这些图形。   在某些情况下，“预览模式”会隐藏这些参数，因为它旨在尽可能匹配已发布的SBSAR文件的行为。   静态参数的列表在[此处](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)可用。 |
| <b><span id="subgraph"></span>子图</b> | 在另一图形中用作[实例节点](#instance-node)的图形。 |
| <b><span id="substance-engine"></span>Substance 引擎</b> | 由Substance 3D团队开发的专有技术，通过非常高效地执行大量变换、效果和合成输入图像来计算图像。   Substance 引擎实现并计算Designer的[原子节点](#atomic-node)。   该引擎通过不同的后端实现，根据其运行的平台：CPU、GPU和操作系统。 在Designer中，可以通过转到[工具>切换引擎](../interface/the-main-toolbar/the-main-toolbar.md)来切换后端。   一些后端提供的性能明显好于其他后端 — 例如，GPU后端比CPU快得多 — 并且在后端之间结果可能略有不同。 |
| <b><span id="substance-graph"></span></b><b>图形</b>Substance（或Substance合成图形） | 输出一个或多个[位图](#bitmap)的图形。   Substance图形可用于多种目的： — 生成一组作为描述材料的纹理的位图； — 作为过滤器对一个或多个位图输入执行图像处理； — 作为生成器生成噪声、图案或原始数据。 |

## T

|  |  |
| --- | --- |
| <b><span id="tessellation"></span>镶嵌</b> | 在计算机图形学中，镶嵌是将曲面细分成多个多边形（通常是三角形）的过程。   此过程可在运行时执行，以动态增加3D模型的多边形数量，通常结合使用[位移](#displacement)和[法线映射](#normal-map)，以使用添加的多边形建立更精细的细节。 |
| <b><span id="texel"></span>文本</b> | [纹理](#texture)的信息单位，类似于像素是图片的信息单位。 |
| <b><span id="texture"></span>纹理</b> | 图像用于表示图形，通过向[着色器](#shader)提供值来描述表面的[材质](#material)属性，并在其[纹理元](#texel)中编码原始数据。   纹理是可以被GPU非常有效地解压缩和处理的对象。 在大多数情况下，此效率需要使用两种分辨率的纹理 — 例如，1024x1024、4096x4096、512x256等。 |
| <b><span id="texture-sampling"></span>纹理取样</b> | 正在获取特定位置的[纹理](#texture)的值。   有些算法需要执行许多样本来比较值、将它们平均或其它操作。   如果采样没有在像素的正中心执行，则Designer中应获取的值包含以下两个选项：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>最接近的：</b>根据像素中心的最接近像素的值</li> <li data-preserve-html="true"><b>双线性滤波：</b>邻近像素在水平和垂直方向之间的插值值，其中越接近的像素权重越大。</li> </ul> |
| <b><span id="tiling"></span>拼贴</b> | 沿水平、垂直或两者同时重复图像，而不会出现明显的接缝或视觉不连续性。   Designer提供了大量[节点](#node)来生成平铺的[噪声](#noise)或[图案](#pattern)。 同样，许多[筛选器](#filter)节点设计用于处理图像同时保留拼贴。 |

## U

|  |  |
| --- | --- |
| <b><span id="usage"></span>使用情况（输出）</b> | 在Substance图中，Usage是[输出](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点的属性，用于让应用程序了解如何在[3D视图](../interface/3d-view/3d-view.md)中将[纹理](#texture)连接到[着色器](#shader)。   将Substance图形应用于3D视图时，所有输出将基于匹配的用法连接到着色器。 即，“基色”到“基色”、“粗糙度”到“粗糙度”等等。   使用“材质”和“紧凑材质”[链接创建模式](../interface/the-graph-view/link-creation-modes/link-creation-modes.md)时，也会使用用例来匹配连接器。 |
| <b><span id="udim"></span>UDIM</b> （UV磁贴） | 将[UV](#uv)空间拆分为具有唯一数字标识符的拼贴的标准，它允许为每个拼贴分配不同的纹理。   UDIM工作流程在VFX管道中很常见，其中高保真资源需要大量细节，以致需要多个高分辨率纹理。 在这种情况下，资源的[UV](#uv)跨多个UDIM（或UV磁贴）排列。   Designer支持UDIM工作流程，并且可以为每个UDIM分配其他Substance图形。 |
| <b><span id="usd"></span>USD</b>（或OpenUSD） | [通用场景描述](https://openusd.org/release/index.html) (USD)是由Pixar构建的3D场景描述格式，为跨应用程序和平台实现互操作和数据交换而构建。   USD文件包括对场景中所用数据的定义，以及该场景的合成，它涉及的所有内容包括：模型、材料、相机、动画、模拟等。USD文件可包括任何类型的数据，前提是应用程序有权访问USD插件，使其能够正确读取和使用数据。   Adobe[参与了Alliance for OpenUSD](https://blog.adobe.com/en/publish/2023/08/01/powering-3d-interoperability-continued-collaboration-through-openusd)，这是一个由3D行业参与者组成的联盟，他们为该格式的开发和标准化做出了积极贡献。 |
| <b><span id="uv"></span>UV</b> | UV 是 3D 模型在 2D 空间中的表示形式。 它们用于将 2D 空间中的 2D 图像映射到 3D 空间中的模型表面。   创建 UV 的过程通常被描述为在模型中切割接缝以展开和展平模型。 |

## V

|  |  |
| --- | --- |
| <b><span id="vertex"></span>顶点</b> | 空间中的一个独特点，通常有两条或多条直线交会。 |

## X

|  |  |
| --- | --- |
| <b><span id="xml"></span>XML</b> | 可扩展标记语言(XML)是一种以人类可读格式存储数据的格式。   与HTML类似，使用标签(&lt;>)和值定义的数据包含在标签中。   [SBS](#sbs-file)文件格式使用XML排列和存储其数据。 |
