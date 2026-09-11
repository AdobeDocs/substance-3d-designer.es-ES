---
title: Toro
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Toro
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# Toro

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de Torus](./3d-sdf-torus.png "Torus")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Función SDF de un toro, que es una forma formada por un círculo menor a lo largo de un círculo mayor.<i>Ambos círculos tienen radios ajustables.

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
| <b>Radio principal</b> *Flotante* | Radio del círculo a lo largo del cual se arrastra el disco secundario para formar la superficie del toro.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Radio menor</b> *Flotante* | Radio del círculo que se está barriendo a lo largo del círculo principal para formar la superficie del toro.<br><br><i>Valor predeterminado: 0,2</i> |
| <b>Posición central</b> *Flotante3* | Posición del espacio mundial del pivote del toro.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Flotante3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
