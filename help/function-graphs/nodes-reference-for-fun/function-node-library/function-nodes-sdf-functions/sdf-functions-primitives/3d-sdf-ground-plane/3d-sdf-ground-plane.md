---
title: Plano de tierra infinito
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Plano de tierra infinito
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Plano de tierra infinito

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de plano de tierra infinito](./3d-sdf-ground-plane.png "Plano de tierra infinito")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para un plano de tierra infinito, con height ajustable.

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
| <b>Height</b> *Flotador* | El height Z-up del plano.<br><br><i>Valor predeterminado: 0</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
