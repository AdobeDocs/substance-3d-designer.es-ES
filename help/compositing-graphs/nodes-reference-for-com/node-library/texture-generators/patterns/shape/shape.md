---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Utilice el nodo Forma para generar formas geométricas básicas para crear patrones y texturas en Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# Forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una variedad de formas de procedimiento, con opciones para modificar formas base. Las formas siempre están perfectamente interpoladas y son de alta precisión.

A pesar de su simplicidad, se trata de un nodo muy útil: es el bloque de construcción de la generación de Heightmap más procedimental! Combinando formas básicas con nodos de transformación, puede crear una forma de mapa de altura con todos los procedimientos que sea mucho más precisa que cualquier mapa de bits.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Mosaico</b> <i>1 - 16</i> | Define la cantidad de veces que el resultado debe aparecer en mosaico. |
| <b>Patrón</b> <i>Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media campana, Campana con bordes, Crescante, Cápsula, Cono, Hemisferio</i> | Selecciona la forma de motivo que se va a utilizar. |
| <b>Específico del patrón</b> <i>0.0 - 1.0</i> | Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Ajusta toda la forma. |
| <b>Tamaño</b> <i>0.0 - 1.0</i> | Permite el escalado no uniforme en los ejes X o Y. |
| <b>Ángulo</b> <i>0.0 - 1.0</i> | Gira toda la forma. |
| <b>Rotación 45°</b> <i>Falso/Verdadero</i> | Rota a 45 grados preestablecidos. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |
| <b>Mosaico no cuadrado</b> <i>Falso/Verdadero</i> | Cuando la Expansión no cuadrada está activada, esto segmentará la forma en mosaico sin aplastarla. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shape-ex.gif" />
        </td>
    </tr>
</table>
