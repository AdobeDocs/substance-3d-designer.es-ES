---
title: Rotar
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Transformar > Rotar
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Rotar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de rotación](./3d-sdf-transform-rotate.png "Rotar")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Gire una forma SDF alrededor de uno o varios ejes desde un punto de giro ajustable, por turnos.<br>Usa el ayudante de <b>transformación dinámica</b> del <b>Visor 3D</b> para visualizar la rotación realizada.

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
| <b>Ángulo</b> *Flotador* | Ángulo, por turnos, en el que se gira la forma SDF.<br><br>El ángulo se visualiza mediante un círculo en el ayudante de <b>transformación de giro</b> del <b>visor 3D</b>. Alinee la cámara para ver la flecha del <b>eje</b> como el centro de este círculo para ver claramente el ángulo de rotación como una fracción de un giro.<br><br><i>Valor predeterminado: 0</i> |
| <b>Eje</b> *Float3* | El vector normalizado que define el eje alrededor del cual gira la forma SDF.<br>P.ej. (0, 1, 0) girará la forma SDF alrededor del eje Y de su punto de giro local.<br><br>El eje se visualiza mediante una flecha en el ayudante <b>Transformar pivote</b> del <b>Visor 3D</b>. El color de la flecha está asignado a los componentes XYZ de este vector.<br><br><i>Valor predeterminado: (0, 1, 0)</i> |
| <b>Posición de pivote</b> *Float3* | Posición del espacio mundial del pivote local de la forma SDF, donde (0, 0, 0) coloca el pivote en el centro de la forma SDF. Define el origen de la rotación.<br><br>El giro se visualiza al principio de la flecha en el ayudante <b>Transformar giro</b> del <b>Visor 3D</b>. |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
