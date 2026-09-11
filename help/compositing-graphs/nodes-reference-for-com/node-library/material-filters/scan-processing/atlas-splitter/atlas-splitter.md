---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Utiliza el nodo de Atlas splitter para dividir los atlas de texturas en texturas individuales para procesar materiales escaneados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](atlas-splitter.resources/atlas-splitter.png "Icono de nodo")

<b>En:</b> Procesamiento De Escaneado/Filtros De Materiales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Toma una entrada de imagen atlas y divide todos los elementos separados como *materiales individuales*.

También se puede utilizar para reorganizar y mover todos los elementos a una cuadrícula.

El nodo funciona como una aplicación avanzada del nodo [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Vista de cuadrícula</b> <i>Booleano</i> | Muestra todas las formas detectadas en una cuadrícula. |
| <b>Opacidad de cuadrícula</b> <i>Flotador</i> | Establece la opacidad de las líneas de la cuadrícula cuando la vista de cuadrícula es verdadera. Opción Depurar |
| <b>Opacidad de selección de cuadrícula</b> <i>Flotador</i> | Establece la opacidad del resaltado de Selección de cuadrícula si la vista de cuadrícula es verdadera. Opción Depurar |
| <b>Escala automática</b> <i>Booleano</i> | Escale automáticamente las formas para que se ajusten a la celda de la cuadrícula. |
| <b>Recorte automático</b> <i>Booleano</i> | Recorta automáticamente el tamaño de salida según la forma más grande para minimizar el espacio vacío. |
| <b>Selección de forma</b> <i>Entero</i> | En la vista de cuadrícula, establece qué celda está resaltada, fuera de la vista de cuadrícula, establece qué celda se devuelve. |
| <b>Omitir forma menor que</b> <i>Flotador</i> | Omite las formas cuyo tamaño diagonal es inferior al valor especificado. |
| <b>Rotación automática</b> <i>Booleano</i> | Gira automáticamente la forma según la proporción de tamaño del cuadro delimitador. |
| <b>Rotación</b> <i>Flotador</i> | Ángulo de rotación de forma global |
| <b>Formato Normal De Entrada</b> <i>Entero</i> | Defina el formato de la entrada normal. Definir un formato incorrecto dará lugar a un resultado incorrecto. |
| <b>Disminuir escala de máscara de opacidad</b> <i>Entero</i> | Reduce la escala de la máscara de opacidad para eliminar el ruido potencial o los píxeles aislados. Evita la detección de formas no deseadas y también aumenta el rendimiento. |
| <b>Ancho de dilatación</b> <i>Flotador</i> | Aplica un efecto de dilatación basado en la máscara de opacidad en todos los canales excepto en Normal y Height. |
| <b>Habilitar Entradas Adicionales</b> <i>Booleano</i> | Hace que las entradas y la configuración de Usuario 1 y Usuario 2 estén disponibles para cualquier mapa adicional que no esté cubierto. |
| <b>Color de fondo personalizado</b> <i>Booleano</i> | Permite elegir un color de fondo personalizado, en lugar de una dilatación del contenido de esa capa. |
| <b>Color de fondo de color base</b> <i>Float3</i> | Color BG personalizado para el color base. |
| <b>Color de fondo normal</b> <i>Float3</i> | Color BG personalizado para Mapa normal. |
| <b>Color Metálico Del Fondo</b> <i>Flotador</i> | Color BG personalizado para Metálico. |
| <b>Color de fondo de rugosidad</b> <i>Flotador</i> | Color BG personalizado para rugosidad |
| <b>Color De Fondo De Height</b> <i>Flotador</i> | Color BG personalizado para Height |
| <b>Usuario 1 Bg Color</b> <i>Flotador</i> | Color BG personalizado para usuario personalizado 1 Mapa |
| <b>Color De Fondo Del Usuario 2</b> <i>Flotador</i> | Color BG personalizado para usuario personalizado 1 Mapa |
