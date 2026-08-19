---
title: Rotar P
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Transformar > Rotar p
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Rotar P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Rotar P](./3d-sdf-transform-rotate-p.png "Rotar P")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Girar el espacio alrededor de un eje en un ángulo ajustable.<br>La posición transformada del mundo de salida se puede conectar a la entrada <b>P</b> de la mayoría de las Funciones SDF para definirlas en este espacio transformado del mundo.<br><br>Use el ayudante de <b>transformación de tabla dinámica</b> del <b>Visor 3D</b> para visualizar la rotación realizada.<br><br><i>Sugerencia:</i> Las transformaciones P se pueden encadenar, pero tenga en cuenta que los resultados dependen del orden de las operaciones.

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
| <b>Ángulo</b> *Flotador* | Ángulo, por turnos, en el que se gira el espacio mundial.<br><br>El ángulo se visualiza mediante un círculo en el ayudante de <b>transformación de giro</b> del <b>visor 3D</b>. Alinea la cámara para ver la flecha del <b>eje</b> como el centro de este círculo y ver claramente el ángulo de tu rotación como una fracción de un giro. |
| <b>Eje</b> *Float3* | El vector normalizado que define el eje alrededor del cual gira el espacio mundial.<br>P.ej. (0, 1, 0) girará el espacio de entorno alrededor del eje Y del punto de giro.<br><br>El eje se visualiza mediante una flecha en el ayudante <b>Transformar pivote</b> del <b>Visor 3D</b>. El color de la flecha está asignado a los componentes XYZ de este vector.<br><br><i>Valor predeterminado: (0, 1, 0)</i> |
| <b>Posición de pivote</b> *Float3* | Posición del espacio mundial del pivote que define el origen de la rotación.<br><br>El punto de giro se visualiza al principio de la flecha en el asistente de <b>transformación de giro</b> del <b>visor 3D</b>. |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
