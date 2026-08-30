---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/resources/warnings-from-dependencies.html"
breadcrumb-title: ''
description: Conozca las advertencias de las dependencias de recursos en Substance 3D Designer y cómo resolverlas.
helpx_creative_field: ""
helpx_description: Designer > Resources > Warnings from dependencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Advertencias de dependencias
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---


# Advertencias de dependencias

En esta página se enumeran las advertencias y los mensajes de error que pueden activar las dependencias de Substance 3D Designer y se ofrecen pasos comunes de solución de problemas para cada una de ellas.

Las dependencias son *otros archivos* a los que hace referencia un archivo Substance 3D (SBS). Incluyen [recursos](../../resources/resources.md) y otros archivos de Substance 3D a los que hacen referencia los nodos de [instancia de gráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).

## ![(error)](warnings-from-dependencies.resources/error.svg) Paquete dependiente no válido

No se puede cargar un paquete de dependencias porque falta, está dañado o es incompatible con la versión de Designer que se está utilizando.

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Existen dos formas principales de corregir este problema:

1. <b>Hacer que la carga de dependencia se realice correctamente</b>

   Compruebe que el paquete de dependencias existe en la ubicación especificada en el mensaje de advertencia. Si no es así, busque el archivo y vuelva a colocarlo en esa ubicación o vuelva a crearlo en su lugar. Si el archivo existe, *intenta cargarlo* en Designer y busca cualquier advertencia o error relacionado con ese paquete. Consulte los pasos de solución de problemas para esos problemas específicos y corríjalos en consecuencia.

   A continuación, vuelve a cargar el paquete host haciendo clic en RMB en él en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) y seleccionando la opción <b>Volver a cargar</b> en el menú contextual.

   ![&#39;Paquete dependiente no válido&#39; solución 1](warnings-from-dependencies.resources/warnings-dep-invalid-dependent-pkg.gif "&#39;Paquete dependiente no válido&#39; solución 1")
1. <b>Reubicar la dependencia en el paquete</b>

   Puede reubicar la dependencia mediante el [Administrador de dependencias](../../interface/dependency-manager/dependency-manager.md) . Haga clic en RMB en el paquete host en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) y seleccione la opción <b>Administrador de dependencias</b> en el menú contextual.

   Busque la dependencia que falta en la lista de Dependendy Manager, haga clic en RMB y seleccione <b>Reubicar...Opción </b>. Busque el paquete de dependencias en el cuadro de diálogo del explorador de archivos y haga clic en <b>Abrir</b>.

   A continuación, vuelve a cargar el paquete host haciendo clic en RMB en él en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) y seleccionando la opción <b>Volver a cargar</b> en el menú contextual.

   ![&#39;Paquete dependiente no válido&#39; solución 2](warnings-from-dependencies.resources/warnings-dep-invalid-dependent-pkg-2.gif "&#39;Paquete dependiente no válido&#39; solución 2")

## ![(error)](warnings-from-dependencies.resources/error.svg) Compruebe que el alias *&#39;X&#39;* está definido en el proyecto

Una de las dependencias o recursos del paquete se está cargando desde una ubicación [con alias](../../interface/preferences-window/project-settings/project-settings.md) en los datos del archivo Substance 3D (SBS) con el alias indicado en la advertencia, aunque ese alias no está definido en los [archivos de proyecto](../../interface/preferences-window/project-settings/project-settings.md) actuales.

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Al menos uno de los [archivos de proyecto](../../interface/preferences-window/project-settings/project-settings.md) debe definir el alias indicado en la advertencia.

![&#39;Comprobar alias definido&#39; solución](warnings-from-dependencies.resources/warnings-dep-alias.gif "&#39;Comprobar alias definido&#39; solución")

## ![(error)](warnings-from-dependencies.resources/error.svg) No se encuentra ningún archivo que coincida con este recurso

No se encuentran los archivos que coinciden con la *plantilla UDIM* para un [recurso de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md).

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Cuando un [recurso de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) está vinculado y Designer detecta una *taxonomía de nomenclatura UDIM* en su nombre de archivo, p. ej. `0x1` en `my_texture_0x1.png`, ofrece vincularlo como *plantilla UDIM*, de modo que los nodos [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) puedan *cambiar automáticamente* a otros mapas de bits en un conjunto UDIM utilizando esa taxonomía, al usar un flujo de trabajo UDIM en Designer. En ese caso, Designer vincula el recurso Bitmap de *otra forma* que tiene en cuenta la plantilla de numeración UDIM.

Existen dos formas principales de corregir este problema:

1. <b>Restaurar los archivos</b>

   Vaya a la ubicación especificada por el atributo <b>Ruta de archivo</b> del recurso y compruebe que existen los archivos que siguen a la plantilla. Si no lo hacen, restáurelos o recréelos.

   ![&#39;No hay ningún archivo que coincida con el recurso&#39; solución 1](warnings-from-dependencies.resources/warnings-dep-udim-2.gif "&#39;No hay ningún archivo que coincida con el recurso&#39; solución 1")
1. <b>Reubicar los archivos</b>

   Si los archivos se movieron o se les cambió el nombre, reubícalos haciendo clic en RMB en el elemento de recurso en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) y selecciona la opción <b>Reubicar</b> para vincular ese recurso al *primer archivo de un conjunto* de imágenes UDIM del mismo tipo.

   ![&#39;No hay ningún archivo que coincida con el recurso&#39; solución 2](warnings-from-dependencies.resources/warnings-dep-udim.gif "&#39;No hay ningún archivo que coincida con el recurso&#39; solución 2")

## ![(error)](warnings-from-dependencies.resources/error.svg) No se encontró el archivo vinculado

El archivo al que hace referencia un recurso vinculado no existe en la ubicación especificada por su atributo <b>Ruta de archivo</b>.

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Existen dos formas principales de corregir este problema:

1. <b>Restaurar el archivo</b>

   Vaya a la ubicación especificada por el atributo <b>File Path</b> del recurso y compruebe que el archivo existe. Si no lo hace, restáurelo o vuelva a crearlo.

   Solución ![&#39;Archivo vinculado no encontrado&#39; Solución 1](warnings-from-dependencies.resources/warnings-dep-file-not-found.gif "&#39;Archivo vinculado no encontrado&#39; Solución 1")
1. <b>Reubicar el archivo</b>

   Si el archivo se movió o se le cambió el nombre, reubícalo haciendo clic en RMB en el elemento de recurso en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) y selecciona la opción <b>Reubicar</b> para vincular ese recurso a otro archivo del mismo tipo.

   ![&#39;Archivo vinculado no encontrado&#39; solución 2](warnings-from-dependencies.resources/warnings-dep-file-not-found-2.gif "&#39;Archivo vinculado no encontrado&#39; solución 2")

## ![(error)](warnings-from-dependencies.resources/error.svg) No se encuentra el espacio de color

Un [recurso de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) hace referencia a un espacio de color que no se encuentra en el entorno actual de [administración de color](../../color-management/color-management.md). Puede ser un perfil ICC o un espacio de color en una configuración OCIO.

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

La lista de opciones para el atributo de espacio de color se rellena automáticamente con el espacio de color válido disponible. Cambie el valor del espacio de color de ese recurso por cualquier otra entrada de la lista.

Como alternativa, agregue ese espacio de color al entorno [administración de color](../../color-management/color-management.md) actual y reinicie Designer. Puede ser un perfil ICC o un espacio de color en una configuración OCIO.

>[!NOTE]
>
> Esta advertencia solo se activa cuando se usa un modo de administración de color que no sea **Heredado** (lo que es similar a deshabilitar la administración de color). Puede habilitar la administración de color en la sección **Administración de color** de la [configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md).

Solución ![&#39;No se encuentra el espacio de color&#39;](warnings-from-dependencies.resources/warnings-dep-color-space.gif "&#39;Solución no se encuentra el espacio de color&#39;")

## No se encontró el recurso de referencia ![(error)](warnings-from-dependencies.resources/error.svg)

El gráfico asignado al mosaico UV de un [recurso de escena 3D](../3d-scene-resource/3d-scene-resource.md) no se encuentra en la ubicación indicada en la advertencia.

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Existen dos formas principales de corregir este problema:

1. <b>Restaurar el gráfico</b>

   Compruebe el contenido del paquete en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) para ver el gráfico especificado en la lista <b>Mosaicos UV</b>. Si no existe, restáurelo o vuelva a crearlo.

   ![&#39;Recurso de referencia no encontrado&#39; solución 1](warnings-from-dependencies.resources/warnings-dep-udim-graph-2.gif "&#39;Recurso de referencia no encontrado&#39; solución 1")
1. <b>Seleccionar otro gráfico</b>

   Asigne otro gráfico del paquete al azulejo UV.

   ![&#39;Recurso de referencia no encontrado&#39; solución 1](warnings-from-dependencies.resources/warnings-dep-udim-graph.gif "&#39;Recurso de referencia no encontrado&#39; solución 2")

## ![(error)](warnings-from-dependencies.resources/error.svg) Los mosaicos UV se asignan varias veces

Un mosaico UV para un [recurso de escena 3D](../3d-scene-resource/3d-scene-resource.md) se asigna más de una vez a un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md).

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Para cada conjunto UV de un recurso de malla 3D, asegúrese de que no haya ningún índice UDIM presente *más de una vez* en la lista <b>Mosaicos UV</b>.

![&#39;Los mosaicos UV se asignan varias veces&#39; solución](warnings-from-dependencies.resources/warnings-dep-udim-same.gif "&#39;Los mosaicos UV se asignan varias veces&#39; solución")

## ![(error)](warnings-from-dependencies.resources/error.svg) Mosaicos UV no válidos

Un mosaico UV enumerado para un [recurso de escena 3D](../3d-scene-resource/3d-scene-resource.md) no está definido en la malla o está dañado.

<b>![(tick)](warnings-from-dependencies.resources/check.svg) Solución</b>

Para cada conjunto UV de un recurso de malla 3D, asegúrese de que todos los elementos de la lista <b>Mosaicos UV</b> hacen referencia a los UDIM que *existen* en el recurso vinculado.

>[!NOTE]
>
> Esta advertencia no se puede desencadenar a través de la interfaz de usuario, ya que *only* muestra los UDIM detectados en el recurso vinculado. Solo modificar los datos del archivo Substance 3D (SBS) *directamente* puede provocar esta advertencia.

![&#39;Solución de mosaicos UV no válida](warnings-from-dependencies.resources/warnings-dep-udim-invalid.gif "&#39;Solución de mosaicos UV no válida")
