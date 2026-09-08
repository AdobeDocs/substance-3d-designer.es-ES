---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ''
description: Utilice el nodo Texto para generar texturas de texto con fuentes y estilos personalizables para crear patrones basados en texto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Texto

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Text](../../../../assets/comp_text_1.png "Atomic node: Texto"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

El nodo Texto proporciona una forma de colocar el texto creado por el usuario en los gráficos. Los usuarios también pueden seleccionar ajustes como Fuente, Alineación y Rotación para personalizar la colocación del texto.

El nodo Texto es muy potente y la única forma de colocar fácilmente el texto. Puede resultar un poco complicado de usar debido a que la colocación siempre se produce en un lienzo limitado y cuadrado, y a que las fuentes se controlan mediante una lista externa definida por el sistema.

</td>
</tr>
</table>

Solo se admiten fuentes Truetype (.ttf) y determinadas fuentes Opentype. Si faltan fuentes en la lista, probablemente sea esta la razón. <b>Las fuentes no se pueden exponer como parámetro.</b>

Cuando se publica en sbsar un gráfico que utiliza texto, la fuente se incrusta en el paquete, al igual que con los mapas de bits y otros recursos, para garantizar que funciona en todos los sistemas y aplicaciones.

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
| <b>Modo de color</b> *Booleano* | Alterna entre una imagen de salida en escala de grises y en color. |
| <b>Texto</b> *Cadena* | Determina la descripción del texto. |
| <b>Fuente</b> *Cadena* | El recurso de fuente utilizado para representar el texto. |
| <b>Tamaño de fuente</b> *Flotador* | Tamaño de fuente del texto en puntos. |
| <b>Alineación</b> *Entero* | Establece la alineación del texto como izquierda, centro (predeterminado) o derecha. |
| <b>Transformación</b> *Float4* | Matriz de transformación 2x2 aplicada al texto procesado. |
| <b>Posición</b> *Float2* | Posición del texto en la imagen de salida. |
| <b>Fondo</b> *Float/Float4* | Color de fondo de la imagen de salida. |
| <b>Color de fuente</b> *Float/Float4* | El color del texto. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Fondo</b> *Escala de grises/Color* PRINCIPAL | Color de fondo de la imagen de salida. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises/Color* |  |

## Ejemplos

*Próximamente.*
