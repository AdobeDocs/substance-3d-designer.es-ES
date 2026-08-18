---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Utilice el nodo Pavimento de arco para generar patrones de pavimento en forma de arco para crear texturas curvas de carretera y trazado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pavimento de arco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Pavimento de arco

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## Pavimento de arco

**En:** *Generadores De Texturas**/Patrones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera un patrón de pavimento de arco parisino. Este efecto no se puede lograr con [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) estándar o [Sampler en mosaico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md), de ahí este nodo dedicado.

## Parámetros

* **Escala**: *1 - 8* Establece la escala o el mosaico global.
* **Cantidad de patrón**: *1 -* 32\
  Define la cantidad de ladrillos utilizados en cada arco.
* **Aleatorio de cantidad de patrón**: *0.0 - 1.0*\
  Aleatoriza la cantidad de ladrillos en cada arco. Tiene el efecto añadido de dar a los ladrillos diferentes escalas.
* **Cantidad mínima del patrón**: *1 - 10*\
  Controla la cantidad mínima de ladrillos al aleatorizar arcos.
* **Cantidad De Arcos**: *0 - 20*\
  Define la cantidad de arcos apilados verticalmente. Cambia el height del ladrillo.
* **Patrón**: *Imagen De Entrada, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradaciones, Ondas, Media Campana, Campana Cortada, Media Luna, Cápsula, Cono*\
  Selecciona la forma de motivo que se va a utilizar.
* **Filtrado de imágenes de entrada**: *Bilineal + Mipmaps, Bilineal, Más Cercano*
* **Escala de patrón**: *0.0 - 1.0* Establece la escala de cada mosaico.
* **Ancho del patrón**: *0.0 - 1.0*\
  Define la anchura de cada azulejo.
* **Height de motivo**: *0.0 - 1.0*\
  Define el height de cada mosaico.
* **Anchura aleatoria del patrón**: *0.0 - 1.0*\
  Aleatoriza la anchura del azulejo.
* **Aleatorio de Height de motivo**: *0.0 - 1.0*\
  Aleatoriza el height del azulejo.
* **Anchura de patrón global aleatoria**: *0.0 - 1.0* Aleatoriza el ancho del azulejo, sin crear espacios más grandes entre ellos.
* **Disminución de Height de motivo**: *0.0 - 1.0* Controla el aplastamiento del height del azulejo en los extremos de cada arco.
* **Aleatorio de color**: *0.0 - 1.0*\
  Aleatoriza los colores del azulejo.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.

## Imágenes de ejemplo

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
