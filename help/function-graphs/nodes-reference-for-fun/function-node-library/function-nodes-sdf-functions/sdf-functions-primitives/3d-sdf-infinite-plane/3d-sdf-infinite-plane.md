---
title: Plano infinito
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Plano infinito
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# Plano infinito

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de plano infinito](./3d-sdf-infinite-plane.png "Plano infinito")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para un plano infinito de orientación y posición ajustables.

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
| <b>Normal</b> *Float3* | El vector normal del espacio del mundo del plano infinito, que controla su orientación.<br>El vector está normalizado.<br><br><i>Valor predeterminado: (0, 0, 1)</i> |
| <b>Posición central</b> *Flotador* | Posición espacial mundial del pivote del plano, como distancia del origen mundial a lo largo de la normal del plano.<br><br><i>Predeterminado: 0</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
