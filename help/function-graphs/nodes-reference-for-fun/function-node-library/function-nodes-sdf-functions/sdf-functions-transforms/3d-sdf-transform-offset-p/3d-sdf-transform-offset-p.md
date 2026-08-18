---
title: Desplazamiento P
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Transformar > Desplazamiento P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# Desplazamiento P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de desplazamiento P](./3d-sdf-transform-offset-p.png "Desplazamiento P")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Desplaza el espacio del mundo a lo largo de un vector.<br>La posición de mundo transformada de salida se puede conectar a la entrada <b>P</b> de la mayoría de las Funciones SDF para definirlas en este espacio de mundo transformado.<br><br><i>Sugerencia:</i> Las transformaciones P se pueden encadenar, pero tenga en cuenta que los resultados dependen del orden de las operaciones.

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
| <b>Desplazamiento</b> *Float3* | La distancia del espacio del mundo se desplazará en las direcciones X, Y y Z. |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
