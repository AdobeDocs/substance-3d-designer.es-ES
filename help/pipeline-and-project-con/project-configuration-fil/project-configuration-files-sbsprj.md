---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: Aprenda a utilizar los archivos de configuración de proyecto SBSPRJ en Substance 3D Designer para administrar la configuración del proyecto.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Archivos de configuración del proyecto: SBSPRJ'
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Información general

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>Los archivos de configuración del proyecto</b> son los archivos más complejos y extensos que se usan para configurar Substance 3D Designer.

Son especiales en el sentido de que puede utilizar varios archivos de configuración de proyecto, en los que cada proyecto &#39;secundario&#39; siguiente expande o reemplaza el &#39;principal&#39; anterior. A menos que se necesite explícitamente, la configuración no se debe modificar ni añadir a los archivos del proyecto, por lo que Designer puede recurrir a su configuración principal, o incluso a los valores predeterminados.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Icono de archivo SBSPRJ](../../assets/sbsprj.png "Icono de archivo SBSPRJ")

</td>
</tr>
</table>

De forma predeterminada, Designer tiene dos configuraciones de proyecto activas:

<b>Proyecto predeterminado: </b>Contiene toda la configuración predeterminada y la biblioteca Designer se incluye en una instalación nueva.*Sólo lectura; no se puede modificar ni quitar.*

<b>Proyecto de usuario: </b>Dado que los valores predeterminados son de solo lectura, *todos los cambios realizados por el usuario* entran en este proyecto de manera predeterminada. *No se puede quitar.*

Esta configuración básica garantiza que la biblioteca predeterminada y otras configuraciones no se puedan dañar o modificar, pero permite que usuarios únicos y aficionados agreguen sus propias modificaciones sin tener que preocuparse por configuraciones complejas.

## Expandir o reemplazar

La mayoría de las configuraciones de un proyecto consecutivo <b>reemplazarán</b> las del proyecto anterior. Por ejemplo, un plugin de Tangent Space diferente en un archivo de proyecto personalizado anulará cualquier plugin de TS definido en el proyecto predeterminado o de usuario. Esto significa que, a menos que se necesite explícitamente, se recomienda no reemplazar ni cambiar la configuración de los proyectos secundarios.

Sin embargo, hay algunas configuraciones que <b>expanden</b> en la configuración principal, en lugar de reemplazarlas. En particular, estos ajustes son las rutas y los filtros de la biblioteca, por lo que siempre se añade más contenido a la biblioteca en lugar de anularlo. Además, están los alias (palabras clave de ruta para rutas de archivo relativas) que se expanden, así como la anulación si se define un duplicado. Esto permite un gran control sobre las rutas de archivo de contenido y las referencias.

## Contenido del archivo de proyecto

Los archivos de proyecto pueden contener las siguientes configuraciones:

<b>Vista 3D: </b>Definiciones de sombreador predeterminado, HDR y estado de escena.

<b>Alias: </b>Alias de palabras clave para rutas relativas.

<b>Horneado: </b>Configuración de las convenciones de asignación de nombres.

<b>General: </b>Plantillas de gráficos, complementos de espacio de tangente, valores predeterminados de formato normal y de imagen.

<b>Biblioteca: </b>Rutas controladas para mostrar en la biblioteca.

<b>Secuencias de comandos: </b>Scripts e intérpretes de devolución de llamada.

Control de versiones de <b>: </b>Configuración para integrar el control de versiones en Designer.

## Modificación de archivos de proyecto

Las configuraciones de proyecto, como todos los demás tipos, se guardan como archivos XML estructurados (utilizando una extensión <b>.sbsprj</b>) que se pueden modificar mediante la interfaz de usuario de Designer o mediante un editor de texto externo.

## Dentro de Substance 3D Designer

Consulte la página [Configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md) para obtener más información sobre cómo administrar archivos de proyecto y cambiar la configuración del proyecto.

Los archivos de proyecto también incluyen <b>categorías</b> y <b>filtros</b> personalizados para la [biblioteca](../../interface/the-library/the-library.md), sobre los que puedes obtener más información en la página [Administración de contenido y filtros personalizados](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md).

## Editar XML externamente

Para Windows, [Notepad++](https://notepad-plus-plus.org) es una buena opción gratuita. En macOS, [Sublime Text](https://www.sublimetext.com/) es una alternativa. Dicho esto, cualquier editor con la sangría adecuada, el colapso de secciones y alguna forma de resaltado de sintaxis hará tu vida mucho más fácil.

Una vez que abra el archivo SBSPRJ en un editor, debería ver un diseño estructurado bastante sencillo, con secciones correspondientes a pestañas en la interfaz de usuario. No todos los escenarios serán documentados aquí, ya que es bastante auto-explicativo.

![Edición XML](../../assets/project-xml.png "Edición XML")

## Rutas y alias relativos

Las rutas de acceso relativas combinadas con alias son una de las partes más complicadas y, sin embargo, más importantes de la configuración de un proyecto, esta sección las aclarará. La adición de alias personalizados para un archivo de proyecto específico se realiza en [Configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md).

Uno de los principales problemas con los archivos que hacen referencia a otros archivos de un sistema en el equipo de varios usuarios es que las rutas de archivo absolutas no funcionarán. Los usuarios pueden definir sus repositorios SVN en ubicaciones completamente diferentes (p. ej. C:/John/Gamedev/SubstanceLibrary o D:/Dev/SubstanceLibrary). Los alias y las rutas relativas funcionan juntos para resolver este problema. De lo contrario, podría abrir el archivo de otra persona e intentará buscar el nodo personalizado utilizado en la ubicación específica en la que el usuario lo tenía localmente, que probablemente no habrá definido exactamente de la misma manera.

Un <b>alias</b> es una palabra clave que reemplaza (parte de) una ruta. Es similar a una variable de entorno de Windows como %TEMP%, donde una sola palabra reemplaza una ruta de acceso utilizada a menudo que se define de forma centralizada. La ventaja es que los trazados se simplifican en todas partes, y una forma de modificar todas las referencias de una sola vez cuando se decide reubicar el trazado.

>[!NOTE]
>
> **Ejemplo de alias**
> 
> | Alias | Valor real del trazado |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>personalizado</b> | *D:\Dev\CustomProject\Substance* |
> 
> La biblioteca predeterminada se encuentra de forma predeterminada en *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*, y todos los gráficos que utilizan contenido predeterminado hacen referencia a este directorio. En lugar de hacer referencia a la ruta de acceso completa, se define un alias de &#39;<b>SBS</b>&#39; (sin comillas). En el caso de una biblioteca predeterminada, el valor exacto de la ruta SBS se establece tras la instalación en el directorio que el usuario elija para Designer.
> 
> Internamente, una referencia se modifica de la siguiente manera, cuando contiene una ruta con un alias:
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>blur\_hq.sbs**

<b>Las rutas de acceso relativas</b> siempre son relativas al archivo en el que están definidas. Esto significa que la ubicación actual del archivo de configuración determina la mayor parte de la ruta de acceso y las rutas de alias se basarán en ella, principalmente agregando una subcarpeta. <b>Esto significa que se recomienda encarecidamente colocar los archivos sbsprj junto a las carpetas que desea ver.</b>

Por ejemplo, tome un repositorio en *C:/Versioncontrol/Substance/* que contenga *CustomProject.sbsprj* y, a continuación, dos carpetas, */Base* y */Tools,* que contengan nodos.

Para definir dos alias relativos para Base y Tools se haría lo siguiente dentro del archivo SBSPRJ:

### C:/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


El resultado de este archivo de configuración es el siguiente:

**BaseAlias://** será *C:/Versioncontrol/Substance/Base/* y **ToolsAlias://** será *C:/Versioncontrol/Substance/Tools/.*

Si desea definir solo *C:/Versioncontrol/Substance/*, la ruta de acceso se mostraría como **&quot;file:.&quot;**, el punto que indica la ubicación del propio archivo.
