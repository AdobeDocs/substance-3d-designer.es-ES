---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: Obtenga más información sobre la barra de herramientas principal de Substance 3D Designer para acceder a herramientas y comandos comunes para el flujo de trabajo.
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Barra de herramientas principal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# La barra de herramientas principal

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Esta página describe la barra de herramientas principal y el menú de [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html), que aparecen en la parte superior izquierda de la ventana principal.Consta de dos partes: los menús principales desplegables y los botones de acceso rápido. También se puede acceder a todas las funciones del botón de acceso rápido a través de los menús <b>Archivo</b> y <b>Editar</b>.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Barra de herramientas principal](the-main-toolbar.resources/mainmenu.png "Barra de herramientas principal")

</td>
</tr>
</table>

## Botones de acceso rápido

![](the-main-toolbar.resources/newsubstance.png) <b>Nuevo gráfico de Substance...:</b> (Ctrl+N)Presenta la ventana [Nuevo gráfico](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) y, a continuación, crea un nuevo paquete con un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md).

![](the-main-toolbar.resources/open.png) <b>Abrir...:</b> (Ctrl+O) Abra un [paquete de Substance existente (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

![](the-main-toolbar.resources/saveall.png) <b>Guardar todo:</b> (Ctrl+⇧+S) Guarda todos los paquetes enumerados en el [Explorador](../../interface/the-explorer-window/the-explorer-window.md).

![](the-main-toolbar.resources/undo.png) <b>Deshacer:</b> (Ctrl+Z) Deshacer la última operación.

![](the-main-toolbar.resources/redo.png) <b>Rehacer:</b> (Ctrl+Y) Rehacer la última operación deshecha.

## Archivo

<b>Nuevo:</b> abre un submenú para crear un gráfico o paquete:

* <b>Nuevo gráfico de Substance...:</b>(Ctrl+N) Le presenta la ventana [Nuevo gráfico](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) que le permite configurar un nuevo gráfico de [Substance](../../compositing-graphs/substance-compositing-graphs.md);
* <b>Nuevo gráfico de funciones de Substance:</b> Crea un nuevo paquete con un [gráfico de funciones de Substance](../../function-graphs/function-graphs.md);
* <b>Vacío:</b> Crea un paquete vacío.

<b>Abrir...:</b> (Ctrl+O) Abra un [paquete de Substance existente (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

<b>Paquetes recientes:</b> Muestra una lista de los paquetes abiertos recientemente. Haga clic en una entrada para abrirla.

<b>Abrir los paquetes de la última sesión (#)</b>: Abre todos los paquetes que estaban abiertos cuando se cerró o finalizó la última sesión.

<b>Guardar todo:</b> (Ctrl+⇧+S) Guarda todos los paquetes abiertos, incluidos los paquetes cargados en segundo plano.

<b>Cerrar todo:</b> Cierra todos los paquetes abiertos.

<b>Recargar recursos:</b> Obliga a Designer a volver a cargar [todos los recursos, incluidos los mapas de bits y los datos del SVG](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

<b>Salir:</b> (Ctrl+Q): cierre Substance 3D Designer.

## Editar

<b>Deshacer:</b> (Ctrl+Z) Deshacer última operación.

<b>Rehacer:</b> (Ctrl+Y) Rehacer última operación deshecha.

<b>Preferencias...:</b> Abre la ventana Preferencias.

>[!NOTE]
>
> Se accede a este cuadro de diálogo desde el menú Substance 3D Designer de la barra de tareas de macOS.

## Herramientas

<b>Cancelar la representación:</b> (Esc) Detiene la operación actual del Substance Engine. Se puede utilizar para anular una operación pesada no deseada.

<b>Motor de suspensión:</b> ( ⇧+Esc) Suspende el motor de procesamiento. Esto puede acelerar la edición de complejos [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md).

<b>Cambiar motor...: </b>(F9) Ofrece una selección de motores de procesamiento, incluidos los motores de GPU (&quot;DirectX&quot; en Windows, &quot;OpenGL&quot; en macOS) y el motor de CPU (&quot;NEON&quot; en Apple Silicon, &quot;SSE&quot; en todos los demás).

<b>Substance Player:</b> Administrar la integración de Designer con Substance Player:

* <b>Localizar Reproductor...:</b> Informe a Designer de dónde está instalado el Reproductor;
* <b>Descargar el reproductor...:</b> Abre la [página de aterrizaje](https://helpx.adobe.com/substance-3d-player/home.html) de la documentación del Substance Player, donde se puede descargar el reproductor.

<b>Administrador de complementos...</b>: Abre la ventana Administrador de complementos, donde puede instalar, cargar y descargar [Complementos de Python para Substance 3D Designer.](../../scripting/scripting.md)

## Windows

<b>Nuevo Explorador:</b> Abre un nuevo conjunto acoplado del Explorador. Puede tener abiertos varios muelles del Explorador.

<b>Nueva vista 3D:</b> Abre un nuevo conjunto acoplado de vista 3D. Puede tener abiertos varios acoplamientos de vista 3D.

<b>Nueva vista de biblioteca:</b> Abre un nuevo conjunto acoplado de biblioteca. Puede tener abiertos varios muelles de biblioteca.

<b>Editor de Python:</b> Abre el Editor de Python usado para[evaluar y crear scripts](../../scripting/scripting.md).

<b>Restablecer diseño:</b> Restablece el área de trabajo al diseño predeterminado. Todas las ventanas se reorganizarán y es posible que algunas ventanas se vuelvan a ocultar. Utilícelo en caso de problemas con el diseño del programa.

<b>Desmaximizar ventana:</b> Cuando cualquier panel está *maximizado*, esta opción lo desmaximiza y restaura el diseño tal y como estaba *antes* de que se maximizara la ventana

<b>Explorador:</b> Muestra u oculta el [Explorador](../the-explorer-window/the-explorer-window.md).

<b>Gráfico:</b> Muestra u oculta la [ventana gráfica](../../interface/the-graph-view/the-graph-view.md).

<b>Parámetros:</b> Muestra u oculta las [propiedades](../properties/properties.md).

<b>Consola:</b> Mostrar u ocultar la ventana de consola.

<b>Vista 3D:</b> Muestra u oculta las [vistas 3D](../../interface/3d-view/3d-view.md).

<b>Administrador de dependencias:</b> Muestra u oculta el [Administrador de dependencias](../../interface/dependency-manager/dependency-manager.md).

<b>Vistas 2D:</b> Muestra u oculta el [vista 2D](../2d-view/2d-view.md).

<b>Biblioteca:</b> Muestra u oculta la [ventana de biblioteca.](../../interface/the-library/the-library.md)

<b>Barra de herramientas principal:</b> Mostrar u ocultar la barra de herramientas principal (solo botones de acceso rápido).

>[!NOTE]
>
> Para obtener más información sobre la administración de paneles de Designer, su personalización y las funciones que mejoran el flujo de trabajo, visita la página [Personalización del espacio de trabajo](../../interface/customizing-your-wor/customizing-your-workspace.md)de esta documentación.

## Ayuda

<b>Tutorials:</b> Abre el sitio web [Substance 3D tutorials](https://substance3d.adobe.com/tutorials/) (anteriormente Substance Academy).<b>\
</b>

<b>Notas de la versión:</b> Abre una ventana con el registro de cambios de la última versión.

<b>Requisitos técnicos:</b> Muestra los requisitos técnicos para ejecutar la aplicación.

<b>Documentación:</b> Abre el explorador web predeterminado en [esta documentación](https://www.adobe.com/go/Substance-3D-doc-Designer_es).

<b>Documentación de scripts:</b> Abre el explorador web en los documentos locales de la API de Python.

<b>Foros...:</b> Abre el explorador web en nuestro foro de la [Comunidad de asistencia técnica](https://forum.substance3d.com/) para ponerse en contacto con la comunidad y hacer preguntas.

<b>Informar de un error...:</b> Abrir ventana de informes de errores.

<b>Exportar registro...:</b> Exporta los archivos de registro actuales a un archivo comprimido (.zip) para proporcionar asistencia técnica.

<b>Proporcionar comentarios...:</b> Abre el explorador web en la página principal de la [Comunidad de asistencia técnica](https://www.adobe.com/go/Substance-3D-feedback-Designer_es) de Adobe.

<b>Recursos de Substance 3D:</b> Busque [contenido 3D premium](https://substance3d.adobe.com/assets) para suscriptores (anteriormente Substance Source).

<b>Recursos de la comunidad de Substance 3D:</b> Le permite examinar [recursos de la comunidad gratuitos](https://substance3d.adobe.com/community-assets/) (anteriormente, Substance share).

<b>Administrar mi cuenta\*:</b> Abre la página web de la cuenta de Adobe.

<b>Iniciar o cerrar sesión...\*:</b> Permite iniciar o cerrar sesión en la cuenta de Adobe.

<b>Pantalla Inicio...:</b> Muestra el cuadro de diálogo [Pantalla Inicio](../../interface/home-screen/home-screen.md).

<b>Novedades...:</b> Muestra una pantalla que resalta las características agregadas a la última versión de Designer

<b>Pantalla de bienvenida...\*:</b> Muestra una pantalla que guía a los nuevos usuarios por el propósito de Designer y su lugar en el [ecosistema de Substance 3D](https://helpx.adobe.com/es/substance-3d.html)

<b>Partners:</b> Te permite acceder a las renuncias de responsabilidad y los avisos de integraciones de terceros de nuestros socios de Designer.

<b>Acerca de Substance 3D Designer...:</b> Muestra información sobre la aplicación y sus componentes, como el número de versión.

\*: Estas opciones solo están disponibles en la versión de Designer instalada mediante [Adobe Creative Cloud Desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud), que requiere una [suscripción a Substance 3D](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar).
