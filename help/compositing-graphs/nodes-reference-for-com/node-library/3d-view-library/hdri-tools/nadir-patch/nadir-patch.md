---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Nadir patch para aplicar parches a la región nadir de los panoramas HDRI y corregir los defectos inferiores en los mapas de entorno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir patch

**En:** *Herramientas HDRI/vistas 3D*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo proporciona la funcionalidad de aplicar parches sobre el punto central del suelo (nadir) de una imagen asignada esféricamente. Se puede utilizar para ocultar o &quot;clonar&quot; un nadir feo, o cámara visible o trípode. Funciona como un [parche de clonación](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), pero con ajustes para imágenes asignadas esféricamente. El usuario selecciona un punto en otra parte de la imagen, es decir, el punto clonado y mezclado en el nadir. No se requieren otras entradas externas que no sean un único HDRI para procesar, pero se puede utilizar una máscara externa como alfa para el efecto de parche.

se puede comprobar y validar rápidamente con [Nadir extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md).

## Entradas

* **Entrada**: *Entrada de color*
* **Entrada de máscara**: *Entrada en escala de grises*\
  Ranura de máscara opcional utilizada para enmascarar el parche. Funciona como un alfa.

## Parámetros

* **Habilitar**: *Falso/Verdadero*\
  Activar o desactivar el efecto de aplicación de parches.
* **Ayuda para mostrar fotogramas**: *Falso/Verdadero*\
  Mostrar u ocultar las líneas auxiliares, con fines de depuración.
* **Thickness de fotogramas**: *0.0 - 1.0*\
  Thickness de líneas auxiliares.
* **Escala del parche**: *0.0 - 1.0*\
  Escala de parche global y uniforme. Afecta tanto al origen como al destino.
* **Tamaño de parche**: *0.0 - 1.0*\
  Tamaño no uniforme del parche.
* **Rotación de parche**: *0.0 - 1.0*\
  Rotación del parche. Afecta al origen y al destino.
* **Alpha de parches**: *Cuadrado suave, gaussiano, entrada de máscara*\
  Defina qué alfa se utiliza para fusionar el parche con el fondo.
* **Dureza del parche**: *0.0 - 1.0*\
  Definir dureza/contraste de alfa.
* **Desplazamiento de rotación de origen**: *0.0 - 1.0*\
  Rotación sólo para el origen del parche.
* **Coordenadas de posición**
  * **Posición de origen**:\
    Posición del origen. Tiene control en vista 2D.
  * **Posición del parche**:\
    Posición del objetivo. Tiene control en vista 2D.

## Imágenes de ejemplo

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
