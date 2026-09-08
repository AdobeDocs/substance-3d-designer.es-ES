---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/cross-section.html"
breadcrumb-title: ''
description: Utilice el nodo Sección transversal para crear máscaras de sección transversal basadas en mapas de height para los efectos de corte y corte en sectores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Cross Section
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sección transversal
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Sección transversal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icono de nodo ![&#39;Sección cruzada&#39;](../../../../../../assets/cross-section-2.png "&#39;Sección cruzada&#39; icono de nodo"){width="200px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja un perfil de sección transversal de una entrada. Se puede ajustar para dividir en vertical u horizontal, y tiene controles para el estilo de dibujo y el desplazamiento y escala de gráficos.

</td>
</tr>
</table>

Este nodo es especialmente útil para depurar y analizar mapas de alto. proporcionándole una vista de perfil de píxeles perfecta, sin necesidad de nodos complejos ni de una configuración larga y menos precisa en la vista 3D.

También se puede utilizar para crear formas y siluetas 2D difíciles de conseguir de otra manera. Combinado con un [nodo de curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)puede visualizar directamente el perfil de curva aplicado a un degradado lineal.

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Coordenada de sección cruzada</b> *Flotador* | Definir en qué coordenada muestrear el sector. Puede ser la coordenada X o Y dependiendo del eje de sección. |
| <b>Eje de sección</b> *Entero* | Defina si el sector es vertical u horizontal. |
| <b>Mostrar ayudante</b> *Booleano* | Activa una superposición que muestra la posición de la sección sobre la imagen de entrada. |
| <b>Configuración auxiliar</b> |  |
| <b>Escala auxiliar</b> *Flotador* | El tamaño de la superposición expresado como múltiplo, donde 1.0 es la imagen completa. |
| <b>Posición auxiliar</b> *Float2* | Posición (X, Y) de la superposición en la imagen de salida, donde (0,0, 0,0) es superior izquierdo y (1,0, 1,0) es inferior derecho. |
| <b>escala de Height</b> *Flotador* | Reduce el gráfico completo. Útil para la visualización de HDR. |
| <b>desplazamiento de Height</b> *Flotador* | Desplaza el gráfico entero hacia arriba o hacia abajo. Útil para la visualización de HDR. |
| <b>Estilo de dibujo</b> *Entero* | Cambiar entre relleno sólido y dibujo de líneas. |
| <b>Invertir degradado</b> *Booleano* | Si Estilo de dibujo está establecido en *Degradado* o *Degradado reflejado*, le permite invertir ese degradado sin afectar al fondo.<br><br>*Nota:* Solo está disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Degradado&#39; o &#39;Degradado reflejado&#39;. |
| <b>Suave / poligonal</b> *Booleano* | Cambia la forma entre un perfil suave perfecto o entre un perfil poligonal irregular.<br><br>*Nota:* Solo está disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Sólido&#39;, &#39;Degradado&#39; o &#39;Degradado reflejado&#39;. |
| <b>Importe del segmento</b> *Entero* | Establece la cantidad de segmentos utilizados para dibujar en estilo poligonal o en estilo de línea.<br><br>*Nota:* Solo está disponible cuando &#39;Suavizado / poligonal&#39; está establecido en &#39;poligonal&#39; o cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Línea&#39;. |
| <b>thickness de línea</b> *Flotador* | Establece el thickness de la línea.<br><br>*Nota:* Solo está disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Línea. |
| <b>Estilo de línea</b> *Entero* | Permite elegir el color y el difuminado de la línea.<br><br>*Nota:* Solo está disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Línea. |
| <b>smoothness de línea</b> *Flotador* | Establece el difuminado de degradado de la línea.<br><br>*Nota:* Solo está disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Línea. |
| <b>Color</b> *Flotador* | Color de escala de grises de la línea o forma.<br><br>*Nota:* Solo está disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Sólido&#39; o &#39;Línea&#39; y &#39;Estilo de línea&#39; está establecido en &#39;Suavizado&#39; o &#39;Sólido&#39;. |
| <b>Color de fondo</b> *Flotador* | Color de escala de grises del fondo.<br><br>*Nota:* No disponible cuando &#39;Estilo de dibujo&#39; está establecido en &#39;Línea&#39; y &#39;Estilo de línea&#39; está establecido en &#39;Id. de segmento&#39; o &#39;Degradado a lo largo de la línea&#39;. |

## Ejemplos

![Sección transversal: ejemplo 1](../../../../../../assets/cross-section-example-01.gif "Corte transversal: ejemplo 1")

![Sección transversal: ejemplo 2](../../../../../../assets/cross-section-example-02.gif "Corte transversal: ejemplo 2")

![Sección transversal: ejemplo 3](../../../../../../assets/cross-section-example-03.png "Corte transversal: ejemplo 3")

![Sección transversal: ejemplo 4](../../../../../../assets/cross-section-example-04.png "Corte transversal: ejemplo 4")
