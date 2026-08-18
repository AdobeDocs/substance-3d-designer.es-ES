---
title: Pirámide
description: Designer > Gráficas de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Pirámide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# Pirámide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de pirámide](./3d-sdf-pyramid.png "Pirámide")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para una pirámide de height ajustable, tamaño base y posición base.

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
| <b>Height</b> *Flotador* | El height Z-up del ápice de la pirámide desde su base.<br><br><i>Valor predeterminado: 1</i> |
| <b>Tamaño base</b> *Float2* | Tamaño de la base de la pirámide en X e Y.<br><br><i>Valor predeterminado: (1, 1)</i> |
| <b>Posición base</b> *Float3* | Posición del espacio mundial de la base de la pirámide.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
