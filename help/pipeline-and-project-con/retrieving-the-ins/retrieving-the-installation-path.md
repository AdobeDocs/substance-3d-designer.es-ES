---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo recuperar la ruta de instalación de Substance 3D Designer para secuencias de comandos y automatización.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recuperación de la ruta de instalación
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 6%

---


# Recuperación de la ruta de instalación

Esta página reagrupa información sobre las formas de recuperar la ruta de instalación de [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html), en función de la versión y la plataforma.

## Windows

### Escritorio de Creative Cloud

1. Abra el <b>Editor del Registro de Windows</b> (regedit)
1. Vaya a la clave del registro: <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Rutas\&lt;/b>
1. Abra la subclave denominada <b>Adobe Substance 3D Designer.exe</b>
1. El valor de la clave contiene la ruta de acceso al ejecutable de la aplicación donde está instalada

>[!NOTE]
>
> Esta clave de registro solo está disponible desde la versión 11.2.\
> Para versiones anteriores, la ruta de instalación se puede recuperar desde las asociaciones de archivos en HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts

### Edición de Substance (independiente)

1. Abra el <b>Editor del Registro de Windows</b> (regedit)
1. Vaya a la clave del registro: <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. Busque la subclave que coincida con <b>AppID</b> de la versión de la aplicación (consulte la tabla siguiente)
1. El valor de la clave contiene la ruta de la ubicación de instalación de la aplicación

| Versión | AppId |
| --- | --- |
| **Versión 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **Versión 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **Versión 7.x (2017.x) a 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **Versión 11.2 (o posterior)** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Edición de Steam

La aplicación se instala en la subcarpeta steamapps/common/ de la carpeta de instalación de Steam.

## macOS

En Mac, la aplicación se instala de la siguiente manera:

| Versión | Ruta |
| --- | --- |
| **11.2 o posterior** | **/Applications/Adobe Substance 3D Designer.app** |
| **Heredado** | **/Applications/Substance Designer.app** |

## Linux

En Linux, el paquete rpm se instala en la siguiente ruta:

| Versión | Ruta |
| --- | --- |
| **11.2 o posterior** | **/opc/Adobe/Adobe\_Substance\_3D\_Designer** |
| **Heredado** | **/opc/Allegorithmic/Substance\_Designer** |
