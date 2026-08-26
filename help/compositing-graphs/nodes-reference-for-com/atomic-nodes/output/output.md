---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Salida
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# Salida

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Salida](../../../../assets/comp_output_1.png "Nodo atómico: Salida"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

El nodo Output especifica el <b>resultado</b> de un gráfico de Substance, o uno de sus resultados si hay más de un nodo Output presente en él.

Cualquier [nodo de instancia](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que represente este gráfico emite la imagen o el valor conectado al nodo de salida de un gráfico y puede [exportarse como salida de gráfico](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md).

</td>
</tr>
</table>

Del mismo modo, cuando un [archivo SBSAR publicado](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) incluye este gráfico, ese archivo puede generar esa imagen en cualquier integración o complemento que consuma el archivo.

Tiene una única ranura de entrada que no tiene en cuenta el tipo, lo que significa que se escribe a sí misma después del tipo de datos conectado a ella.

No tiene parámetros, sino más bien atributos que son de gran importancia para etiquetar adecuadamente el resultado y ponerlo a su uso previsto.

Cada gráfico de Substance debe tener *al menos un nodo de salida*. Si no existe ningún resultado, el gráfico nunca puede devolver un resultado real y se genera [warning](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md).

## Atributos

|  |  |
| --- | --- |
| <b>Identificador</b> *Cadena* | Identificador único de la salida. Esta propiedad no se puede dejar en blanco y no puede contener caracteres especiales ni espacios.   El identificador se utiliza porque la etiqueta del nodo es la propiedad &#39;Label&#39; que se deja en blanco. También se puede usar para nombrar [texturas exportadas](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). |
| <b>Descripción</b> *Cadena* | La descripción opcional que se utiliza como información sobre herramientas de la salida son los gráficos de Substance. |
| <b>Etiqueta</b> *Cadena* | Se utiliza como etiqueta para el nodo de salida y su conector correspondiente en [nodos de instancia](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que representan este gráfico. La etiqueta puede contener espacios y caracteres especiales. |
| <b>Datos de usuario</b> *Cadena* | Metadatos opcionales que pueden utilizarse para operaciones de filtrado específicas. [Substance 3D Painter](https://www.adobe.com/products/substance3d/apps/painter.html) usa estos datos para [controlar algunas características](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/user-data). |
| <b>Grupo</b> *Cadena* | Atributo utilizado para agrupar resultados para los [modos de creación de vínculos](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) de Designer.   Las salidas con un atributo &#39;Group&#39; idéntico se presentan como una única conexión en el modo de creación de vínculos &#39;Compact Material&#39;. |

## Atributos de integración

Estos son atributos que están pensados para ser utilizados por integraciones/complementos que consumen el gráfico en un [archivo SBSAR publicado](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).

Por lo tanto, no afectan al formato de [exportaciones de mapas de bits](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). Además, solo se usa el atributo <b>Usage</b> en Designer. Consulte los detalles a continuación.

<b>Uso</b>

|  |  |
| --- | --- |
| <b>Componente</b> *Cadena* | Se utiliza para asignar algunos canales de textura a las entradas de sombreado SVBRDF adecuadas en flujos de trabajo AxF. |
| <b>Uso</b> *Cadena* | Define el tipo y el uso del nodo de salida. Esta propiedad es importante ya que controla:<ul data-preserve-html="true"> <li data-preserve-html="true">Conexión de nodos en gráficos de Substance al utilizar [algunos modos de creación de vínculos](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) </li> <li data-preserve-html="true">Conexión de texturas a sombreados en la vista 3D (consulte a continuación: &#39;[Acerca de la función de los usos en la vista 3D](#usages-role-3dview)&#39;)</li> <li data-preserve-html="true">Conexión de texturas a materiales en integraciones/complementos</li> </ul> |
| <b>Espacio de color</b> *Cadena* | Define el espacio de color en el que se debe interpretar esta salida. Se utiliza en algunas integraciones de otras aplicaciones y no tiene ningún impacto en Designer. |

### Función de los usos en la vista 3D

Dado que las salidas de gráficos a menudo están pensadas para ser el resultado final de un canal de textura específico, las salidas se pueden enviar automáticamente al muestreador adecuado del sombreado utilizado en la vista 3D.

De hecho, una salida cuya propiedad <b>Usage</b> *coincida con un uso de muestra* en la vista 3D se conectará a ese muestreador. Por ejemplo, una salida con un uso de `basecolor` se conectará al muestreador `basecolor` del sombreador de vista 3D. Obtén más información en la sección [Ver datos en la vista 3D](../../../../interface/3d-view/3d-view.md) de la página [Vista 3D](https://substance3d.adobe.com/documentation/display/draftdesigner/.3d%20view%20vdraftversion).

Haga clic en RMB en un área vacía en la [vista de gráfico](../../../../interface/the-graph-view/the-graph-view.md) y seleccione la opción <b>Ver resultados en vista 3D</b> en el menú contextual para conectar todas las salidas a las muestras de vista 3D con *usos coincidentes*.

>[!IMPORTANT]
>
> Si se configuran varios usos para, por ejemplo, asignar usos a canales en una textura empaquetada, solo el *primer uso* de la lista se conectará a la vista 3D. Esta es una limitación conocida.

## Salida predeterminada

Cuando un gráfico tiene más de una salida, se puede establecer una de ellas como salida predeterminada para ese gráfico. Esto especifica para cuál de los resultados se debe utilizar:

* La miniatura de cualquier nodo de instancia que represente ese gráfico
* Visualización de estos nodos de instancia en la vista 2D
* La miniatura de ese gráfico en la biblioteca (aprende a agregar tus propios recursos [aquí](../../../../interface/preferences-window/project-settings/project-settings.md))

Esta función le permite organizar las salidas del gráfico en cualquier orden independientemente de cómo se visualizará el gráfico como un nodo.

Para definir un nodo de salida como salida por defecto de un gráfico:

* Haga clic con el botón derecho en un nodo Salida y seleccione la acción &#39;Establecer como salida predeterminada&#39; en el menú contextual.
* En las propiedades del nodo Salida, utilice el botón &#39;Establecer como predeterminado&#39; en el encabezado de la sección &#39;Atributos&#39;.

A continuación se muestra un ejemplo de nodos de instancia antes y después de definir una salida predeterminada:

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="../../../../assets/defaultouput2.png" alt="defaultouput2">
      <br><i>Antes</i>
    </td>
    <td style="border: 0">
      <img src="../../../../assets/defaultouput1.png" alt="defaultouput1">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
