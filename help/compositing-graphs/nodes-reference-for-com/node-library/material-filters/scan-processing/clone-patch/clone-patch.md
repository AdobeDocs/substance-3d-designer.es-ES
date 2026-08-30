---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Parche de Clonar para clonar y parchear áreas de materiales escaneados para eliminar artefactos e imperfecciones.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parche de clonación
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# Parche de clonación

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-patch.resources/clone-patch.png){width="128px"}

![](clone-patch.resources/clone-patch-grayscale.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El parche de Clonar es un nodo procedimiento y paramétrico denominado &quot;Clonar Stamp&quot;. Clona un área de una entrada en otra, ocultando detalles potencialmente no deseados. Si bien no es tan rápido y fácil como usar una herramienta familiar en una aplicación basada en pincel, proporciona la ventaja clave de no ser destructivo y de trabajar dentro de un flujo de trabajo basado en nodos. Además, este nodo realiza un análisis inteligente del área de origen y de destino, e intenta fusionar las cosas lo mejor posible en función del contraste, los valores y las formas.

Esto está destinado principalmente a esos raros momentos en los que desea hacer una corrección manual de un área específica, en caso de que haya un detalle no deseado en algún lugar.

Tenga en cuenta que esto no funciona como un pincel estándar sencillo de &quot;Sello&quot;. La forma del área mezclada se basa en las formas y valores de las áreas con las que está trabajando, lo que significa que se trata de un nodo bastante pesado que requiere paciencia, pero ofrece excelentes resultados.

También es importante comprender el hecho de que puede mover el área de destino con un gizmo, pero el área de origen debe establecerse cambiando los parámetros de &quot;Matriz de origen&quot;.

>[!NOTE]
>
> Si desea esto para un material completo (como suele ser el caso), consulte [Parche de Clonar de materiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).
> 
> Para aquellos casos en los que desee realizar esta operación en varias entradas al mismo tiempo (sin que sea un material), consulte [Parche para varios Clonar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Es normal (solo para Color)</b> <i>Falso/Verdadero</i> | Establece si la entrada es un mapa normal y si la fusión debe tratarse como tal. |
| <b>Forma</b> <i>Cuadrado, disco</i> | Establece la forma del sello. Sólo se usa como base. |
| <b>Edge</b> |  |
| <b>Umbral</b> <i>0.0 - 1.0</i> | Define hasta dónde debe llegar el área mezclada. Esto crece en pasos, a lo largo de formas en el área de destino y tiene muy poco efecto con fondos uniformes<i>.</i> |
| <b>Desenfocar</b> <i>0.0 - 2.0</i> | Desenfoca los bordes del área de sello en caso de que sea necesaria una transición más suave. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Redondea los bordes de la forma de sello para que los contornos fluyan más suavemente. |
| <b>Resolución de cuadrícula</b> <i>1 - 11</i> | Define la resolución de calidad del análisis de fusión. Un valor más alto significa una fusión más precisa. |
| <b>Transformaciones</b> |  |
| <b>Matriz de origen</b> <i>(Matriz de transformación)</i> | Transforma el origen (Escala y rotación). No se puede realizar en el lienzo; cambie solo mediante estos parámetros. |
| <b>Desplazamiento de origen</b> <i>-0.5 - 0.5</i> | Traduce la ubicación de origen. No se puede realizar en el lienzo; cambie solo mediante estos parámetros. <i>Este parámetro es probablemente el principal que desea cambiar.</i> |
| <b>Matriz de destino</b> <i>(Matriz de transformación)</i> | Transforma la ubicación de destino (Escala y rotación). También se puede hacer a través de Gizmo en lienzo. |
| <b>Desplazamiento de destino</b> <i>-0.5 - 0.5</i> | Traduce la ubicación de destino. También se puede hacer a través de Gizmo en lienzo. |
