---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Utilice el nodo Extrusión de forma para extruir formas y crear efectos de profundidad similares a 3D en texturas de Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusión de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# Extrusión de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## Extrusión de forma

**En:** *Generadores De Texturas**/Patrones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo avanzado que permite que las entradas binarias 2d de &quot;forma&quot; se representen en mapas de altura girados en 3D. Funciona de forma similar a una extrusión en un paquete 3D en el que se extruye una forma a lo largo de su eje, creando un volumen. En combinación con la máscara de degradado de perfil, también se pueden crear cuerpos de tipo Revolución/Torno. Muy útil para crear formas artificiales complejas para mapas de altura.

## Parámetros

### Entradas

* **Entrada de extrusión de forma**: *Entrada en escala de grises* Si la forma de extrusión se establece en Personalizada, puedes conectar tu propia máscara de forma binaria (preferiblemente) aquí.
* **Degradado de perfil**: *Entrada en escala de grises\
  Si Tipo de perfil está establecido en Degradado vertical, se puede utilizar para definir la escala de la forma a lo largo del eje, para cuerpos de revolución.*
* **Máscara de perfil**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para ocultar o mostrar la forma Extruida a lo largo de su eje. Se puede utilizar para romper la continuidad de la forma a lo largo de su eje. Sólo se interpreta como binario: los valores de posición de escala de grises se redondean a 0 o 1.

### Parámetros

* **Extruir Height**: *0.0 -* 1.0\
  Cantidad que se extruye la forma hacia arriba desde el centro.
* **Extruir Profundidad**: *0.0 - 1.0* Cantidad que se extruye la forma por aguas abajo desde el centro.
* **Extruir forma**: *Cubo, cilindro, entrada personalizada* Use formas integradas o escriba su propia forma personalizada externamente.
* **Tamaño de forma de extrusión**: *0.0 - 1.0* Solo se usa con el cubo y el cilindro incorporados, determina el tamaño de la forma base y se puede escalar de forma no uniforme.
* **Escala**: *0.0 - 1.0*\
  Establezca la escala global del efecto. Con Formas integradas, esta es una escala de forma base uniforme y no afecta al Height ni a la Profundidad.\
  Con la entrada personalizada, esto escala todo el resultado final de una manera uniforme.
* **Tipo de perfil**: *Degradado vertical, recto, máscara* Control principal para determinar el comportamiento del efecto y el uso de mapas de entrada adicionales opcionales.\
  Recto es el comportamiento de extrusión estándar, Degradado vertical permite valores de escala personalizados a lo largo de todo el eje, Máscara permite ocultar secciones a lo largo del eje por máscara.
* **Height biselado**: *0.0 - 1.0* Establece hasta dónde llega el bisel a lo largo del eje de extrusión.
* **Intensidad de bisel**: *0.0 - 1.0* Establece cuánto se retrae el bisel de la forma original.
* **Curva biselada**: *-1.0 - 1.0* Establecer curva cóncava o convexa del efecto Bisel. Un valor de 0 significa recto, sin curva.
* **Bisel simétrico**: *Falso/Verdadero* Alterne para aplicar bisel en la parte superior e inferior de la forma.
* **Multiplicador de escala reducida**: *0 - 2* Control de reducción de escala incorporado. Se puede utilizar para agregar rápidamente suavizado; asegúrese de aumentar también la resolución del nodo.
* **Posición**:\
  Control principal para la rotación de resultados en el espacio 3D. Se correlaciona con Gizmo de intersección en la vista 2D.
* **Intervalo de salida**: *[0, 1], [-1, 1]*Defina los valores mínimo y máximo de salida. Si el rango se establece en [-1,1], los valores negativos se presentan como negros.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
