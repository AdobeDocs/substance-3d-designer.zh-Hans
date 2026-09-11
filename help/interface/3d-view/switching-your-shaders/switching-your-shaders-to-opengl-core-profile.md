---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer 3D视图中将着色器切换到OpenGL核心配置文件，以提高兼容性和性能。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 将着色器切换到OpenGL核心配置文件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# 将着色器切换到OpenGL核心配置文件

自版本2018.2.0起，3D视口使用OpenGL核心配置文件。\
此时，我们更新了从GLSL版本120到GLSL版本330的部分着色器。

您可能希望更新自己的着色器以利用新的GLSL函数，或者使GLSL代码更现代。 请注意，在MacOS上，旧着色器可能无法再使用。\
有关新增功能的完整概述，我们强烈建议您仔细阅读官方OpenGL文档。 例如，您可以查看[OpenGL着色语言规范3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf)。\
否则，以下快速指南将帮助您在GLSL 3.30中转换GLSL 1.20着色器：

## 更新版本号

首先，请`#version 330`替换您以前的`#version`指令（如果尚未替换，则将其添加到文件顶部）。

### 将“attribute”和“varying”替换为“in”或“out”

现在，`attribute`和`varying`变量已显式声明为`in`或`out`，具体取决于着色器阶段：

在着色器中，顶点的`attribute`被声明为`in`，而要传递给片段着色器的`varying`被声明为`out`。\
例如：

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


将变为：

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


同样在碎片着色器中，变化也会出现。 还应声明一个将替换gl\_FracColor（不再内置）的out变量：

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


将变为：

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### 使用新的纹理查找函数

随着着色语言的新版本，纹理查找API得到了简化和增强。

`texture1D()`、`texture2D()`、`texture3D()`和`textureCube()`函数都成为`texture()`的重载。\
同样，`texture2DLod()`变为`textureLod()`，`texture2DGrad()`变为`textureGrad()`，依此类推。

您现在还可以访问有用的功能，如`textureSize()`（在文本中查询取样器大小）、`textureOffset()`（对目标位置的邻居进行取样）、`textureFetch()`（在像素中提供取样位置）等等。
