---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz de forma para añadir fuentes de luz con forma personalizada a entornos HDRI para conseguir efectos de iluminación creativos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# Luz de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-light.resources/panorama-shape.png){width="200px"}

<b>En:</b> Vista 3D > Herramientas HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una forma rectangular proyectada esféricamente. La transformación de la forma se controla mediante un gizmo de transformación.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de imagen de fondo</b> <i>Entrada de color</i> | Fondo opcional sobre el que componer la luz generada. |
| <b>Entrada de imagen de forma</b> <i>Entrada de color</i> | Imagen opcional para asignar a la luz Esfera. Solo se usa cuando el modo Color de forma está establecido en Entrada de imagen. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Matriz de formas</b> |  |
| <b>Matriz</b> <i>(Matriz de transformación)</i> | Control de transformación para el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Desplazamiento</b> <i>-2.0 - 2.0</i> | Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Forma</b> <i>Rectángulo, disco</i> | Elige la forma que quieres colocar. |
| <b>Modo de color de forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagen</i> | Elija el método que desee utilizar para definir el color de la forma. La entrada de imagen permite utilizar la segunda ranura de entrada. |
| <b>Color</b> <i>(Valor de color)</i> | Solo con el modo Color de forma establecido en RGB. Selecciona el color de la forma. |
| <b>Temperatura de forma</b> <i>800.0 - 20000.0</i> | Solo con el modo Color de forma establecido en Temperatura. Establece el valor Kelvin para el color de la forma. |
| <b>Gamma de entrada de imagen de forma</b> <i>sRGB, lineal</i> | Solo con el modo Color de forma establecido en Entrada de imagen. Determine cómo interpretar la entrada de imágenes de formas. |
| <b>Exposición de forma (EV)</b> <i>0.0 - 10.0</i> | Defina el valor de exposición para la forma generada, que se corresponde perfectamente con el valor de exposición de la imagen de fondo. |
| <b>Dureza de forma</b> <i>0.0 - 1.0</i> | Defina la dureza de los bordes de la forma. |
| <b>Exposición de zona interactiva (EV)</b> <i>0.0 - 10.0</i> | Definir exposición de zona interactiva central. Tenga en cuenta que esto no es muy visible en el modo de RGB. |
| <b>Tamaño de zona interactiva</b> <i>0.0 - 1.0</i> | Tamaño de la zona interactiva central. |
| <b>Difuminación de zona interactiva</b> <i>0.0 - 1.0</i> | Caída del punto de conexión central. |
| <b>Posición de zona interactiva</b> <i>0.0 - 1.0</i> | Posición X e Y de la zona interactiva central. |
| <b>Habilitar entrada de fondo</b> <i>Falso/Verdadero</i> | Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido. |
| <b>Gama de fondo</b> <i>sRGB, lineal</i> | Si se utiliza Entrada en segundo plano, defina cómo interpretar la entrada en segundo plano. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-light.resources/shape-light-ex.gif" />
        </td>
    </tr>
</table>
