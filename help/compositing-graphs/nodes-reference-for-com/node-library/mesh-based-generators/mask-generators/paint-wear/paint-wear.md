---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Desgaste de pintura para generar máscaras de desgaste de pintura basadas en la geometría de malla para crear efectos realistas de recorte de pintura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de pintura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# Desgaste de pintura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## Desgaste de pintura

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el desgaste de la pintura y el desgaste en los bordes.

## Parámetros

### Entradas

* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Máscara de variación**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la cantidad total de desgaste de la pintura, revelando gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Oclusión**: *0.0 - 1.0* Define la cantidad de efecto que tiene el AO horneado en la prevención del desgaste en áreas más oscuras.
* **Radio**: *0.0 - 2.0* Establece hasta dónde se extiende el efecto de recorte desde los bordes convexos.
* **Variación**: *0.0 - 1.0* Establezca la cantidad de variación (suciedad) que se mezclará en el efecto.
* **Omitir máscara de variación**: *Falso/Verdadero* Habilita la ranura de entrada de mapa de variación personalizada (suciedad).

## Imágenes de ejemplo

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
