---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Configure las rutas de búsqueda de complementos en Substance 3D Designer para especificar dónde se encuentran los complementos de Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rutas de búsqueda de complementos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Rutas de búsqueda de complementos

Designer buscará complementos en directorios específicos (es decir, rutas de búsqueda). Esta página explica cómo configurar estas rutas.

Los usuarios pueden *agregar directorios personalizados* manualmente en las preferencias de software o especificarlos mediante variables de entorno.

## Adición manual de rutas de búsqueda de complementos

1. Vaya a <b>Editar > Preferencias...</b>
1. Seleccione la categoría <b>Proyectos</b>
1. Seleccione el <b>archivo de proyecto</b> que desea editar
1. En la pestaña <b>Python</b>, haz clic en el botón *<b>+</b>*para agregar el directorio que contiene los complementos
1. Haga clic en <b>Aceptar</b> para validar

![Configurar complementos de Python rutas de búsqueda Configuración del proyecto](plugin-search-paths.resources/plugin-search-paths-01.png "Configurar complementos de Python rutas de búsqueda Configuración del proyecto")

## Uso de variables de entorno

La aplicación buscará complementos en todas las rutas especificadas mediante la variable de entorno <b>SBS\_DESIGNER\_PYTHON\_PATH </b>.
