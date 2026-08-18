---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de materiales para fusionar materiales enteros mediante máscaras para crear efectos de materiales compuestos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de materiales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Fusión de materiales

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## Fusión de materiales

**En:** *Filtros/Fusión De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Mezcla de materiales es el equivalente multicanal de material completo de [el nodo de mezcla atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Se mezcla entre dos materiales completos (todos los canales posibles) basados en una máscara de escala de grises, u opcionalmente basados en un solo color de una Máscara de ID de color.

Este nodo es útil si desea fusionar dos materiales y tener un mapa en escala de grises, pero no un ID de color completo. Si tienes una torta con ID de color y deseas mezclar más de dos materiales, te recomendamos que uses [Mezcla de varios materiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

## Parámetros

### Entradas

* **IDcolor**: *Entrada de color*\
  Mapa de ID de color al horno opcional.
* **Máscara de escala de grises**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo cuando utilice mapas de Specular/Brillo en lugar de Metálico/Rugosidad, por ejemplo.
* **Difusión**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Color base**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Normal**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
* **Specular**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Emissive**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Brillo**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Rugosidad**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Metálico**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Specular level**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Oclusión de ambiente**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Height**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Opacidad**
  * **Opacidad**: *0.0 - 1.0*\
    Fusión de opacidad entre primer plano y fondo
  * **Modo De Fusión**: *Normal, Agregar, Restar, Multiplicar, Agregar/Separar, Máx., Mín., Cambiar*
* **Máscara de ID de color**: *Falso/Verdadero* Usar Máscara de ID de color en lugar de máscara de escala de grises. Tenga en cuenta que esto es solo para un color!
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
