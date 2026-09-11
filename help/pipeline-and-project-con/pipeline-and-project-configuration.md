---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Configure las opciones de canalización y proyecto en Substance 3D Designer para optimizar el flujo de trabajo y el resultado.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuración de tuberías y proyectos
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Configuración de tuberías y proyectos

Substance 3D Designer cuenta con un potente sistema para configurar la aplicación para el uso de canalización. Mediante un sistema avanzado de archivos jerárquicos de &quot;**Project**&quot;, la aplicación se puede configurar instantáneamente según los estándares de Studio o Project, y todas las configuraciones y el contenido de la biblioteca se encuentran en Control de versiones. El objetivo principal del sistema es centralizar todas las configuraciones relevantes para la canalización, pero permitir que varias configuraciones se anulen y se amplíen entre sí.

>[!WARNING]
>
> Este sistema no está diseñado para usuarios individuales con requisitos más sencillos, sino para *estudios con grandes proyectos y equipos* y una mayor necesidad de organización. Para hacer pleno uso de este sistema, una buena cantidad de planificación y preparación, así como un cierto grado de configuración automatizada se recomienda!

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Jerarquía de archivos de configuración

Designer tiene 3 niveles o archivos de configuración, cada uno con un propósito diferente. Para Windows, todos los archivos se encuentran en *~User\AppData\Local\Adobe\Adobe Substance 3D Designer.*

La imagen ilustra la relación entre los diferentes archivos de la configuración predeterminada de Designer después de una nueva instalación.

</td>
<td style="border: 0;" valign="top">

![Jerarquía de archivos de configuración](pipeline-and-project-configuration.resources/filestructureoverview.png "Jerarquía de archivos de configuración")

</td>
</tr>
</table>

* <b>[Usuario\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b> contiene la configuración general del programa, de la que todas las canalizaciones de proyecto, excepto una, no son relevantes. Este archivo es único y no se puede intercambiar, Designer está codificado para utilizar este archivo exacto.\
  Contiene una única referencia a un archivo de configuración.
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b> se puede intercambiar por otros archivos SBSCFG con nombres diferentes, pero solo se puede usar un archivo SBSCFG al mismo tiempo.\
  Contiene varias referencias a archivos de Project. *Tenga en cuenta que para la configuración predeterminada, estos archivos no están definidos explícitamente, pero están codificados de forma rígida.*
* Los archivos <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> contienen la configuración relevante de proyecto/canalización. Se pueden definir varios proyectos en una jerarquía, reemplazándolos o expandiéndolos en el proyecto definido anteriormente.

## Configuración de canalización de Designer

Cada tipo de archivo se explica con más detalle en las páginas secundarias de esta página, pero la breve descripción general de cómo definir idealmente una configuración personalizada para Designer es la siguiente:

1. <b>Identifica y agrupa qué configuraciones agregar a tus archivos de Project.</b> Esto es diferente para cada estudio y requiere una cierta cantidad de planificación!\
   En casi todos los casos deben definirse al menos dos proyectos: uno para valores predeterminados globales para todo el estudio (como plantillas estándar, archivos de sombreador, configuración de haga un bake) y otro con contenido más específico como contenido de biblioteca. Si tiene diferentes proyectos ejecutándose a la vez, puede que desee crear varias configuraciones de proyecto para cada uno (por lo tanto, un total de 3 o más).
1. <b>Cree los [archivos SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) correspondientes y colóquelos junto con su contenido en el Control de versiones.</b> Se recomienda encarecidamente separar el contenido de la canalización y biblioteca de Designer del contenido y los recursos reales del proyecto (modelos 3D, texturas, código) creando un *repositorio independiente* para él.
1. <b>Cree un archivo de [configuración SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) que muestre todos los archivos del proyecto, colóquelo en el Control de versiones </b>. Si tiene varios proyectos, puede crear una configuración para cada proyecto.
1. <b>Configure el archivo [User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) de cada usuario para que haga referencia a su archivo de configuración correspondiente.</b>\
   Puede hacer que cada usuario lo haga manualmente o puede escribir esto mediante secuencias de comandos inyectando líneas en su archivo XML. [Más información en la página correspondiente](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md).
