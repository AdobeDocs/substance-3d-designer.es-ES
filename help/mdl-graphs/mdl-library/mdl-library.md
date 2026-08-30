---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: Acceda a la biblioteca del lenguaje de definición de materiales de Substance 3D Designer para crear materiales personalizados.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Biblioteca MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Biblioteca MDL

Esta página presenta la biblioteca de contenido relacionado con [gráficos MDL](../../mdl-graphs/mdl-graphs.md) y materiales incluidos en Substance 3D Designer. También se explica cómo instalar y administrar contenido personalizado en [Library](../../interface/the-library/the-library.md).

## Contenido MDL en la biblioteca

Los nodos que se pueden usar en gráficos MDL están disponibles en la sección <b>mdl</b> de la [Biblioteca](../../interface/the-library/the-library.md). Los nodos se organizan en filtros de acuerdo con el módulo MDL en el que se definen.\
Si los módulos se almacenan en subcarpetas, esta jerarquía se *reflejará* en la biblioteca como *categorías*.

Esta sección incluye contenido de las siguientes fuentes:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Contenido incorporado

Designer incluye módulos MDL, que contienen los componentes básicos para la creación de gráficos MDL, así como definiciones completas de materiales listas para usarse.

Este contenido se almacena en esta ubicación en el directorio de instalación : `./resources/view3d/iray/`

### Contenido personalizado

Además del contenido integrado, puedes agregar *tus propios* módulos MDL a la biblioteca.

De hecho, cualquier módulo MDL que se encuentre bajo los directorios enumerados en la sección <b>MDL</b> de la [configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md) se agrega a esta sección *cumulativamente* en los archivos del proyecto.

### NVIDIA vMaterials

Si la biblioteca [vMaterials](https://developer.nvidia.com/vmaterials) de NVIDIA está instalada, se *agrega automáticamente* a la biblioteca en su *propia categoría*.

</td>
<td style="border: 0;" valign="top">

![Recursos MDL en la biblioteca](mdl-library.resources/mdl-library.png "Recursos MDL en la biblioteca")

La sección &quot;mdl&quot; de *en la biblioteca, la biblioteca de vMaterials y el contenido personalizado se enmarcan*

</td>
</tr>
</table>

## Contenido MDL en la vista 3D

Todos los módulos MDL disponibles en la biblioteca se pueden usar en la [vista 3D](../../interface/3d-view/3d-view.md) cuando se usa el procesador Iray.

Abra el menú <b>Materiales</b> y abra un submenú de *material de escena* para examinar los módulos MDL disponibles. Las listas incluyen:

* Contenido incorporado
* Contenido personalizado
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* Se cargaron [gráficos MDL](../../mdl-graphs/mdl-graphs.md)

![Materiales MDL en el Vista 3D](mdl-library.resources/mdl-apply-in-3dview-material-list.png "Materiales MDL en el Vista 3D")

*Materiales MDL en el Vista 3D*
