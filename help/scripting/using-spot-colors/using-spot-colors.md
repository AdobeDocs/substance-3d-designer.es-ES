---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/using-spot-colors.html"
breadcrumb-title: ''
description: Aprenda a utilizar tintas planas en la creación de scripts de Substance 3D Designer Python para flujos de trabajo de color especializados.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using spot colors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de tintas planas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Uso de tintas planas

La clase </b>SDSpotColorLibrary<b>, a la que se tiene acceso desde la clase <b>SDApplication</b>, contiene información sobre las bibliotecas de tintas planas incluidas en Designer.

Con esta clase es posible enumerar libros de colores y tintas planas y buscar tintas planas específicas o la tinta plana más cercana a un color RGB determinado.

Las tintas planas *no están disponibles* en Designer al usar <b>OpenColorIO</b>. En este caso, app.getSpotColorLibrary() devolverá <b>None</b>.

>[!IMPORTANT]
>
> Las tintas planas *no están disponibles* en Designer al usar <b>OpenColorIO</b>. En este caso, app.getSpotColorLibrary() devolverá <b>None</b>.

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


Las tintas planas se pueden recuperar y establecer en propiedades de nodo.

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
