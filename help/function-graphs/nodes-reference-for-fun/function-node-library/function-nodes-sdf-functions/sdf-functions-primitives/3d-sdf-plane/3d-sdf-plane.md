---
title: Plano
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Plano
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Plano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de plano](./3d-sdf-plane.png "Plano")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para un plano de orientación, posición y tamaño ajustables.

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
| <b>Normal</b> *Float3* | El espacio del mundo vector normal del plano, que controla su orientación.<br>El vector está normalizado.<br><br><i>Valor predeterminado: (0, 0, 1)</i> |
| <b>Tamaño</b> *Float2* | El tamaño del plano en X e Y.<br><br><i>Valor predeterminado: (1, 1)</i> |
| <b>Thickness</b> *Flotador* | El thickness del plano, aplicado en todas las direcciones.<br>El plano se redondea al aumentar el thickness.<br><br><i>Valor predeterminado: 0</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno del giro del plano.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
