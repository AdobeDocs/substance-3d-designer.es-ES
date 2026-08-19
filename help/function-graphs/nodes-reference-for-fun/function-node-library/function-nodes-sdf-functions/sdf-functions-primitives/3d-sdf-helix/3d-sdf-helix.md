---
title: Hélice (aprox.)
description: Designer > Gráficas de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Hélice (aprox.)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Hélice (aprox.)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Hélice ![aprox. icon](./3d-sdf-helix.png "Helix (aprox.)")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para una aproximación de una hélice, que es una forma formada por el barrido de un círculo a lo largo de una curva que serpentea a lo largo de una curva ascendente alrededor de un eje.<br><br><i>Nota:</i>Dado que esta Función SDF es una aproximación, pueden aparecer artefactos al procesarla.

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
| <b>Radio principal</b> *Flotador* | Distancia de la curva de bobinado desde el eje.<br><br><i>Valor predeterminado: 0,4</i> |
| <b>Radio menor</b> *Flotador* | Radio del círculo que se está barriendo a lo largo de la curva para formar la superficie de la hélice.<br><br><i>Valor predeterminado: 0,1</i> |
| <b>Height</b> *Flotador* | El height Z-up de la hélice.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Windings</b> *Flotador* | El número de veces que la curva gira completamente alrededor del eje en pasos de 0,5.<br>Es decir, cuántas veces la hélice girará dentro de un height de 0,5.<br><br><i>Valor predeterminado: 4</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno del pivote de la hélice.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
