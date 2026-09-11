---
title: Escala
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Transformar > Escala
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# Escala

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de escala](./3d-sdf-transform-scale.png "Escala")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Escalar de manera uniforme una forma SDF.

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
| <b>SDF</b> *Flotante* | Forma SDF de entrada. |
| <b>Escala</b> *Flotante* | Factor de escala uniforme.<br><br><i>Valor predeterminado: 1</i> |
| <b>Posición de pivote</b> *Flotante3* | Posición del espacio mundial del pivote local de la forma SDF, donde (0, 0, 0) coloca el pivote en el centro de la forma SDF. <br>Define el origen de la escala.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Flotante3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
