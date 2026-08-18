---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: Utilice el nodo Trazados a spline para convertir los datos de trazado en splines y utilizarlos con nodos basados en spline.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trazados a spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# Trazados a spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/paths-to-splines-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Convierte rutas de acceso en splines que se pueden visualizar mediante un nodo [Spline Render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) y procesar mediante [nodos Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md).

</td>
</tr>
</table>

>[!NOTE]
>
> Las splines son curvas, por lo que no pueden conservar el enfoque de los trazados. Se espera un cierto suavizado de las formas al convertir trazados en splines.

>[!TIP]
>
> Este nodo se puede usar después del nodo [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) para formar una cadena que convierta una máscara en splines.

## Conectores de entrada

<b>Rutas</b> *Color*\
Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de rutas.

## Conectores de salida

<b>Códigos polinómicos </b>*Color* Coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen en color:\
    Posición <b>R</b> - X\
    <b>G</b> - Posición Y\
    <b>B</b> - Height\
    <b>A</b> - Datos empaquetados:\
        * Firmar: La spline está cerrada (negativa) o abierta (positiva);\
        * Valor absoluto: Thickness + 1.

<b>Datos de spline</b> *Color*\
Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen <b>color</b>:\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Sin usar\
<b>A</b> - Sin usar

<b>Cantidad de spline</b> *Entero*\
Número de splines de entrada.

## Parámetros

<b>Precisión de splines</b> *Entero*\
El logaritmo en base 2 (log2) del número de vértices muestreados en cada trazado de la entrada Paths para crear la spline correspondiente.

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-Before.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-After.jpg" alt="PathsToSpline-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-After.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
