---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Utilice el nodo Dust para generar máscaras de acumulación de dust basadas en la geometría de malla para crear efectos de dust y suciedad realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el dust acumulado en áreas ocluidas y bajas, así como solo en áreas que miran hacia arriba. Requiere que funcionen el AO y las Normas Espaciales Mundiales.

## Parámetros

### Entradas

* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para la colocación de dustes. ¡Obligatorio!
* **Normal del Espacio Mundial**: *Entrada de color*\
  Mapa con bake utilizado para la colocación de dustes. ¡Obligatorio!
* **Ruido**: *Entrada en escala de grises*\
  La asignación de dust personalizada (opcional) solo aparece cuando Ruido de reemplazo está establecido en True.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Establece la cantidad total de dustes.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el dust.
* **Importe de Oclusión**: *0.0 - 1.0* Establece la influencia de AO; aparecerá más dust en las áreas ocluidas.
* **Opacidad de ruido**: *0.0 - 1.0* Establece la cantidad de ruido visible en las áreas polvorientas.
* **Anular ruido**: *Falso/Verdadero* Establecido para utilizar la entrada de mapa de dust personalizado.

## Imágenes de ejemplo

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
