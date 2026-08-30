---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: Aprenda a administrar el contenido y los filtros personalizados en la biblioteca de Substance 3D Designer para el acceso organizado a los recursos.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Administración de contenido y filtros personalizados
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# Administración de contenido y filtros personalizados

Esta página explica el método para crear categorías y filtros para administrar contenido personalizado en la biblioteca. También incluye sugerencias para flujos de trabajo basados en proyectos.

## Información general

Después de [agregar contenido personalizado a la biblioteca](../../../interface/preferences-window/project-settings/project-settings.md), debes hacer que *sea detectable*.

La biblioteca utiliza varios *puntos de datos* para identificar contenido, con el fin de filtrarlo y mostrarlo en las búsquedas. Estos puntos de datos incluyen:

* Nombre
* Extensión
* URL (es decir, *nombre de archivo*)
* Atributos

Puedes organizar tu <b>biblioteca</b> en categorías que contengan filtros específicos y adaptarla a las necesidades de tu proyecto.\
De hecho, las categorías y filtros personalizados pueden ser *específicos del proyecto* y guardarse en [archivos de proyecto](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbsprj). Estos archivos se pueden ensamblar en [archivos de configuración](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbscfg) y distribuirse a un equipo para que todos los artistas puedan usar las* mismas categorías de <b>biblioteca</b>* para cualquier proyecto determinado.

Esto significa que con uno o más archivos de Project, puedes establecer las carpetas cuyo contenido debe agregarse a <b>Library</b>, así como las categorías y filtros que ordenarán y organizarán ese contenido.

![Contenido personalizado en la biblioteca](managing-custom-content-and-filters.resources/library-filters.png "Contenido personalizado en la biblioteca")

## Atributos de gráfico

Los gráficos contenidos en los archivos [SBS](../../../getting-started/overview/overview.md) y [SBSAR](../../../getting-started/overview/overview.md) se pueden *filtrar y buscar* en la biblioteca mediante el conjunto de datos de la sección [Atributos](../../../compositing-graphs/graph-parameters/graph-parameters.md) de las propiedades del gráfico. Algunos de estos atributos también se pueden establecer en otros [tipos de recurso](../../../resources/resources.md).

## Filtros y carpetas personalizados

Los filtros son parámetros de búsqueda booleanos simples (True/False) que harán que aparezca un recurso dentro de la biblioteca cuando se seleccione <b>Filter</b>. Los recursos pueden ser cualquier cosa guardada dentro de un paquete. Tenga en cuenta lo siguiente:

* Un <b>Filtro</b> coincidirá con todos los recursos, en *todas las rutas controladas*.
* Un <b>Filtro</b> puede contener varias condiciones, *todas ellas deben evaluarse como Verdadero* (Y-condición) para que el recurso aparezca bajo ese filtro.
* Un [recurso](../../../resources/resources.md) puede aparecer bajo varios filtros, pero *no es exclusivo* de ningún filtro.
* Un [recurso](../../../resources/resources.md) de una ruta de acceso controlada está *disponible* en la <b>biblioteca</b>, incluso si es *no* bajo ningún <b>filtro</b>, mediante la función <b>Buscar</b>.

### Cómo crear filtros y carpetas

Las categorías (es decir, carpetas) y los filtros se crean y editan mediante los siguientes botones:

<b>![](managing-custom-content-and-filters.resources/library-icon-new-folder.png) Agregar carpeta:</b> Crea una carpeta expansible en la vista de biblioteca. *no puede* crear subcarpetas.

<b>![](managing-custom-content-and-filters.resources/library-icon-new-filter.png) Agregar filtro:</b> Agrega un nuevo filtro dentro de la carpeta seleccionada. *no puede* agregar filtros a las carpetas predeterminadas existentes.

<b>![](managing-custom-content-and-filters.resources/library-icon-edit.png) Editar elemento:</b> Edita la carpeta o el filtro seleccionados actualmente. *No se puede* editar ninguna de las propiedades de Carpetas y filtros predeterminados.

Para *quitar* una carpeta o un filtro, *haz clic con el botón derecho* en él y selecciona la opción <b>Quitar</b> del menú contextual.

### Edición de filtros y carpetas

Las <b>carpetas</b> y <b>filtros</b> se identifican mediante los siguientes datos:

* <b>Nombre</b> se muestra en la vista de árbol de la biblioteca.
* [Archivo de configuración del proyecto (SBSPRJ)](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) en el que se almacena este elemento.

>[!WARNING]
>
> Es *muy* importante configurarlas correctamente para asegurarte de que editas el *proyecto correcto*.

![Edición de filtro personalizado](managing-custom-content-and-filters.resources/library-filters-edit.png "Edición de filtro personalizado")

**Los filtros** suelen necesitar tener *condiciones* configuradas para lograr su propósito de filtrado. Estas condiciones se configuran según los siguientes criterios:

* **Tipo de recurso**: establece un [tipo de recurso](../../../resources/resources.md) específico, como [gráficos](../../../compositing-graphs/substance-compositing-graphs.md)
* **Atributo** al que aplicar la condición: consulte la lista anterior
* **Lógica de la condición**: permite que el filtro incluya resultados con coincidencias positivas, negativas, parciales y completas
* **Palabra clave Condition:** cadena con la que se comprueban los criterios **Attribute** y **Condition logic**. Cuando se deja en blanco, se incluye cualquier recurso que coincida con estos dos criterios

Puede *agregar o quitar* condiciones mediante los botones &#39;**+**&#39; y &#39;**x**&#39; situados en el extremo derecho de la palabra clave Condition.

>[!NOTE]
>
> Un filtro sin ninguna condición configurada hará que se muestre *todo el contenido de **Biblioteca**&#x200B;de*.

## Prácticas recomendadas

### Directrices recomendadas

* La regla general para la biblioteca predeterminada es que <b>Folder</b> aparece en el atributo <b>Category</b>, mientras que el nombre <b>Filter</b> está determinado por el atributo <b>Tag</b>
* No crees nodos personalizados que se mezclen con la biblioteca predeterminada a menos que *explícitamente* lo desees. Tus nodos *aparecerán* en Filtros predeterminados si coinciden, así que tendrás que asegurarte de usar un *sistema de etiquetado/nomenclatura diferente* para evitar eso
* Usar identificadores *únicos* y *por proyecto*. Estos se pueden colocar donde quieras (como <b>Descripción</b>, <b>Categoría</b> o <b>Datos de usuario</b>), siempre y cuando seas *consistente* entre todos los proyectos. Esto facilita mucho la búsqueda y el filtrado del contenido *por proyecto*
* Utilice el atributo <b>Author</b> para realizar un seguimiento de la persona responsable inicialmente del contenido, sin tener que examinar los registros de Control de versiones
* Una forma eficaz de crear <b>iconos</b> es usar la opción <b>Generate</b> del atributo de gráfico [Icon](../../../compositing-graphs/graph-parameters/graph-parameters.md) o crear un gráfico [template](../../../interface/preferences-window/project-settings/project-settings.md) para generarlos. De esta manera, puede garantizar la coherencia y ahorrar trabajo al crearlas. Todos los iconos de biblioteca predeterminados se crearon en Designer de esta manera.

### Administración de contenido de ámbito variable

* Puede agregar recursos a *categorías existentes* si esto tiene más sentido. No será tan fácil administrar y mantener los filtros, y puedes usar un estilo de icono especial para *diferenciarlos*.
* Puedes definir tus carpetas y filtros en un *archivo global* (de nivel de estudio) de [configuración del proyecto](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) y, a continuación, agregarles contenido simplemente añadiendo rutas controladas de *archivos de proyecto*[&#128279;](../../../interface/preferences-window/project-settings/project-settings.md) consecutivos
* Puede definir carpetas y filtros específicos para *cada proyecto* para mantenerlos separados
* Puede mezclar, hacer coincidir y utilizar métodos de los tres anteriores: utilizar filtros existentes, definir nuevos filtros globales y crear filtros únicos por proyecto
