---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Wear de fibra de vidrio para generar máscaras de desgaste en bordes de fibra de vidrio en función de la curvatura de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de fibra de vidrio
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Edge Wear de fibra de vidrio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## Edge Wear de fibra de vidrio

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Representa una máscara específicamente destinada a un tipo de fibra de vidrio de desgaste, tal vez podría ser utilizado para tela. Debido a la naturaleza muy enlosada y repetitiva de las fibras, la fusión triplanar puede habilitarse opcionalmente.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para el resaltado de bordes. ¡Obligatorio!
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para enmascarar áreas ocluidas. No es obligatorio, pero definitivamente recomendable.
* **Entrada de Suciedad**: *Entrada en escala de grises*\
  Ranura personalizada opcional para anular el patrón de fibra.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Normal del Espacio Mundial**: *Entrada de color*\
  Solo se usa para triplanar.
* **Posición**: *Entrada de color*\
  Solo se usa para triplanar.

### Parámetros

* **Nivel de desgaste**: *0.0 - 1.0* Como un [Histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), revela progresivamente el desgaste.
* **Contraste de desgaste**: *0.0 - 1.0* Establece el contraste total del efecto.
* **Smoothness de bordes**: *0.0 - 16.0* Define el sangrado/desenfoque de los bordes resaltados.
* **Cantidad de Suciedades**: *0.0 - 1.0* Establece la cantidad de efecto de fibra que se debe mezclar entre los bordes. Ajusta esto junto con el nivel de desgaste para obtener el máximo control.
* **Enmascaramiento de Oclusión ambiental**: *0.0 - 1.0* Define la influencia que tiene el AO sobre la ocultación del efecto.
* **Peso de curvatura**: *0.0 - 1.0* Establece la cantidad de influencia que tienen los bordes convexos de la Curvatura.
* **Usar Suciedad personalizada**: *Falso/Verdadero* Reemplaza las fibras integradas con mapa personalizado.
* **Usar triplanar**: *False/True* Permite que [Tri Planar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) oculte las costuras.
* **Contraste de fusión triplanar**: *0.0 - 1.0* Controla el contraste del efecto Triplanar.

## Imágenes de ejemplo

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
