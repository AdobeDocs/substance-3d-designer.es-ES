---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Utilice el nodo Fugas para generar patrones de fugas basados en la geometría de malla para crear manchas de agua y efectos de fluidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pérdidas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# Pérdidas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## Pérdidas

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Este nodo representa las fugas de dirt y suciedad procedentes de bordes afilados. A medida que se generan rayas con Posición horneada, siempre se ejecutan hacia abajo.

Asegúrese de intentar cambiar la máscara de variación: dado que controla la colocación de las rayas, puede tener una influencia mucho mayor que con otros generadores de máscaras.

## Parámetros

### Entradas

* **Posición**: *Entrada en escala de grises*\
  Mapa de posición al horno, utilizado para direcciones de rayas. ¡Obligatorio!
* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para la colocación de rayas. ¡Obligatorio!
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras. Se recomienda, pero se puede utilizar blanco plano en su lugar.
* **Espacio normal**: *Entrada de color*\
  Baked World Space Normalmap, utilizado para la dirección de rayas. ¡Obligatorio!
* **Máscara de variación**: *Entrada en escala de grises*\
  Máscara de variación opcional, que se activa estableciendo el valor de override en True.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Nivel total del resultado. Revela el efecto progresivamente y afecta también a la longitud. Se debe establecer bastante alto para obtener goteos largos.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Variación**: *0.0 - 1.0* Establece la cantidad de variación a gran escala usada para enmascarar las rayas. Si establece este valor en 0, se generarán rayas uniformes, así que evite esto.
* **Longitud**: *0.0 - 8.0* Longitud de los goteos de rayas. Si se establece este valor demasiado alto a pequeña escala, se producirá un paso visible. Juega con el nivel también.
* **Ocluir**: *X, Y, Z, Ninguno* Establece la dirección en la que debe afectar el AO.
* **Omitir máscara de variación**: *Falso/Verdadero* Permite reemplazar la máscara de variación con una ranura de entrada personalizada. El uso de máscaras más dispersas o más densas puede ser interesante y es una buena manera de controlar los goteos.

## Imágenes de ejemplo

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
