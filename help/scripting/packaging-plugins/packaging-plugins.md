---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo empaquetar complementos de Python para Substance 3D Designer para su distribución e instalación.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Complementos de empaquetado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# Complementos de empaquetado

## Contenido del paquete del complemento

Los paquetes son un único archivo, internamente un archivo zip, que contiene un archivo **pluginInfo.json** con metadatos sobre el complemento,

el código del complemento y cualquier otro archivo o recurso necesario para que el complemento funcione.

**Entradas PluginInfo.json:**

| Entrada | Descripción | Valor predeterminado | Notas |
| --- | --- | --- | --- |
| metadata\_format\_version | Formato del archivo de metadatos. | 1 | Requerido. Actualmente debe establecerse en 1. |
| nombre | El nombre del complemento. |  | Requerido. Debe coincidir con el nombre del módulo Python que contiene el código del complemento |
| versión | La versión del complemento. |  | Opcional. |
| autor | El autor del complemento. |  | Opcional. |
| correo electrónico | Correo electrónico del autor del complemento. |  | Opcional. |
| min\_designer\_version | Versión mínima de la aplicación requerida por el plugin para funcionar. | 2019.2 | Opcional. |
| plataforma | Plataforma en la que se ejecuta el complemento. | cualquier | Opcional. Para los complementos que contengan código compilado, esta entrada se puede utilizar para deshabilitar el complemento en plataformas no compatibles.Valores posibles: win, linux, osx, any. |

## Creación de un nuevo proyecto de paquete de complementos

Proporcionamos un proyecto de plantilla [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) para simplificar la creación de proyectos de paquetes de complementos.

Puede utilizarlo directamente o modificarlo para sus propias necesidades.

La plantilla se encuentra en el directorio de la aplicación, en <b>plugins/tools/pkgplugintemplate</b>.

1. <b>Instale Python si aún no está instalado en el sistema</b>

   Cookiecutter es compatible con Python 2 y Python 3
1. <b>Instalar Cookiecutter si aún no lo tienes</b>

   Normalmente esto se puede hacer usando pip:

   ```
   pip install cookiecutter
   ```


   Para obtener formas alternativas de instalar Cookiecutter o para obtener más información sobre Cookiecutter, consulte la documentación en <https://cookiecutter.readthedocs.io/en/latest/installation.html>
1. <b>Crear un nuevo proyecto de paquete de complementos</b>

   En una ventana de terminal, ejecute:

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   Rellene la información requerida. El nuevo proyecto se creará en el directorio especificado.
1. <b>Empaquete el complemento una vez completado el desarrollo</b>

   En una ventana de terminal, ejecute:

   ```
   python makepackage.py
   ```

1. El paquete del complemento se generará en el directorio de compilación.
