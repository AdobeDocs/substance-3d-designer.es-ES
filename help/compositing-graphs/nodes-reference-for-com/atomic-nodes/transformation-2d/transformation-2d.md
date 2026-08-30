---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación 2D para aplicar transformaciones 2D a texturas, incluidas la traslación, la rotación y la escala.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación 2D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# Transformación 2D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Transformación 2D](transformation-2d.resources/comp_transformation_1.png "Nodo atómico: Transformación 2D"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Aplica una matriz de transformación 2D a una imagen: conversión, rotación, escala, simetría y distorsión.

Es bastante similar a Transformar (Ctrl-T) en Photoshop o a usar el manipulador de asignación 2D en Substance 3D Painter.

</td>
</tr>
</table>

Este es un nodo extremadamente útil y ampliamente aplicado, que permite aumentar el mosaico, eliminar el mosaico, colocar una imagen en una posición específica, estirar o aplastar una entrada, etc.

Sin embargo, no puede ser una coincidencia perfecta para ciertas aplicaciones, por lo que los siguientes nodos pueden ser de interés: [Transformación segura](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md), [Transformación no cuadrada](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md), [Transformación cuádruple](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md) y [Transformación trapezoide](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Desactivación del mosaico
> 
> Establezca el [método de herencia](../../../../glossary/glossary.md) del &#39;Modo de segmentación&#39; [parámetro base](../../../../glossary/glossary.md) en &#39;Absoluto&#39;, que luego le permite establecer el valor del parámetro en &#39;Sin segmentación&#39;:
> 
> ![](transformation-2d.resources/tilingmode.png)

>[!NOTE]
>
> Los valores de escala y rotación en las propiedades del nodo son *en relación con la transformación actual* y no se aplican a la vista 2D hasta que haga clic en el botón &quot;Aplicar&quot;.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Parámetros

|  |  |
| --- | --- |
| <b>Matriz de transformación</b> *Float4* | Abra el transformar matriz subyacente para la edición directa. Permite cambiar la rotación y la escala. También se puede ajustar mediante el gizmo en la vista 2D.   Advertencia: no se correlacionan directamente con la vista y son ajustes relativos que se pueden aplicar por pasos. |
| <b>Desplazamiento</b> *Float2* | Define el desplazamiento 2D de la imagen. Permite cambiar la posición o el desplazamiento También se puede ajustar mediante el gizmo en la vista 2D.   Se relaciona directamente con la salida de la vista 2D. |
| <b>Modo Mipmap</b> *Entero* | Permite cambiar a un nivel manual [mipmap](../../../../glossary/glossary.md), que reduce los artefactos de una imagen mediante el filtrado de texturas. |
| <b>Nivel de mapa MIP</b> *Entero* | Establece el nivel [mipmap](../../../../glossary/glossary.md) que se va a usar.     *Disponible cuando &#39;Mipmap mode&#39; está establecido en &#39;Manual&#39;* |
| <b>Color mate</b> *Float4* | El color utilizado como fondo cuando el mosaico de la transformación está desactivado. Es decir, establece el color utilizado cuando la entrada transformada no cubre un área de la salida.   Se puede hacer transparente si se trabaja en color RGBA. |
| <b>Filtrado</b> *Entero* | Define el método de disminución de resolución utilizado. No funciona particularmente bien con la reducción del Nivel de mapa MIP. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises/Color* PRINCIPAL | La imagen que se va a transformar. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises/Color* |  |

## Ejemplos

*Próximamente.*
