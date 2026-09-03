---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: Solución de problemas de visualización 3D en Substance 3D Designer, incluidos problemas de procesamiento, visualización y rendimiento.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemas de visualización en 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---


# Problemas de visualización en 3D

Esta página enumera problemas técnicos relacionados con la [vista 3D](../../interface/3d-view/3d-view.md) de Substance 3D Designer y ofrece pasos de solución de problemas para cada uno.

## Bajo rendimiento: No se utiliza la GPU discreta

**![(error)](3d-view-issues.resources/error.svg) Problema**

Substance 3D Designer no usa la *GPU discreta* (<b>dGPU</b>) del sistema y usa la *GPU integrada* (<b>iGPU</b>) en su lugar. El resultado es un rendimiento bajo al procesar gráficos o la [vista 3D](../../interface/3d-view/3d-view.md).

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Los sistemas con gráficos intercambiables pueden *forzar la dGPU*, que debe usarse para una *aplicación específica* en software dedicado, según el fabricante de la GPU.

Por ejemplo, los usuarios con una <b>Nvidia dGPU</b> pueden hacer lo siguiente:

1. Cerrar Substance 3D Designer
2. Abra el <b>Panel de control de NVIDIA</b>
3. Vaya a la pantalla <b>Administrar configuración 3D</b> en la sección <b>Configuración 3D</b>
4. Busque la entrada &quot;Substance 3D Designer&quot; en la pestaña <b>Program Settings</b>
5. Seleccione <b>Procesador NVIDIA de alto rendimiento</b> en el cuadro combinado <b>GPU preferido</b>
6. Iniciar Substance 3D Designer

>[!WARNING]
>
> Tenga en cuenta que las GPU integradas (iGPU) *no son compatibles*. Puede obtener más información en la página [Requisitos del sistema](../../getting-started/system-requirements/system-requirements.md).

## El objeto 3D es plano

**![(error)](3d-view-issues.resources/error.svg) Problema**

Un objeto 3D que presentaba volúmenes detallados en una sesión se vuelve plano en la siguiente sesión, sin embargo el gráfico no ha cambiado y el mapa de altura lleva los mismos datos.

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

El efecto de deformación de un objeto 3D según un mapa de altura se realiza mediante una técnica denominada **desplazamiento de teselación**. Esta técnica implica dos pasos:

1. **Mosaico**: la geometría del objeto está *subdividida* en vértices, lo que da como resultado una *geometría más densa* para admitir detalles de volumen más precisos
2. **Desplazamiento**: los vértices se *mueven*, es decir, se desplazan, a lo largo de su *vector normal*. El vector normal sigue la dirección en la que se encuentra un polígono y tiene una magnitud (es decir, longitud) de 1

Se conoce el desplazamiento *direction*: la dirección del vector normal.\
El desplazamiento *distancia* que se debe recorrer para mover los vértices se calcula de la siguiente manera: `Distance = Height scale * Height map`. Dado que el mapa de altura *no ha cambiado* en el gráfico, se sale de la **escala de Height**.

El valor de escala de Height predeterminado es **1.0**, lo que puede provocar un efecto de desplazamiento *no perceptible*, dependiendo de la malla mostrada en la Vista 3D y del mapa de altura aplicado a ella.

Este valor se puede modificar de las siguientes maneras:

| En la vista 3D | En la vista de gráfico |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Use el **Desplazamiento emergente** en la barra de herramientas de la izquierda.<br>Obtenga más información en la [página dedicada](../../interface/3d-view/displacement/displacement.md). | Cree un nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) y establezca el uso de `heightScale` en sus propiedades.<br>Proporcione un valor a este resultado con un valor, usando un [nodo de Flotante constante](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats) por ejemplo, y luego *vuelva a aplicar el gráfico* en la Vista 3D. |

>[!TIP]
>
> Con este método, puede establecer un valor de escala de Height personalizado *por gráfico*, que le permite ajustarlo para que coincida con el material específico de ese gráfico.

## La vista 3D es completamente negra

**![(error)](3d-view-issues.resources/error.svg) Problema**

En las versiones 15.0.0 y posteriores, la ventana gráfica de la vista 3D es de color negro liso. Veo algunas superposiciones de texto (p. ej., muestras y tiempo de procesamiento), pero la escena 3D no es visible.

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Versión 15.1 y superior

Los nuevos procesadores 3D se actualizaron en la versión 15.1 y requieren controladores de GPU recientes. Actualice los controladores de la GPU del sistema a la versión más reciente.

Puede encontrar controladores aquí:   [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Versión 15.0 y posteriores

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) presentó nuestros nuevos [procesadores 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) internos que usan tecnologías modernas y, por lo tanto, no son compatibles con GPU más antiguas.

Las GPU compatibles incluyen NVIDIA RTX serie 20 (Turing) o superior, según los [requisitos del sistema](../../getting-started/system-requirements/system-requirements.md) de Designer.

Puede seguir utilizando el procesador OpenGL de forma predeterminada, utilizando la opción [new en la configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md):

1. Vaya a Editar > Preferencias > Proyectos
2. Seleccione el último archivo de proyecto de la lista
3. En la lista de archivos de proyecto, seleccione la ficha Vista 3D
4. Establezca la opción &quot;Procesador predeterminado&quot; en &quot;OpenGL (obsoleto)&quot;.
5. Haga clic en Aceptar para validar los cambios

Ahora, toda la nueva vista 3D utilizará el procesador OpenGL de forma predeterminada, lo que le permitirá seguir trabajando como antes.

>[!NOTE]
>
> El mismo problema y los mismos pasos de solución de problemas se aplican a la mayoría de las GPU AMD e Intel, que actualmente *no son compatibles* con nuestros nuevos procesadores 3D.

>[!IMPORTANT]
>
> El procesador OpenGL está *obsoleto* y es posible que se elimine de Designer en el futuro. Se recomienda actualizar la GPU del sistema para evitar interrupciones en el flujo de trabajo y garantizar una asistencia continua.

## Se muestra el mensaje &quot;Procesador no compatible&quot;

**![(error)](3d-view-issues.resources/error.svg) Problema**

En las versiones 15.0.0 y posteriores, el mensaje &quot;Procesador no compatible&quot; aparece en la esquina inferior derecha del puerto de visualización al utilizar los nuevos procesadores 3D (rasterizador, trazador de rutas de GPU). La escena 3D no es visible.

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) presentó nuestros nuevos [procesadores 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) internos que usan tecnologías modernas y, por lo tanto, no son compatibles con GPU más antiguas.

Las GPU compatibles incluyen NVIDIA RTX serie 20 (Turing) o superior, según los [requisitos del sistema](../../getting-started/system-requirements/system-requirements.md) de Designer.

En la configuración predeterminada, la Vista 3D volverá automáticamente al procesador de OpenGL si la opción &quot;Procesador predeterminado&quot; está establecida en &quot;Predeterminado (procesador predefinido)&quot; en [Configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md).

Puede encontrar y ajustar esa opción siguiendo estos pasos:

1. Vaya a Editar > Preferencias > Proyectos
2. Seleccione el último archivo de proyecto de la lista
3. En la lista de archivos de proyecto, seleccione la ficha Vista 3D
4. La opción &quot;Procesador predeterminado&quot; aparece en la configuración de la pestaña

>[!NOTE]
>
> Actualmente, solo las GPU de la <b>serie NVIDIA GTX</b> se pueden detectar como no compatibles.
> 
> Sin embargo, la mayoría de las GPU AMD e Intel tampoco son compatibles y producirán un renderizado en negro sin mensaje. Consulte el elemento &quot;La Vista 3D está totalmente en negro&quot; que aparece arriba para obtener ayuda sobre estas GPU.

>[!IMPORTANT]
>
> El procesador OpenGL está *obsoleto* y es posible que se elimine de Designer en el futuro. Se recomienda actualizar la GPU del sistema para evitar interrupciones en el flujo de trabajo y garantizar una asistencia continua.

## El objeto 3D se ve completamente suave

**![(error)](3d-view-issues.resources/error.svg) Problema**

Después de trabajar en los datos enviados al **Height** [salida](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), el objeto parece tener algo de volumen, pero *parece completamente suave*, como si la información del height se omitiera en el sombreado.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Asegúrese de que los datos de height *se convierten en normales* que están conectados a la **salida](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)** Normal[.

Al usar la técnica **Desplazamiento de teselación** (ver &quot;El objeto 3D es plano&quot; más arriba), los objetos pueden *deformarse* para seguir los datos del height, pero su superficie *no reaccionará a la luz de forma diferente* hasta que sus *normales* también se modifiquen para tener en cuenta los datos del height.

La solución es bastante simple: conecte el último nodo de la secuencia que conduce a la salida del Height a un nodo [Normal](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). Ajuste el parámetro **Intensity** de ese nodo según el material en el que esté trabajando y conecte el nodo Normal a la salida **Normal**.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](3d-view-issues.resources/3d-view-issues-01.gif){width="256px"}

</td>
</tr>
</table>

## El procesamiento es borroso o pixelado

**![(error)](3d-view-issues.resources/error.svg) Problema**

La imagen representada se ve borrosa o pixelada cuando el sistema usa *escala de visualización*.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

De forma predeterminada, Designer utiliza la resolución de visualización *escalada* para definir la resolución de representación de la [vista 3D](../../interface/3d-view/3d-view.md). Puede cambiar esta opción para que se utilice la resolución de visualización *nativa* en su lugar para un procesamiento nítido.

Abra el menú **Editar** y seleccione **Preferencias...Opción**. En la ventana [Preferencias](../../interface/preferences-window/preferences-window.md), abre la sección **Vista 3D** y establece el parámetro **Escala de ventana gráfica** en *Ninguno*.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](3d-view-issues.resources/3d-view-issues-02.png){width="256px"}

</td>
</tr>
</table>

## No puedo encontrar la propiedad del &#39;factor de teselación&#39;

**![(error)](3d-view-issues.resources/error.svg) Problema**

Después de actualizar Designer a la versión 15.0.0, no puedo encontrar el parámetro &quot;Factor de teselación&quot; en las propiedades del material donde solía estar.

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Al utilizar los nuevos procesadores (rasterizador y Trazador de ruta de GPU), el &quot;factor de teselación&quot; se encuentra en las propiedades de estos procesadores. En la vista 3D, vaya a <b>Procesador > Editar configuración</b>. La propiedad se mostrará en el conjunto acoplado Propiedades.

>[!NOTE]
>
> El ámbito de la teselación varía según el procesador:
> 
> * Rasterizador/Trazador de ruta de GPU: un valor único aplicado global a toda la escena.
> * OpenGL: un valor por material.
> * Iray: un valor por malla.

## Los objetos 3D tienen un aspecto incorrecto: su sombreado no se adapta a la iluminación

**![(error)](3d-view-issues.resources/error.svg) Problema**

El sombreado de los objetos se basa en sus vectores normales, tangentes y binormales. Sus coordenadas utilizan el intervalo `[-1, 1]`, mientras que los mapas de normales utilizan el intervalo `[0, 1]` en la mayoría de los casos. Para adaptar los valores de uno a otro, se debe aplicar un sesgo y una escala de <b>y</b>: `value * scale + bias`.

Por ejemplo, una escala de 2 y un sesgo de -1 adapta el valor x de `[0, 1]` a `[-1, 1]` de esta forma: `x * 2 - 1`.

Designer no aplica una escala ni un sesgo normales a menos que se especifiquen mediante una malla 3D. Si falta esa información, se genera una advertencia en la consola al [reemplazar cualquiera de sus materiales](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md):

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Para escenas exportadas a formatos USD hace un tiempo: Vuelva a exportar la escena con una versión reciente de USD, que incluirá los datos necesarios. Preste atención a las propiedades relacionadas con la escala normal y el sesgo, si los hay, lo que dependerá del software utilizado para exportar la escena.

Cuando [se reemplaza un material](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), Designer procesa la malla y calcula los datos que faltan en relación con sus normales, tangentes y binormales. Si la escala y el sesgo predeterminados de Designer coinciden con los requeridos para la malla, la malla se verá correcta cuando se reemplace.

## Bloqueo al iniciar la vista 3D

**![(error)](3d-view-issues.resources/error.svg) Problema**

Designer se bloquea al iniciar la vista 3D, al crear un proyecto, cargar un proyecto o iniciar manualmente una vista 3D.

**![(marca)](3d-view-issues.resources/check.svg) Pasos recomendados**

Primero, asegúrate de que tu sistema cumple con los [requisitos del sistema](../../getting-started/system-requirements/system-requirements.md) de Designer.

A continuación, actualice los controladores gráficos. Puede encontrar los controladores más recientes para la GPU siguiendo estos vínculos:   [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Si tu sistema incluye tanto una GPU integrada (iGPU) como una GPU discreta (dGPU), asegúrate de *actualizar los controladores de*.

A continuación, desactive cualquier software que pueda inyectar o superponer datos en un proceso de gráficos 3D. Algunos ejemplos son:

* Inyectores de postproceso como ReShade
* Superposiciones como cursores personalizados o métricas de rendimiento de GPU
* Software de captura de pantalla para grabar, transmitir o compartir gráficos en 3D en tiempo real
