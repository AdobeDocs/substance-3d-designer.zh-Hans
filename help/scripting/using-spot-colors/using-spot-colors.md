---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/using-spot-colors.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python脚本中使用专色执行专门的颜色工作流程。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using spot colors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用专色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 使用专色

<b>个SDSpotColorLibrary </b>类可从<b>SDApplication</b>类访问，其中包含有关Designer中包含的专色库的信息。

使用此类可以列出色标簿和专色，并查找特定的专色或与给定RGB最接近的专色。

使用<b>OpenColorIO</b>时，Designer中的专色&#x200B;*不可用*。 在这种情况下，app.getSpotColorLibrary()将返回<b>None</b>。

>[!IMPORTANT]
>
> 使用<b>OpenColorIO</b>时，Designer中的专色&#x200B;*不可用*。 在这种情况下，app.getSpotColorLibrary()将返回<b>None</b>。

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

spotLib = app.getSpotColorLibrary() 

 

## Find a color by color book and color name.

col = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

 

print(col) 

print(col.get()) 

 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col)) 

 

## Find the closest spot color in a specific book, to an RGB color.

## The RGB color is specified in the working color space currently used by Designer.

col = spotLib.findClosestSpotColor( 

    spotColorBookName="PANTONE+ Solid Coated", 

    r=88 / 255.0, 

    g=132 / 255.0, 

    b=167 / 255.0 

) 

 

print(col) 

print(col.get()) 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col))
```


可以从节点属性中检索专色并将其设置为专色。

```
import sd 

from sd.api.sdbasetypes import * 

from sd.api.sdvaluecolorrgba import SDValueColorRGBA 

from sd.api.sdvaluespotcolor import SDValueSpotColor 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getUIMgr() 

spotLib = app.getSpotColorLibrary() 

 

node = uiMgr.getCurrentGraphSelection()[0] 

 

## Set RGBA color in node property.

rgbaColor = SDValueColorRGBA.sNew(ColorRGBA(0.7, 0.5, 0.2, 1)) 

node.setInputPropertyValueFromId("outputcolor", rgbaColor) 

 

## Set spot color in node property.

spotColor = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

node.setInputPropertyValueFromId("outputcolor", spotColor) 

 

## Get color from node property (could be a SDValueColorRGBA or a SDValueSpotColor)

anyColor = node.getInputPropertyValueFromId("outputcolor") 

 

## Print the RGBA components of the color.

print(anyColor.get()) 

 

## Check if the color is a spot color.

if isinstance(anyColor, SDValueSpotColor): 

## Print the spot color information of the color.

    print(spotLib.getSpotColorBookName(anyColor)) 

    print(spotLib.getSpotColorName(anyColor)) 

 
```
