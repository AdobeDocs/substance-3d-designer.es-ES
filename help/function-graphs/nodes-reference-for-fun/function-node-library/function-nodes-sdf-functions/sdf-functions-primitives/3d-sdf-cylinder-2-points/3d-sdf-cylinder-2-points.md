---
title: Cilindro 2 puntos
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Cilindro 2 puntos
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Cilindro 2 puntos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de cilindro de 2 puntos](./3d-sdf-cylinder-2-points.png "Cilindro de 2 puntos")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Función SDF de un cilindro de radio ajustable definido por las posiciones de sus discos de inicio y fin.

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
| <b>Inicio</b> *Flotante3* | Posición del disco de inicio del cilindro.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>Fin</b> *Flotante3* | Posición del disco final del cilindro.<br><br><i>Valor predeterminado: (0, 0, 1)</i> |
| <b>Radio</b> *Flotante* | El radio del cilindro.<br><br><i>Valor predeterminado: 0,25</i> |
| <b>P</b> *Flotante3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
