---
title: Prisma hexagonal
description: Designer > Gráficas de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Primitiva > Prisma hexagonal
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Prisma hexagonal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de prisma hexagonal](./3d-sdf-hexagonal-prism.png "Prisma hexagonal")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para un prisma de 6 lados de height ajustable, radio y redondeo de bordes.

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
| <b>Height</b> *Flotador* | El height Z-up del prisma hexagonal desde su base.<br><br><i>Valor predeterminado: 1</i> |
| <b>Radio</b> *Flotador* | Radio del prisma hexagonal.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Redondeo</b> *Flotador* | El radio de los arcos redondeados aplicados a los bordes del prisma hexagonal.<br><br><i>Nota:</i> los bordes duros pueden aparecer donde se cruzan los radios de redondeo.<br><br><i>Valor predeterminado: 0</i> |
| <b>Posición central</b> *Float3* | Posición del espacio mundial del pivote del prisma hexagonal.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
