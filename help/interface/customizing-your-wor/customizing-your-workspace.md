---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/customizing-your-workspace.html"
breadcrumb-title: ''
description: Aprenda a personalizar su espacio de trabajo en Substance 3D Designer para optimizar sus preferencias de flujo de trabajo y diseño.
helpx_creative_field: ""
helpx_description: Designer > Interface > Customizing your workspace
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Personalización del espacio de trabajo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# Personalización del espacio de trabajo

Esta página presenta las formas de organizar los paneles en la interfaz de usuario de [Adobe Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) y aprovechar sus funciones para mejorar tus flujos de trabajo.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## Menú de Windows

Este menú le permite administrar los principales elementos de la interfaz de usuario de Designer. Cada opción se describe en la sección <b>Windows</b> de [esta página](../the-main-toolbar/the-main-toolbar.md) sobre la barra de herramientas principal. Aquí, proporcionaremos conceptos adicionales relacionados con este menú.

### Mostrar u ocultar una vista

Para mostrar u ocultar un elemento de interfaz específico, haga clic en su nombre en el menú *Windows*. Los elementos mostrados tienen una marca de verificación ![](../../assets/image2015-12-17-10-43-24.png).

### Rellenar un muelle con una vista

En Designer, un conjunto acoplado es un *contenedor independiente de su contenido*. Esto significa que puede existir un conjunto de elementos acoplados <b>Library</b> y estar vacío, ya que no contiene ninguna vista de biblioteca *view*.

Las opciones <b>New Explorer</b>, <b>New 3D view</b> y <b>New Library view</b> crean vistas, que se colocarán de acuerdo con el estado actual de la interfaz de usuario:

* Si hay un conjunto acoplado vacío disponible, la nueva vista se crea *dentro de él*
* Si los muelles vacíos *no* están disponibles, se crea un *nuevo muelle* para albergar la nueva vista

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menú Windows](../../assets/windows-menu-1.png "Menú Windows")

</td>
</tr>
</table>

## Cambio de tamaño de muelles

Se puede cambiar el tamaño de los muelles moviendo cualquiera de sus bordes. Los demás muelles cambiarán de tamaño dinámicamente para ajustarse.

![Redimensionando muelles](../../assets/interface-customisation-resize.gif "Redimensionando muelles")

## Mudanza de muelles

Se puede mover cualquier conjunto acoplado alrededor de la ventana principal mediante su *barra de título*. En función de la ubicación a la que se mueva el conjunto, se cambiará el tamaño de los muelles para ajustarlos.

![Muelles móviles](../../assets/interface-customisation-move.gif "Muelles móviles")

## Estaciones de tabulación

Los Docks pueden estar apilados en pestañas. Esto resulta útil para guardar el espacio de la pantalla o agregar vistas que se relacionan entre sí de alguna manera.

Puede separar los muelles moviendo un muelle con su barra de título *sobre un muelle existente*, por ejemplo, los muelles no cambian de tamaño ni se mueven, pero aparece un *marco* alrededor del muelle de destino.

![Muelles de tabulación](../../assets/interface-customisation-tab.gif "Muelles de tabulación")

## Desacoplamiento

Un conjunto acoplado se puede desacoplar en una *ventana flotante* que se puede cambiar de tamaño y mover fuera de la ventana principal, incluso fuera de otra pantalla.

Esto se puede hacer de dos maneras:

* Mueve el dock usando su *barra de título* y colócalo *fuera de la ventana principal* o en un área de la ventana principal que *no es un dock*. Puede volver a acoplar este conjunto acoplado moviéndolo en otro conjunto acoplado *en la ventana principal* o haciendo clic en el botón <b>![](../../assets/dock-icons-redock.png) Volver a acoplar </b>;
* Haciendo clic en el botón <b>![](../../assets/dock-icons-undock.png) Desacoplar</b>. Un dock desacoplado con este método puede *solo* reacoplarse haciendo clic en el botón <b>![](../../assets/dock-icons-redock.png) Reacoplar</b>.

![Desacoplando](../../assets/interface-customisation-undock.gif "Desacoplando")

## Maximización de los muelles

Se puede maximizar cualquier conjunto acoplado para que se ajuste al área o a su *ventana principal*:

* Los muelles acoplados se extenderán por todo el área de la *ventana principal*, excluyendo la barra de título, la barra de herramientas principal y la barra de estado
* Los muelles no acoplados se extenderán por *toda la pantalla*

Los muelles se pueden maximizar de dos maneras:

* Colocando el *cursor sobre el muelle* y presionando la tecla <b>Mayús+Espacio</b>
* Haciendo clic en el botón <b>![](../../assets/dock-icons-maximise.png) Maximizar</b>

Los muelles maximizados se pueden minimizar en el tamaño y la ubicación que tenían *antes de maximizarlos*. Esto se puede hacer de tres maneras:

* Colocando el *cursor sobre el muelle* y presionando la tecla <b>Mayús+Espacio</b>
* Haciendo clic en el botón <b>![](../../assets/dock-icons-minimise.png) Minimizar</b>
* Abriendo el menú <b>Windows</b> y seleccionando la opción <b>Desmaximizar ventana</b>

>[!NOTE]
>
> Solo se puede maximizar *un conjunto acoplado* a la vez.

>[!IMPORTANT]
>
> Cuando se maximiza un conjunto acoplado, algunos comportamientos de la interfaz pueden diferir:
> 
> * Los acoplamientos que aparecen o se actualizan automáticamente lo hacen en segundo plano (por ejemplo, Propiedades, vista 2D)
> * Los elementos de menú están *deshabilitados* en el menú **Windows**
> * Los botones están *deshabilitados* en la barra de título del dock
> * Un conjunto acoplado maximizado en la ventana principal *no se puede mover* con su barra de título

![Maximización de muelles](../../assets/interface-customisation-maximise.gif "Maximización de muelles")

## Fijar muelles

Al fijar un conjunto acoplado *, se impide que se rellene* con otro contenido o una vista diferente.

Cuando se ancla un dock, cualquier contenido futuro que deba mostrarse en su lugar *creará un nuevo dock* para hospedarlo. Este nuevo dock no se fijará y, por lo tanto, puede actualizar y alojar contenido nuevo.

Para fijar un conjunto acoplado, haga clic en su botón ![](../../assets/dock-icons-pin.png) <b>Fijar</b>. A continuación, puedes *desanclarlo* con el botón ![](../../assets/dock-icons-pinned.png) <b>Desanclar</b> para que *esté disponible* de nuevo para alojar cualquier contenido nuevo.

*Se puede anclar más de un dock de* a la vez, incluidos varios de *mismo tipo*.

Los muelles de fijación le proporcionan las siguientes capacidades:

* Visualización y ajuste de propiedades de varios nodos al mismo tiempo
* Visualización simultánea de dos o más mapas de bits
* Trabajo simultáneo en varios gráficos

![Muelles de fijación](../../assets/interface-customisation-pin.gif "Muelles de fijación")

## Cerrando muelles

Se puede cerrar cualquier estación de acoplamiento haciendo clic en su botón ![](../../assets/dock-icons-close.png) <b>Cerrar</b>.

## Restablecer el diseño de la interfaz

Para restablecer toda la interfaz de usuario en su diseño predeterminado, abre el menú <b>Windows</b> y selecciona la opción <b>Restablecer diseño</b>.

Su estado de visualización también se restablecerá, lo que significa que los muelles cerrados se pueden *reabrir* (por ejemplo, la vista 3D) y los muelles mostrados se pueden *cerrar* (por ejemplo, la consola, el administrador de dependencias, los muelles creados por los complementos).

![Restablecer diseño](../../assets/interface-customisation-reset.gif "Restablecer diseño")
