---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Designer Python脚本中的色彩管理功能来获取准确的颜色。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# 使用色彩管理

可从<b>SDApplication</b>类访问的<b> SDColorManagementEngine </b>类包含有关&#x200B;*当前色彩管理设置*&#x200B;的信息。

## 访问和查询色彩管理引擎

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


此外，还可以&#x200B;*将色彩空间*&#x200B;分配给Python中的位图资源。

### 在位图资源上设置色彩空间

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## 使用色彩空间转换编写SDTexture

**SDTexture**&#x200B;类的&#x200B;**save**&#x200B;方法现在接受可选的&#x200B;**outputColorSpace**&#x200B;参数。 指定后，将在保存图像之前&#x200B;*应用色彩空间转换*。

如果色彩管理模式支持嵌入的ICC配置文件&#x200B;*和*，则目标文件格式也支持它们，则色彩空间ICC配置文件将&#x200B;*嵌入到生成的图像文件中*。
