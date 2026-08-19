---
title: Voltear
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Transformar > Voltear
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# Voltear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Voltear icono](./3d-sdf-transform-flip.png "Voltear")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplica una transformación espejo a la forma SDF de entrada.<br>Básicamente realiza una escala negativa en los ejes seleccionados.

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
| <b>SDF</b> *Flotador* | Forma SDF de entrada. |
| <b>Eje de simetría</b> *Entero3* | Use un entero3 para establecer el eje de simetría deseado.<br>P.ej. (1, 0, 0) reflejará el eje X.<br><br><i>Valor predeterminado: (1, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
