---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de color de material para fusionar canales de color entre materiales para crear efectos de material compuesto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de color de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# Fusión de color de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## Fusión de color de material

**En:** *Filtros/Fusión De Materiales*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo permite realizar ajustes en un material completo multicanal mediante la fusión de colores sólidos en la parte superior. Esta es la principal diferencia con [Fusión de ajuste de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), que solo permite ajustes de tipo [Niveles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) en los canales, mientras que este nodo utiliza ajustes de tipo [Fusionar](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) con un color sólido.

Este nodo es muy útil cuando desea introducir una sugerencia de color plano en Color base o Difusión, o cuando desea &quot;acoplar&quot; otros canales mediante un valor de color sólido definido.

## Parámetros

### Entradas

* **IDcolor**: *Entrada de color*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Máscara de escala de grises**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo cuando utilice mapas de Specular/Brillo en lugar de Metálico/Rugosidad, por ejemplo.
* **Difusión**
  * **Color**: *(Valor de color)*Valor de color que se va a fusionar encima del canal de difusión.
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo.
  * **Modo De Fusión**: *Modo de fusión Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar* para usar en la operación.
* **Color base**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Normal**
  * **Origen**: *Height, máscara*
  * **Modo De Fusión**: *Combinar, Fusionar*
  * **Intensidad de Height**: *0.0 - 1.0*
  * **Opacidad del Height**: *0.0 - 1.0*
  * **Formato**: *DirectX, OpenGL*
* **Specular**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Emissive**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Brillo**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Rugosidad**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Metálico**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Specular level**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Oclusión de ambiente**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Height**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Opacidad**
  * Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión.
* **Máscara de ID de color**: *Falso/Verdadero* Usar Máscara de ID de color en lugar de máscara de escala de grises. Tenga en cuenta que esto es solo para un color!\
  Activa todas las opciones siguientes.
* **Color**: *(Valor de color)*Qué color seleccionar y convertir a blanco.
* **Rugosidad**: *0.01 - 1.0* Hasta qué punto el color que has elegido se fusiona con el color de tus vecinos.
* **Relleno**: *0.0 - 1.0* Contraste de transición del color elegido.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
