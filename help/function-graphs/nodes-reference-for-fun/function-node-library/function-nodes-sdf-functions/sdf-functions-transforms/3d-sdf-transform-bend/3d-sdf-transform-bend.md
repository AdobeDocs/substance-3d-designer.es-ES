---
title: Curvar (inexacto)
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Transformar > Curvar (inexacto)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# Curvar (inexacto)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de curva (inexacta)](./3d-sdf-transform-bend.png "Curvar (inexacta)")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dobla una forma SDF alrededor de su eje Y local entre un punto inicial y final en ángulo.<br><br><i>Nota:</i>Como esta función de transformación no es exacta, pueden aparecer artefactos al procesarla.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](../../working-with-sdf-functions.md)

## Entradas

|  |  |
| :--- | :--- |
| <b>SDF</b> *Flotador* | Forma SDF de entrada. |
| <b>Ángulo</b> *Flotador* | Ángulo, por turnos, de la rotación aplicada al final del plegado. |
| <b>Inicio</b> *Flotador* | Posición del mundo en el eje Z donde comienza el plegado. No se dobla todo el volumen inferior. |
| <b>Fin</b> *Flotador* | Posición del mundo en el eje Z donde termina el plegado. Todo el volumen anterior se gira uniformemente en el ángulo especificado. |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
