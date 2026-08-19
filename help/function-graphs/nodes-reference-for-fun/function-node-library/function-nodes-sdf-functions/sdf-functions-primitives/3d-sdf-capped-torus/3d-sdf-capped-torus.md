---
title: Toro tapado
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Toro limitado
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Toro tapado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de torus con tope](./3d-sdf-capped-torus.png "Torus con tope")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Función SDF para un toro tapado, donde el barrido del círculo menor a lo largo de un círculo mayor puede ser tapado en un ángulo.<br>Ambos círculos tienen radios ajustables.

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
| <b>Radio principal</b> *Flotador* | Radio del círculo principal a lo largo del cual se arrastra el círculo secundario para formar la superficie del toro.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Radio menor</b> *Flotador* | Radio del círculo menor que se está barriendo a lo largo del círculo mayor para formar la superficie del toro.<br><br><i>Valor predeterminado: 0,2</i> |
| <b>Ángulo</b> *Flotador* | Ángulo central, por turnos, que define el arco de recorte del círculo principal a lo largo del cual no se barrerá el círculo secundario.<br><br><i>Valor predeterminado: 0,75</i> |
| <b>Desplazamiento de ángulo</b> *Flotador* | Desplazamiento, a lo largo del radio principal, del arco de recorte a lo largo del cual no se barrerá el círculo menor.<br><br><i>Valor predeterminado: 0</i> |
| <b>Simétrica</b> *Booleano* | Controla si el arco de recorte debe dibujarse en una o dos direcciones.<br><br><i>Valor predeterminado: True</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno del pivote del toro limitado.<br><br><i>Valor predeterminado: (0, 0, 0,5)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
