---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: 在Substance 3D Designer 3D视图中使用GLSLFX着色器自定义素材渲染和预览效果。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GLSLFX着色器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# GLSLFX着色器

GLSLFX文件是应用程序与glsl着色器文件之间的桥梁。\
它允许使用任意的glsl着色器，而无需修改代码。

## 文件格式

GLSLFX文件格式为XML文件。 支持注释。

### 标头和根节点

XML根节点元素名为<b>glslfx</b>。

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### 正文

#### 方法

描述方法的XML元素。 技术就是当前外汇的变动。 GLSLFX可以包含多种技术，但必须至少定义一种技术。

几何将使用应用程序定义的技术之一进行渲染。

+++XML元素定义
<b>名称：</b>方法

<b>属性：</b>

* name：用于命名技术的任何字符串

+++

XML元素可以有多个子级。 在技术中定义的元素覆盖全局定义的元素。

例如，它用于覆盖某些统一值并获取此技术的FX变化。

#### 渲染通道

描述渲染通道的XML元素。 渲染刀路描述几何的渲染。

一种技术可以包含将按顺序执行的多个渲染刀路。 不包含渲染通道的技术与包含“屏幕上”渲染通道的技术等效。

渲染通道中定义的元素会覆盖父技术中定义的元素。

+++XML元素定义
<b>名称：</b>次

<b>属性：</b>

* 输出

* 屏外：渲染将完成到用户定义的渲染目标中

* 屏幕上：渲染将导入默认渲染目标

+++

#### 着色器

设置每种类型的GLSL着色器文件。

XML元素定义：

+++XML元素定义
<b>名称：</b>着色器

<b>属性：</b>

* 类型：GLSL着色器类型；

* filename：glsl着色器文件的路径。 可以是绝对的，也可以是相对于GLSLFX文件的；

* primitiveType：呈现基元的方法。


| “类型”值 | 描述 |
| --- | --- |
| 顶点 | 顶点着色器 |
| 几何 | 几何着色器 |
| tess\_control | 镶嵌控制着色器 |
| tess\_eval | 镶嵌评估着色器 |
| 碎片 | 碎片着色器 |



| “primitiveType”值 | 描述 |
| --- | --- |
| 点 | 渲染为点 |
| lineloop | 渲染为线条循环 |
| patch[1..N] | 渲染为具有[1..N]顶点的修补程序 |


+++

#### 属性

允许设置OpenGL状态的某些部分。

+++XML元素定义
<b>名称：</b>属性

<b>属性：</b>

* 名称：要设置的属性的名称。 该名称基于OpenGL函数或glEnum名称：
  * 枚举语法：不带“GL\_”前缀（小写）。 示例： glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;&quot;， glDisable(GL\_CULL\_FACE) => &quot;&quot;
  * 函数语法：不带“gl”前缀、小写和所有用“\_”字符分隔的单词。 示例：glBlendFunc(GL\_SRC\_ALPHA， GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* 枚举语法：不带“GL\_”前缀（小写）。 示例： glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;&quot;， glDisable(GL\_CULL\_FACE) => &quot;&quot;

* 函数语法：不带“gl”前缀、小写和所有用“\_”字符分隔的单词。 示例：glBlendFunc(GL\_SRC\_ALPHA， GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* value：属性的值。


| “名称”值 | “值”值 | 描述 |
| --- | --- | --- |
| blend\_enabled | 布尔值 | 启用/禁用混合模式 |
|  | true |  |
|  | 假连翘 |  |
| 混合\_func | 字符串，字符串 | 设置源和目标混合函数 |
|  | 零 | 对于OpenGL枚举GL\_ZERO |
|  | 一 | 对于OpenGL枚举GL\_ONE |
|  | src\_color | 对于OpenGL枚举GL\_SRC\_COLOR |
|  | one\_minus\_src\_color | 用于OpenGL枚举GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | 对于OpenGL枚举GL\_DST\_COLOR |
|  | one\_minus\_dst\_color | 用于OpenGL枚举GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | 对于OpenGL枚举GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | 用于OpenGL枚举GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alpha | 对于OpenGL枚举GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | 用于OpenGL枚举GL\_ONE\_MINUS\_DST\_ALPHA |
|  | constant\_color | 对于OpenGL枚举GL\_CONSTANT\_COLOR |
|  | one\_minus\_constant\_color | 用于OpenGL枚举GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | constant\_alpha | 用于OpenGL枚举GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | 用于OpenGL枚举GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | 用于OpenGL枚举GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | 对于OpenGL枚举GL\_SRC1\_COLOR |
|  | one\_minus\_src1\_color | 用于OpenGL枚举GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | 对于OpenGL枚举GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | 用于OpenGL枚举GL\_ONE\_MINUS\_SRC1\_ALPHA |
| cull\_face\_enabled | 布尔值 | 启用/禁用人脸剔除 |
|  | true |  |
|  | 假连翘 |  |
| cull\_face\_mode | 字符串 | 设置人脸剔除模式 |
|  | 前面 | 对于OpenGL枚举GL\_FRONT |
|  | 背面 | 对于OpenGL枚举GL\_BACK |
|  | front\_and\_back | 用于OpenGL枚举GL\_FRONT\_AND\_BACK |
| 深度\_func | 字符串 | 设置深度比较函数 |
|  | 从不 | 对于OpenGL枚举GL\_NEVER |
|  | 视图中 | 用于OpenGL枚举GL\_LESS |
|  | 勒卡尔 | 对于OpenGL枚举GL\_LEQUAL |
|  | 相等 | 对于OpenGL枚举GL\_EQUAL |
|  | notequal | 对于OpenGL枚举GL\_NOTEQUAL |
|  | gequal | 对于OpenGL枚举GL\_GEQUAL |
|  | 更大 | 用于OpenGL枚举GL\_GREATER |
|  | 总是 | 对于OpenGL枚举GL\_ALWAYS |


+++

#### 制服

允许覆盖某些全局定义或父技术中定义的制式。 这允许更改此技术或渲染通道的着色器行为。

有关其定义的更多详细信息，请参阅下面的<b>制服</b>部分。

+++示例


+++

## 渲染目标

对于“屏外”渲染通道，必须在渲染通道中定义渲染目标。

+++XML元素定义
<b>名称：</b>输出

<b>属性：</b>

* 附件：OpenGL附件点，灵感来自OpenGL名称：\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
  GL\_深度\_附件=> &#39;深度&#39;

附件：OpenGL附件点，灵感来自OpenGL名称：\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
GL\_深度\_附件=> &#39;深度&#39;

* 名称：渲染目标的名称。\
  可在稍后的渲染通道中使用它将此渲染目标绑定为取样器。

名称：渲染目标的名称。\
可在稍后的渲染通道中使用它将此渲染目标绑定为取样器。

* 格式：渲染目标的内部格式。

格式：渲染目标的内部格式。

* 清除：定义清除值的可选属性。\
  如果存在，渲染目标将在渲染通道开始处被清除为此值。\
  如果缺失，渲染目标将保留其以前的内容。

+++

>[!NOTE]
>
> “屏幕”渲染通道中禁止使用彩色渲染目标，但可以与任何渲染通道共享深度渲染目标（但当场景中混合多个素材时，可能会中断渲染）。

<b>关于格式</b>

对于深度格式，支持所有仅深度（无模板）的OpenGL格式：

* GL\_深度\_组件16 => &#39;深度26&#39;
* GL\_深度\_组件24 => &#39;深度34&#39;
* GL\_深度\_组件32 => &#39;深度42&#39;
* GL\_深度\_组件32F => &#39;深度42f&#39;

对于颜色格式，该名称基于OpenGL枚举名称，不带“GL\_”前缀（使用小写）。\
不支持三种声道格式(RGB)，请改用RGBA格式。\
支持的每个渠道的位深度：

* 规范化无符号整数： 8， 16
* 浮点： 16， 32

这些规则的一个例外是受支持的GL\_R11F\_G11F\_B10F格式：

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => &quot;rg16&quot;

### 采样器

如果允许覆盖某些全局定义的取样器，则无法在某个技术中定义它们。 这允许为此渲染通道定义取样器用法，或从上一个渲染通道的渲染目标进行读取。

请参阅<b>取样器</b>部分以了解有关其定义的更多详细信息。

+++示例


+++

## 输入顶点格式

这允许定义在顶点着色器中定义的每个属性的语义。

<b>XML元素定义：</b>

名称： &#39;vertexformat&#39;

属性：

* “name”：在顶点着色器中定义的属性的名称。
* “semantic”：属性的语义。

| “语义”值 | 描述 |
| --- | --- |
| 位置 | 顶点位置(float3) |
| 正常 | 顶点法向(float3) |
| texcoord[0..N] | 顶点纹理坐标缓冲区N (float2) |
| tangent[0..N] | 顶点切线缓冲区N (float4) |
| 二正则[0..N] | 顶点双正规缓冲区N (float4) |

示例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## 采样器

这允许定义每个取样器的用法。\
应用程序使用它来了解要在指定取样器中设置哪种纹理。

<b>XML元素定义：</b>

名称： &#39;sampler&#39;

属性：

* &#39;name&#39;：着色器文件中取样器变量的名称。
* &#39;usage&#39;：取样器的用法。 它匹配在图形的输出节点中指定的用法。

| “使用情况”值 | 描述 |
| --- | --- |
| 扩散 | 漫射图 |
| 不透明度 | 不透明度图 |
| 自发光 | 发射图 |
| 环境包容 | 环境遮蔽图 |
| 氛围 | 环境图 |
| mask | 蒙版图 |
| 细节正常 | 细节法线图 |
| 正常 | 法线图 |
| 隆起物 | 凹凸图 |
| Height | Height图 |
| 位移 | 位移图 |
| specularlevel | Specular level图 |
| specularcolor | Specular彩图 |
| Specular | Specular图 |
| 光泽度 | 光泽度图 |
| 粗糙度 | 粗糙度图 |
| 各向异性 | 异嗜性水平图 |
| 各向异性 | 各向异性角映射 |
| 传输 | 透射图 |
| 反射 | 反射图 |
| 折射 | 折射图 |
| 环境 | 环境映射（多维数据集映射） |
| 全景图 | 全景图（经纬度图） |
| 蓝橡胶 | 256x256抖动纹理 |

* 支持多种用途。
  * 示例：

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


“isHidden”：指示取样器是否应显示在GUI中的布尔值

* 示例：

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


绕排模式：

<table data-preserve-html="true"><tbody><tr><th>名称</th><th>值</th></tr><tr><td rowspan="4">texture_wrap_s、texture_wrap_t、texture_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">重复<br/><br/></td></tr></tbody></table>

纹理滤镜

<table data-preserve-html="true"><tbody><tr><th>名称</th><th>值</th></tr><tr><td rowspan="6">texture_min_filter， texture_mag_filter<br/><br/><br/></td><td>最接近的</td></tr><tr><td>线性</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

示例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## 制服

这允许您添加有关每种着色器制服的其他信息。

<b>XML元素定义：</b>

名称： &#39;uniform&#39;

属性：

&#39;name&#39;：着色器文件中制服的名称。

| “语义”值 | 描述 |
| --- | --- |
| 世界 | 世界矩阵(float16) |
| 世界反转 | 全局反转置矩阵(float16) |
| worldviewprojection | “世界视图”投影矩阵(float16) |
| viewinverse | 全局逆矩阵(float16) |
| worldview | “世界视图”矩阵(float16) |
| modelview | 模型视图矩阵(float16) |
| 投影 | 投影矩阵(float16) |
| 氛围 | 场景环境颜色(float3) |
| lightposition[0..N] | 场景第N灯的位置(float3) |
| lightcolor[0..N] | 场景第N灯的颜色(float3) |
| 光照强度[0..N] | 场景第N光强度（浮动） |
| globaltime | 当前时间（秒）（浮点） |
| 分辨率 | 视区分辨率(int2) |
| 鼠 | 鼠标位置(int2) |
| 示例可发布大小 | 用于计算环境光照(int)的样本数 |
| 辐照食谱 | 球面谐波矢量的阵列(float3[10]) |
| 全景mamipmapheight | 全景图中的多级渐远纹理级别数（浮点） |
| 全景旋转 | 全景图的角度旋转角度（浮点） |
| 全景维护 | 全景图的强度（浮点） |
| computebinormalinfragmentshader | 每个片段是否计算二正规？ （如果不是，则按顶点）(bool) |
| isdirectxnormal | 是DirectX吗？ (bool) |
| uvwscale | u、v、w的缩放值(float3) |
| renderuvtile | 仅渲染1个UV磁贴？ (bool) |
| uvtilecoords | 要渲染的UV拼贴坐标(int2) |

“semantic”：统一的语义。 （所有矩阵均为float16）。

示例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


示例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### 其他参数

其他附加信息可添加到每个制服，以便：

* 定义默认值
* 固定值
* 控制统一在应用程序中的显示方式：
* 设置标签
* 设置用于在应用程序中编辑值的构件信息：
* 构件名称、最小值、最大值、增量/递减步长
* 组小组件中的组表单

由于可以覆盖每种技术的制服，因此允许显示每种技术的特定GUI设置。

<b>XML元素定义：</b>

名称： &#39;uniform&#39;

属性：

* &#39;name&#39;：着色器文件中制服的名称。
* &#39;default&#39;：统一的默认值
* &#39;min&#39;：有效性范围的最小值
* &#39;max&#39;：有效性范围的最大值
* “guiName”：应用程序GUI中统一的名称
* “guiGroup”：将统一放置在应用程序GUI中的组的名称
* “guiWidget”：用于在应用程序的GUI中编辑统一值的小组件的名称

| “guiWidget”值 | 描述 |
| --- | --- |
| 滑块 | floatN的滑块构件 |
| 角度 | 浮点角度构件 |
| 颜色 | float3、float4颜色的颜色构件 |
| 复选框 | 用于bool的CheckBox构件 |

* “guiMin”：小组件的最小值
* &#39;guiMax&#39;：小组件的最大值

## 示例：镶嵌/视差

### 视差顶点着色器文件

位于。\tessellation\_parallax\parallax\vs.glsl

内容：

> #version 120

属性vec4 iVS\_Position；\
属性vec4 iVS\_Normal；\
属性vec2 iVS\_UV；\
属性vec4 iVS\_Tangent；\
属性vec4 iVS\_Binormal；

改变vec3 iFS\_Normal；\
改变vec2 iFS\_UV；\
改变vec3 iFS\_Tangent；\
改变vec3 iFS\_Binormal；\
改变vec3 iFS\_PointWS；

uniform mat4 worldMatrix；\
uniform mat4 worldViewProjMatrix；

void main()\
&lbrace;\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position；\
iFS\_Normal = iVS\_Normal.xyz；\
iFS\_UV = iVS\_UV；\
iFS\_Tangent = iVS\_Tangent.xyz；\
iFS\_Binormal = iVS\_Binormal.xyz；\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position)。xyz；\
&rbrace;

### 镶嵌顶点着色器文件

位于。\tessellation\_parallax\tessellation\vs.glsl

内容：

&#x200B;>> 

&#x200B;#version 120

属性vec4 iVS\_Position；\
属性vec4 iVS\_Normal；\
属性vec2 iVS\_UV；\
属性vec4 iVS\_Tangent；\
属性vec4 iVS\_Binormal；

varying vec4 oVS\_Normal；\
改变vec2 oVS\_UV；\
改变vec4 oVS\_Tangent；\
改变vec4 oVS\_Binormal；

void main()\
&lbrace;\
gl\_Position = iVS\_Position；\
oVS\_Normal = iVS\_Normal；\
oVS\_UV = iVS\_UV；\
oVS\_Tangent = iVS\_Tangent；\
oVS\_Binormal = iVS\_Binormal；\
&rbrace;

### 镶嵌控制着色器文件

位于。\tessellation\_parallax\tessellation\tcs.glsl

内容：

&#x200B;>> 

&#x200B;#version 400核心\
&#x200B;#extension GL\_ARB\_tessellation\_shader ：启用

layout(vertices = 3) out；

in vec4 oVS\_Normal[]；\
in vec2 oVS\_UV[]；\
in vec4 oVS\_Tangent[]；\
in vec4 oVS\_Binormal[]；

out vec4 oTCS\_Normal[]；\
out vec2 oTCS\_UV[]；\
out vec4 oTCS\_Tangent[]；\
out vec4 oTCS\_Binormal[]；

均匀浮点镶嵌因子；

void main()\
&lbrace;\
gl\_TessLevelOuter[0] = tesselationFactor；\
gl\_TessLevelOuter[1] = tesselationFactor；\
gl\_TessLevelOuter[2] = tesselationFactor；\
gl\_TessLevelInner[0] = tesselationFactor；\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position；

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID]；\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID]；\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID]；\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID]；\
&rbrace;

### 镶嵌评估着色器文件

位于。\tessellation\_parallax\tessellation\tcs.glsl

内容：

&#x200B;>> 

&#x200B;#version 400核心

layout（三角形， equal\_spacing， ccw） in；

in vec4 oTCS\_Normal[]；\
在vec2 oTCS\_UV[]中；\
in vec4 oTCS\_Tangent[]；\
in vec4 oTCS\_Binormal[]；

uniform mat4 worldMatrix；\
uniform mat4 worldViewProjMatrix；

uniform sampler2D heightMap；

均匀浮点拼贴= 1.0f；\
统一浮点高度heightMapScale = 1.0f；

out vec3 iFS\_Normal；\
out vec2 iFS\_UV；\
out vec3 iFS\_Tangent；\
out vec3 iFS\_Binormal；\
out vec3 iFS\_PointWS；

vec3插值3D(vec3 v0、vec3 v1、vec3 v2、vec3 uvw)\
&lbrace;\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2；\
&rbrace;

vec2插值2D(vec2 v0、vec2 v1、vec2 v2、vec3 uvw)\
&lbrace;\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2；\
&rbrace;

void main()\
&lbrace;\
vec3 uvw = gl\_TessCoord.xyz；

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz， gl\_in[1].gl\_Position.xyz， gl\_in[2].gl\_Position.xyz， uvw)；\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz， oTCS\_Normal[1].xyz， oTCS\_Normal[2].xyz， uvw)；\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz， oTCS\_Tangent[1].xyz， oTCS\_Tangent[2].xyz， uvw))；\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz， oTCS\_Binormal[1].xyz， oTCS\_Binormal[2].xyz， uvw)；\
vec2 newUV = interpolate2D(oTCS\_UV[0]， oTCS\_UV[1]， oTCS\_UV[2]， uvw)；

float heightTexSample = texture（heightMap， newUV \&#42;拼贴）。x \&#42; 2.0 - 1.0；\
newPos += newNormal \&#42; heightTexSample \&#42; heightMapScale；

vec4 obj\_pos = vec4(newPos， 1)；\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos；

iFS\_UV = newUV \&#42;拼贴；\
iFS\_Tangent = newTangent；\
iFS\_Binormal = newBinormal；\
iFS\_Normal = newNormal；\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos)。xyz；\
&rbrace;

### 碎片着色器文件

位于。\tessellation\_parallax\fs.glsl

内容：

&#x200B;>> 

&#x200B;#version 120

// #define ALG\_NORMAL\_DIRECTX\
&#x200B;#define ALG\_NORMAL\_OPENGL

&#x200B;#ifdef ALG\_NORMAL\_DIRECTX\
//#define翻转\_法向\_X\
&#x200B;#define翻转_法向\_Y\
//#define翻转\_法向\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_DIRECTX

&#x200B;#ifdef ALG\_NORMAL\_OPENGL\
//#define翻转\_法向\_X\
&#x200B;#define翻转_法向\_Y\
//#define翻转\_法向\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_OPENGL

改变vec3 iFS\_Normal；\
改变vec2 iFS\_UV；\
改变vec3 iFS\_Tangent；\
改变vec3 iFS\_Binormal；\
改变vec3 iFS\_PointWS；

uniform vec3 Lamp0Pos = vec3(0.0f、0.0f、70.0f)；\
统一vec3 Lamp0Color = vec3(1.0f、1.0f、1.0f)；\
uniform vec3 Lamp1Pos = vec3(70.0f、0.0f、0.0f)；\
uniform vec3 Lamp1Color = vec3(0.198f，0.198f，0.198f)；\
uniform bool flipNormal = true；\
统一浮点TilingDetail = 3.0f；\
统一浮点SpecExpon = 50.0；\
均匀浮点Ks = 1.0；\
uniform int parallax\_mode = 0；\
均匀浮点镶嵌因子= 4.0；\
统一浮点高度heightMapScale = 1.0f；\
统一浮点深度\_detail = 0.5f；\
均匀浮点Kr = 0.5f；\
uniform int KF\_on = 1；\
统一浮点数KF = 1.0f；\
uniform vec3 AmbiColor = vec3(0.07f，0.07f，0.07f)；\
均匀浮点拼贴= 1.0f；\
uniform int enableTilingInFS = 0；

uniform sampler2D heightMap；\
uniform sampler2D normalMap；\
uniform sampler2D detailNormalMap；\
一致sampler2D emissiveMap；\
均匀采样器2D漫射图；\
均匀采样器2D specularMap；\
uniform sampler2D opacityMap；\
uniform samplerCube environmentMap；

uniform mat4 worldMatrix；\
一致mat4 worldInverseTransposeMatrix；\
统一mat4 viewInverseMatrix；

vec4 litFct(float NdotL、float NdotH、float specExp)\
&lbrace;\
浮点环境变量= 1.0；\
float spinder = max(NdotL， 0.0)；\
floatSpecular= step(0.0， NdotL) \&#42; pow(max(0.0， NdotH)， specExp)；\
return vec4（环境，扩散，Specular，1.0）；\
&rbrace;

vec3 lerpFct（vec3 v0， vec3 v1，浮动百分比）\
&lbrace;\
返回v0 + (v1-v0) \&#42;百分比；\
&rbrace;

//冯着色\
void phong\_着色(\
在vec3 LightColor中，\
在vec3 normalWS，\
在vec3 pointToLightDirWS中，\
在vec3 pointToCameraDirWS中，\
inout vec3 DiffuseContrib，\
inout vec3 SpecularContrib)\
&lbrace;\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS)；\
vec4 litV = litFct(dot(normalWS， pointToLightDirWS)， dot(normalWS， Hn)， SpecExpon)；\
DiffuseContrib = litV.y \&#42; LightColor；\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor；\
&rbrace;

vec3 fixNormalSample(vec3 v)\
&lbrace;\
vec3结果= v - vec3(0.5,0.5,0.5)；

&#x200B;#ifdef翻转_法向\_X\
result.x = -result.x；\
&#x200B;#endif // ifdef FLIP\_NORMAL\_X\
&#x200B;#ifdef翻转_法向\_Y\
result.y = -result.y；\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Y\
&#x200B;#ifdef翻转_法向\_Z\
result.z = -result.z；\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Z

返回结果；\
&rbrace;

vec3 normalVecOSToWS(vec3 normal)\
&lbrace;\
返回正常；\
&rbrace;

void main()\
&lbrace;\
vec3 cameraPosWS = viewInverseMatrix[3].xyz；\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS)；\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS)；\
vec3 pointToCameraDirWS = normalize(cameraPosWS)；\
vec3 normalOS = normalize(iFS\_Normal)；\
vec3 tangentOS = normalize(iFS\_Tangent)；\
vec3 binormalOS = normalize(iFS\_Binormal)；

// ------------------------------------------\
//确保TBN正交归一化\
binormalOS = normalize(cross(normalOS， tangentOS))；\
tangentOS =规范化(cross(binormalOS， normalOS))；

vec3 cumulatedNormalOS = normalOS；

// ------------------------------------------\
//更新UV\
float a = dot(normalOS，-pointToCameraDirWS)；\
vec3 s = vec3(dot(pointToCameraDirWS，tangentOS)， dot(pointToCameraDirWS，binormalOS)， a)；\
vec2 uv = enableTilingInFS == 0 ？ iFS\_UV ： （iFS\_UV \&#42;平铺）；\
floatHeight= texture2D(heightMap，uv)。x \&#42; 2.0 - 1.0 ；\
float parallax = parallax\_mode == 0 ？ （镶嵌系数/ 100000.f + heightMapScale / 500.f） ： (heightMapScale / 50.f)；\
uv += （Height\&#42; s.xy \&#42;视差） ；

// ------------------------------------------\
//从normalMap添加法线\
vec3 normalTS = texture2D(normalMap，uv)。xyz；\
normalTS = fixNormalSample(normalTS)；\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS；\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS；\
cumulatedNormalOS = normalize(cumulatedNormalOS)；

// ------------------------------------------\
//添加细节正常映射\
vec3 normalDetailTS = texture2D(detailNormalMap，uv\&#42;TilingDetail)。xyz；\
normalDetailTS = fixNormalSample(normalDetailTS)；\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5)，normalDetailTS，深度\_detail)；\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS；\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS；\
cumulatedNormalOS = normalize(cumulatedNormalOS)；

if (length(normalTS)&lt;0.0001)\
累积正常操作系统=正常操作系统；

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS)；

// ------------------------------------------\
//计算扩散和Specular

// Light 0贡献\
vec3 diffContrib = vec3(0， 0， 0)；\
vec3 specContrib = vec3(0， 0， 0)；\
phong\_着色(Lamp0Color， cumulatedNormalWS， pointToLight0DirWS， pointToCameraDirWS， diffContrib， specContrib)；

//光源1的贡献\
vec3 diffContrib2 = vec3(0， 0， 0)；\
vec3 specContrib2 = vec3(0， 0， 0)；\
phong\_着色(Lamp1Color， cumulatedNormalWS， pointToLight1DirWS， pointToCameraDirWS， diffContrib2， specContrib2)；

diffContrib += diffContrib2；\
specContrib += specContrib2；

vec4漫射色= texture2D(diffuseMap，uv)；

vec3 specularColor = texture2D(specularMap，uv)。rgb；\
vec3 R = reflect(pointToCameraDirWS，cumulatedNormalWS)；\
vec3 reflColor = Kr \&#42; textureCube(environmentMap，R.xyz)。bgr；

float FallofRefl；

if (KF >= 0.0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs)，cumulatedNormalWS))，0)\&#42;KF\_on；\
else\
FallofRefl = (1-max((1-dot(pointToCameraDirWS/(-KFs)，cumulatedNormalWS)))，0)\&#42;KF\_on；

if (KF\_on == 0)\
FallofRefl=1.0；

vec3 Ambiant\_final = spinderColor.rgb\&#42;AmbiColor；

// ------------------------------------------\
vec3的发射率= texture2D(emissiveMap，uv)。xyz；

vec3 finalcolor = Ambiant\_final\
&#x200B;+ specularColor\&#42;specContrib\
&#x200B;+ spinderColor.rgb\&#42;diffContrib\
&#x200B;+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
+放射性；

//最终颜色\
vec4 finalColor4 = vec4(finalcolor， texture2D(opacityMap，uv))；

gl\_FragColor = finalColor4；\
&rbrace;

### GLSLFX文件

glslfx文件定义了两种渲染几何图形的技术：

* 一种是采用硬件镶嵌技术
* 另一种是基于视差效果，如果用户硬件不支持镶嵌，该效果将被用作回退。

位于。\tessellation\_parallax\fs.glsl

内容：

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
