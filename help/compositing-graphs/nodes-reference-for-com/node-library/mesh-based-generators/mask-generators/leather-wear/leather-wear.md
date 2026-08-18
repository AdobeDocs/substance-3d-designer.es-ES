---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Desgaste de cuero para generar máscaras de desgaste en superficies de cuero basadas en la curvatura de la malla y los puntos de contacto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de cuero
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Desgaste de cuero

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## Desgaste de cuero

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el desgaste con un patrón de cuero, con más desgaste en los bordes basados en la curvatura. Es similar a [Edge Wear de fibra de vidrio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) en cuanto a funcionalidad y tiene en su mayoría los mismos parámetros.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para la colocación de los bordes. ¡Obligatorio!
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para ocluir ciertas áreas. Recomendado, pero no obligatorio.
* **Entrada de Suciedad**: *Entrada en escala de grises*\
  Ranura de entrada de mapa de Suciedades opcional que se puede activar mediante el parámetro &quot;Usar Suciedad personalizada&quot;.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel de desgaste**: *0.0 - 1.0* Define el nivel de desgaste global, revelando gradualmente.
* **Contraste de desgaste**: *0.0 - 1.0* Establece el contraste del efecto.
* **Cantidad de Suciedades**: *0.0 - 1.0* Define la cantidad de suciedad (patrón de piel predeterminado) que se debe mezclar entre los bordes.
* **Enmascaramiento de Oclusión ambiental**: *0.0 - 1.0* Define hasta qué punto el AO oculta los efectos de desgaste.
* **Peso de curvatura**: *0.0 - 1.0* Establece hasta qué punto los bordes de la curvatura afectan el resultado final. Incluso si se establece en 0, todavía necesita un mapa de curvatura.
* **Usar Suciedad personalizada**: *Falso/Verdadero* Permite reemplazar el patrón de cuero predeterminado integrado. Utilice en su lugar una ranura de entrada personalizada.

## Imágenes de ejemplo

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
