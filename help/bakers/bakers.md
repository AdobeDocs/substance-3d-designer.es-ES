---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: Aprenda a utilizar Substance 3D Designer baker para calcular información basada en malla en archivos de textura.
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bakers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# Bakers

Hacer un bake se refiere a la acción de **transferir información basada en malla a texturas**. Los sombreadores o los filtros de Substance leen esta información para generar efectos o texturas más avanzados.

>[!NOTE]
>
> Para obtener más información sobre cómo hacer un bake, consulta la [Documentación de Haga un bake](https://experienceleague.adobe.com/es/docs/substance-3d/bakers/home).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Se puede tener acceso a la ventana haciendo un bake a través del archivo de malla en la ventana [Explorer](../interface/the-explorer-window/the-explorer-window.md). Haga clic con el botón derecho en el nombre de la malla y elija &quot;**Hacer un bake información del modelo**&quot; para abrir la ventana de hacer un bake.

</td>
<td width="33.33%" style="border: 0;" valign="top">

Opción ![&#39;Hacer un bake información de modo&#39; en el menú contextual del recurso de escena 3D](bakers.resources/sd-mesh-right-click.png "&#39;Hacer un bake información de modo&#39; en el menú contextual del recurso de escena 3D")

</td>
</tr>
</table>

![Haciendo un bake ventana](bakers.resources/sd-window-overview.png "Haciendo un bake ventana")

## Información general

La ventana de hacer un bake de se divide en varios paneles que se describen a continuación.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Elementos para hacer un bake

Este panel controla qué parte de la malla de baja densidad se utilizará para realizar el haga un bake.

Enumera la geometría que se encuentra dentro del fichero de malla de baja polimerización. De forma predeterminada, la lista se basa en los materiales individuales que se encuentran en el archivo, pero se puede cambiar a submallas en su lugar cuando sea pertinente. Puede desmarcar la casilla de verificación de los elementos que se deben omitir durante el proceso de hacer un bake.

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/sd-mesh-selection.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Salida

Este panel controla dónde se ubicará la textura hecha un bake.

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/sd-output.png)

</td>
</tr>
</table>

| *Parámetro* | *Descripción* |
| --- | --- |
| **Método** | Controla cómo se almacenarán las texturas hechas un bake con el paquete de Substance.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Incrustado</strong> : las texturas hechas un bake se almacenan en una subcarpeta junto al paquete de Substance con un nombre específico.</li><li data-preserve-html="true"><strong>Vinculado</strong> (predeterminado) : la textura horneada se almacena en la carpeta definida y, a continuación, se hace referencia a ella en el Substance empaquetado.</li></ul> |
| **Carpeta** | Ubicación de las texturas horneadas al guardarlas. Haga clic en el botón de tres puntos para abrir un cuadro de diálogo de archivo y elija la carpeta de exportación. Aparecerá una marca de verificación a la derecha para indicar si la carpeta realmente existe o no. |
| **Nombre** | Convención de nomenclatura de las texturas horneadas. Haga clic en el botón de tres puntos para abrir un menú desplegable e insertar otros marcadores de posición (nombre de fondo, personalizado, material, malla). |
| **Ejemplo** | Simule un nombre de archivo para probar la convención de nomenclatura. |
| **Colocar recurso en una carpeta específica de malla** | Si se activa, las texturas horneadas se guardarán dentro de una carpeta denominada archivo de malla. |

### Mallas de alta definición

Este panel controla la lista de mallas de alta densidad y los ajustes relacionados. Consulte los [parámetros comunes](https://experienceleague.adobe.com/es/docs/substance-3d/bakers/bakers-settings/common-parameters) para obtener más información.

![Mallas de alta definición](bakers.resources/sd-high.png "Mallas de alta definición")

### Valores predeterminados

Consulte los [parámetros comunes](https://experienceleague.adobe.com/es/docs/substance-3d/bakers/bakers-settings/common-parameters) para obtener más información.

![Valores predeterminados](bakers.resources/sd-default-values.png "Valores predeterminados")

### Lista de procesamiento y ajustes de Bakers

La **lista de procesamiento de Bakers** es donde puedes elegir qué textura horneada quieres generar. De forma predeterminada, la lista está vacía.

* **Agregando un nuevo panadero:** Haga clic en el botón &quot;Agregar panadero&quot;.
* **Quitando un panadero:** Selecciona el panadero en la lista, luego haz clic en el botón &quot;Eliminar panadero&quot;.
* **Mover un panadero a la parte superior:** Seleccione el panadero en la lista y, a continuación, haga clic en el botón &quot;Tire hacia arriba&quot;.
* **Bajando por un panadero:** Selecciona el panadero en la lista, luego haz clic en el botón &quot;Empujar hacia abajo&quot;.

Cada panadero en el hereda de forma predeterminada los valores predeterminados (véase más arriba). El tamaño (resolución), por ejemplo, se puede anular haciendo clic en la celda de la línea del baker. Esto es cierto para los demás ajustes de la línea.

Al hacer clic en un baker de la lista, la vista Parámetros de Baker se actualizará con sus parámetros específicos.

Para obtener más información sobre los parámetros específicos, consulte: [Configuración de Bakeres](https://experienceleague.adobe.com/es/docs/substance-3d/bakers/bakers-settings/bakers-settings).

![lista de procesamiento de Bakeres](bakers.resources/sd-baker-list.png "lista de procesamiento de Bakeres")
