---
title: Cono tapado 2 puntos
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Cono cerrado de 2 puntos
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Cono tapado 2 puntos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de cono cerrado de 2 puntos](./3d-sdf-capped-cone-2-points.png "Cono cerrado de 2 puntos")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Función SDF de un cono cerrado definido por las posiciones de su base y superior.<br>La base y la parte superior tienen radios ajustables.

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
| <b>Base de posición</b> *Flotante3* | Posición de la base del cono cerrado.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>Posición superior</b> *Flotante3* | Posición de la parte superior del cono cerrado.<br><br><i>Valor predeterminado: (0, 0, 1)</i> |
| <b>Base de radio</b> *Flotante* | Radio de la base del cono cerrado.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Radio superior</b> *Flotante* | Radio de la parte superior del cono cerrado.<br><br><i>Valor predeterminado: 0,2</i> |
| <b>P</b> *Flotante3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
