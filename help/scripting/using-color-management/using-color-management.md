---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Aprenda a utilizar las funciones de gestión de color en la creación de scripts de Substance 3D Designer Python para obtener colores precisos.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de la gestión de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Uso de la gestión de color

La clase </b>SDColorManagementEngine<b>, a la que se tiene acceso desde la clase <b>SDApplication</b>, contiene información sobre la *configuración actual de administración de color*.

## Acceso y consulta del motor de gestión de color

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


Además, es posible *asignar espacios de color* a recursos de mapa de bits desde Python.

### Definición de espacios de color en recursos de mapa de bits

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


## Escribir SDTextures con conversiones de espacio de color

El método **save** de la clase **SDTexture** ahora acepta un parámetro **outputColorSpace** opcional. Cuando se especifique, la conversión del espacio de color se *aplicará antes de guardar la imagen*.

Si el modo de administración de color admite los perfiles ICC incrustados *y*, el formato de archivo de destino también los admite, el perfil ICC del espacio de color se *incrustará en el archivo de imagen resultante*.
