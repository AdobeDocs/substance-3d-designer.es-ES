---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Aprenda a utilizar variables de entorno en Substance 3D Designer para configurar rutas y ajustes del sistema.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables de entorno
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# Variables de entorno

Esta página muestra variables de entorno que se pueden utilizar para anular el comportamiento predeterminado de la aplicación.

| Variable | Descripción |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | La ruta desde la que Designer cargará [complementos de Python](../../scripting/plugin-basics/plugin-basics.md). |
| **SUBSTANCE\_DESIGNER\_LICENSE** | La ubicación del archivo de licencia (*license.key*) que debe usar Designer.   Reemplaza la ruta establecida en el [Asistente de activación](../../getting-started/activation-and-licenses/activation-and-licenses.md) de Designer.  **Nota:** Es posible que las versiones anteriores deban usar un nombre de variable alternativo:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | Ruta de acceso al archivo de configuración de OCIO que se debe usar al usar OpenColorIO [administración de color](../../color-management/color-management.md).   Reemplaza la ruta establecida en la configuración de administración de color de Designer en [Configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md). |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | El retraso en segundos antes de liberar una licencia de licencia en caso de una configuración para varios usuarios El valor predeterminado es de 7200 segundos (2 horas). |
