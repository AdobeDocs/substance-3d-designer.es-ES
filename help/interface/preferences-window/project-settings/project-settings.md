---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window/project-settings.html"
breadcrumb-title: ''
description: Configure los ajustes del proyecto en las preferencias de Substance 3D Designer para personalizar el comportamiento predeterminado del proyecto.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Project settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuración del proyecto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '2687'
ht-degree: 1%

---


# Configuración del proyecto

Esta página presenta la <b>configuración de proyectos</b> en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) y la configuración que contiene.

Substance 3D Designer le permite crear preferencias *por proyecto* y compartirlas entre estaciones de trabajo. Estas preferencias se encuentran en la pestaña <b>Proyectos</b> de la ventana [Preferencias](../../../interface/preferences-window/preferences-window.md).

Esto es muy útil si quieres configurar un entorno de trabajo común para un equipo que trabaja en el mismo proyecto, usando el archivo de proyecto *same* en *todos los* sistemas.

>[!NOTE]
>
> Para obtener más información sobre la configuración e integración de Substance 3D Designer en una **canalización de producción**, *recomendamos encarecidamente* que haga referencia a la sección [Configuración de canalización y proyecto](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) de la documentación.

![Configuración del proyecto](project-settings.resources/2019-3-0-prefs-proj-01.png "Configuración del proyecto"){zoomable="yes"}

## Configuración

### Archivo de configuración

Esto le permite establecer la ruta de acceso del <b>archivo de configuración</b> para Substance 3D Designer. Un archivo de configuración utiliza la extensión <b>\*.sbscfg</b> y contiene una lista de archivos de proyecto junto con una configuración de presentación de compatibilidad establecida.

*Valor predeterminado: default\_configuration.sbscfg*

>[!NOTE]
>
> Puede usar la opción de línea de comandos **—config-file** para iniciar Designer con un archivo de configuración específico.\
> Para obtener más información sobre los archivos de configuración, consulte la página [Lista de configuración - SBSCFG](../../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) de la documentación.

### Archivos de proyecto

Un archivo de proyecto contiene una serie de ajustes que definen aspectos clave del entorno de trabajo en Designer, organizados en fichas. Esta configuración se muestra en el capítulo Proyecto de esta página. Los archivos de proyecto utilizan la extensión <b>\*.sbsprj</b>.

Puede importar varios archivos de proyecto para utilizarlos en su entorno de trabajo en Designer. Cuando existen varios archivos de proyecto, los ajustes que son listas (por ejemplo, rutas controladas de biblioteca, alias, etc.) son *combined*, y los valores de configuración que son valores de conjunto únicos están definidos por el *último archivo de proyecto de la lista*.

*Valor predeterminado: default\_project.sbsprj (solo lectura), user\_project.sbsprj*

>[!NOTE]
>
> Para obtener más información sobre el uso de archivos de proyecto en una canalización de producción, consulte la página [Archivos de configuración del proyecto - SBSPRJ](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) de la documentación.

### Pantalla de compatibilidad

Algunos de los nodos creados con una versión reciente de Designer no son compatibles con versiones anteriores del Substance Engine.

<b>Modo de compatibilidad</b> resaltará los nodos que *no* son compatibles con el Substance Engine seleccionado, con un contorno amarillo.

*Valor predeterminado: Substance Engine v7*

### Vista 3D

|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Procesador predeterminado</b> | Esta configuración le permite seleccionar el [procesador 3D](../../../interface/3d-view/3d-renderers/3d-renderers.md) que debe usarse de forma predeterminada al iniciar una *nueva* [vista 3D](../../../interface/3d-view/3d-view.md).<br><br>*Valor predeterminado: Predeterminado (procesador predefinido)* |
| <b>Sombreador predeterminado</b> | Esta configuración te permite seleccionar el sombreado que se debe usar de forma predeterminada al iniciar una *nueva* [vista 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Predeterminada: open_pbr.glslfx* |
| <b>Mapa de entorno predeterminado</b> | Esta configuración le permite seleccionar la textura que debe aplicarse de forma predeterminada al entorno al iniciar una *nueva* [vista 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Predeterminada: panorama\_map.hdr* |
| <b>Archivo de estado predeterminado</b> | El [archivo de estado de escena **de la &#x200B;](../../../interface/3d-view/3d-view.md)vista 3D** incluye una serie de configuraciones para la vista 3D, como la posición de la cámara, la exposición del entorno y la malla. Se utiliza para almacenar el estado de la vista 3D para que pueda cargar rápidamente una escena que se adapte a sus necesidades. Los archivos de estado de escena utilizan la extensión **\*.sbsscn**.Esta configuración le permite seleccionar el archivo de estado de escena de la vista 3D que debe utilizarse al iniciar una nueva vista 3D.  **Alerta:** Algunas actualizaciones de software pueden cambiar la forma en que se guardan o cargan los estados de escena. Si la escena está *no restaurada correctamente*, se recomienda establecer manualmente el estado deseado de la escena y *volver a exportar* el archivo de estado de escena que usa como predeterminado. <br><br>*Valor predeterminado: Vacío (en este caso, se usa un estado de escena preestablecido)* |
| <b>Estado de iluminación predeterminado</b> | Esta configuración le permite seleccionar cuál de las luces disponibles predefinidas debe habilitarse al iniciar un nuevo [Vista 3D](../../../interface/3d-view/3d-view.md), *si no hay ningún archivo establecido* en el campo **Archivo de estado predeterminado**<br><br>*Valor predeterminado: Solo luz ambiente* |

### Alias

Los alias se usan para *acortar* rutas del sistema y permitir que los equipos *compartan* activos de manera más eficiente. Se utilizan alias *en todo el software*, así como en *archivos SBS*.

Esta configuración le permite *agregar* y *editar* alias. Cuando se aplica un alias, *reemplaza* la ruta asignada con la siguiente sintaxis: <b>://</b>.

Ejemplo: si se coloca un recurso *myResource* en la carpeta *myFolder* en la ubicación *C:/Users/user/Documents*, al asignar esta ubicación a *myalias* se generará la ruta de acceso *myalias://myFolder/myResource* que se está utilizando en la aplicación *y* el paquete SBS al que pertenece el recurso.

*Valor predeterminado: sbs; sd-3dview-shapes; sd-3dview-maps; sd-3dview-shaders (proyecto predeterminado)*

>[!WARNING]
>
> Los alias son *globales para la aplicación*. Esto significa que se aplicarán a *todas las rutas* utilizadas en la aplicación, así como a todas las rutas de *archivos de configuración de proyecto SBSPRJ cargados*. Tenga esto en cuenta al configurar el entorno del proyecto.\
> Además, se recomienda *no anidar* alias, es decir, asignar un alias a una ruta que también está incluida en otro alias.

### Bakers

|                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Nombre de recurso predeterminado</b> | Esta configuración le permite establecer una **plantilla de nomenclatura** predeterminada que se utilizará para los archivos de imagen de salida. Los alias disponibles en la [ventana de hacer un bake](../../../bakers/bakers.md) también se pueden usar aquí (p. ej. *$(mesh)*, *$(bakername)*, *$(udim)*, *$(custom)*)<br><br>*Valor predeterminado: $(mesh)\_$(bakername)* |
| <b>Ajuste preestablecido predeterminado</b> | Al abrir la [ventana de hacer un bake](../../../bakers/bakers.md), puedes configurarla **ya** con bakeres y configuraciones específicas usando esta opción para apuntar a un archivo *JSON* de ajustes preestablecidos. Este archivo se puede exportar desde la ventana de hacer un bake una vez que se haya configurado según sus necesidades <br><br>*Valor predeterminado: Ninguno* |
| <b>modo de filtro de nombres</b> | El objeto de escena cuyo nombre debe utilizarse para hacer coincidir los objetos de escena de poli bajo y poli alto:<ul data-preserve-html="true"> <li data-preserve-html="true">Nombre de la geometría: utilizar el nombre del objeto de geometría de malla</li> <li data-preserve-html="true">Nombre del padre (heredado): usar el nombre del padre del objeto de geometría de malla (igual que en las versiones 14.1 y anteriores de Designer)</li> </ul>*Valor predeterminado: Nombre de geometría* |
| <b>Macros de nombre de recurso</b> | En lugar del alias *$(bakername)*, puede usar sus propias cadenas de caracteres para [cada baker](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings).  Cuando se use el alias ***$(custom)*** en el nombre de imagen de salida de cualquier baker, se reemplazará por la cadena de caracteres que coincida con ese baker en la lista. Si se deja en blanco una celda de la lista correspondiente a un panadero, el alias *$(custom)* *no* se reemplazará para este panadero.Ejemplo: El valor &quot;c-mesh&quot; asignado al panadero &quot;Curvature Map From Mesh&quot; cambiará automáticamente el nombre de *t\_mymesh\_&#x200B;**$(custom)*** por *t\_mymesh\_&#x200B;**c-mesh*** para la salida del panadero Curvature From Mesh *only *<br><br>*Predeterminado: Ninguno* |
| <b>Filtro de nombre de submallas</b> | Cuando se usa la opción **Coincidir por nombre** en [panaderos](../../../bakers/bakers.md), las partes de las versiones de baja y alta definición de una malla se *coinciden* si el nombre de las partes anteriores a los **sufijos** definidos es *idéntico*. Esta configuración le permite establecer sus propios sufijos para que se ajusten a su flujo de trabajo específico. Las partes coincidentes de las mallas pueden hacer que los rayos ignoren la geometría no deseada en las operaciones de horneado.Ejemplo: el objeto *body-torso&#x200B;**\_low*** de la malla *body.fbx* coincidiría con el objeto *body-torso&#x200B;**\_high &#x200B;*** en *body\_high.fbx,* *si estos objetos existen* en estas mallas *.**Valor predeterminado: \_low (Malla de poli baja) / \_high (Malla de poli alta)*Del mismo modo,**&#x200B;backfaces&#x200B;**se pueden *omitir de forma selectiva* para las partes de una malla cuyo nombre incluya el &#x200B;** sufijo&#x200B;**definido, para [panaderos específicos](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings) que incluyen la opción &#x200B;** Ignorar cara posterior**<br><br>* Valor predeterminado: \_ignorebf *<br><br>* Nota:* Los sufijos Ignorar malla de fondo y Poly alta/baja se pueden combinar *en cualquier orden* (p. ej. *body-torso\_low\_ignorebf*) |

### Gestión de colores

Consulte la página [Administración de color](../../../color-management/color-management.md).

>[!WARNING]
>
> Los cambios realizados en esta configuración surtirán efecto después de reiniciar Designer.

### General

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Plantillas de Substance</b> | Al crear un nuevo gráfico, se le pide que empiece a trabajar con una **plantilla** que puede tener una serie de configuraciones y contenido *preconfigurados*, como salidas (p. ej. *PBR (Metallic/Roughness)*). Esta configuración le permite dirigir Designer a directorios en los que puede almacenar sus propios archivos SBS para utilizarlos como plantillas. Las plantillas personalizadas se *agregarán a la lista* al crear un nuevo gráfico <br><br>*Valor predeterminado: Ninguno *<br><br>*Nota:* Se recomienda utilizar las plantillas actuales como referencia para configurar y dar formato a los archivos SBS de plantilla.  Las plantillas se encuentran en la carpeta **resources > templates** del directorio de instalación de Substance 3D Designer. |
| <b>Escenas 3D</b> | De forma predeterminada, Designer utiliza el **espacio de tangente MikkT** en la vista 3D. MikkT se usa mucho y es el valor predeterminado en programas como Unity, Unreal Engine 4, Blender y xNormal. Puede usar **su propio espacio tangente** para la vista 3D, que proporciona a Designer en forma de una entrada de *archivo DLL* en esta configuración. La etiqueta se detecta automáticamente a partir del archivo DLL y puede editar la descripción del complemento <br><br>*Default: mikktspace.dll* Volver a calcular siempre los fotogramas tangentes <br><br>*Valor predeterminado: Desmarcado*&#x200B;Ángulo de suavizado normal y tangente <br><br>*Valor predeterminado: 180,0°* |
| <b>Misc</b> | Las asignaciones normales se pueden generar o procesar usando el formato <b>DirectX</b> o <b>OpenGL</b>. Esta configuración establece el valor de este formato en varios lugares, como [propiedades de material](../../../interface/3d-view/material-properties/material-properties.md) en la [Vista 3D](../../../interface/3d-view/3d-view.md) y los parámetros de nodo de filtro [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md).<br><br>*Valor predeterminado: DirectX*<br><br> En lo que respecta al nodo de filtro [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), puedes establecer el valor predeterminado para el parámetro <b>Contenido del canal del Alpha</b>. Puede elegir forzar el valor alfa a 1 en todos los casos o rellenarlo con información de su entrada.<br><br>*Valor predeterminado: Forzar el Alpha a 1* |
| <b>Formatos de imagen</b> | Esto te permite especificar la configuración de formato predeterminada para *imágenes* exportadas <br><br>*Valor predeterminado: Predeterminado (BMP) / Onda basada en Piz, sin marcar, sin marcar (EXR) / Sin marcar, sin marcar, 75 (JPG) / Mejor velocidad, sin marcar (PNG) / Predeterminado (TGA) / LZW (TIF) / Sin marcar, 75 (WEBP)* |
| <b>Rutas de dependencias</b> | <p>Los paquetes SBS suelen tener <b>dependencias</b>, es decir, dependen de <i>recursos externos</i>, como otros paquetes SBS, mapas de bits o archivos de vectores.<br>Estas dependencias, que se enumeran en el [Administrador de dependencias](../../../interface/dependency-manager/dependency-manager.md), se almacenan y se <i>hace referencia a ellas en el paquete SBS</i> con una <b>ruta</b> que señala a estos recursos.</p><p>Para las dependencias que incluyen la <i>misma ruta</i> que el paquete SBS (es decir, que se encuentran en las mismas ubicaciones o subcarpetas de esa ubicación), la ruta de referencia se escribe <b>relativa a</b> la ubicación del paquete SBS.</p><p>Ejemplo: para un paquete SBS <code>myproject/mypackage.sbs</code>, una imagen <code>myproject/myfolder/myimage.png</code> se hará referencia a <code>myfolder/myimage.png</code> ruta de acceso en <code>mypackage.sbs</code>).</p><p>Para las dependencias que <i>no</i> incluyen la misma ruta de acceso que el paquete SBS (es decir, están ubicadas en una ubicación totalmente diferente del paquete SBS), puede elegir cómo se escribe la ruta de acceso.</p><p>Si se establece en <b>rutas relativas</b>, se hará referencia al recurso de la misma manera que se describe anteriormente.</p><p>Ejemplo: para un paquete SBS <code>myparentfolder/myproject/mypackage.sbs</code>, una imagen <code>myparentfolder/myotherfolder/myimage.png</code> se hará referencia a <code>../myotherfolder/myimage.png</code> ruta de acceso en <code>mypackage.sbs</code>.</p><p>Si se establece en <b>rutas absolutas</b>, se hará referencia al recurso mediante su ruta de acceso completa del sistema.</p><p>Ejemplo: para un paquete SBS <code>myparentfolder/myproject/mypackage.sbs</code>, una imagen <code>myparentfolder/myotherfolder/myimage.png</code> se hará referencia a esta misma ruta completa en <code>mypackage.sbs</code></p><p><i>Valor predeterminado: ...rutas relativas.</i></p><p><i>Nota:</i> En todos los casos, mover los recursos <i>romperá dependencias</i> , lo que dará como resultado <b>nodos de instancia de Ghost</b> en gráficos.  Para <i>consolidar</i> todas las dependencias en una sola carpeta de proyecto junto con el paquete SBS, puede usar la opción <b>Exportar con dependencias...</b> características en el panel [Explorador](../../the-explorer-window/the-explorer-window.md). Esto crea de manera efectiva una carpeta de proyecto <i>autocontenida</i> que se puede mover libremente. |

### Biblioteca

Esta sección te permite <b>administrar el contenido personalizado</b> de la [biblioteca](../../../interface/the-library/the-library.md).

El contenido de todas las carpetas enumeradas en la lista <b>Rutas añadidas</b> se incluirá en la biblioteca. Cualquier cambio en el contenido se refleja en la biblioteca, después de un período de actualización que se puede establecer en la [biblioteca](../../../interface/preferences-window/preferences-window.md) [pestaña](../../../interface/preferences-window/preferences-window.md) de la ventana [Preferencias](../../../interface/preferences-window/preferences-window.md).

En las columnas de la lista, puede encontrar opciones que le proporcionan un control más granular sobre la forma en que el contenido de estas carpetas se agrega a la biblioteca:

* **Habilitado:** El contenido de la carpeta se muestra en la biblioteca (*Predeterminado: Comprobado*)
* **Recursivo:** El contenido de todas las carpetas secundarias también se muestra en la biblioteca (*Predeterminado: Comprobado*)
* **Excluir patrón:** Los archivos cuyo *nombre* coincide con la entrada Regex (expresión regular) son *no* mostrados en la biblioteca (p. ej. `wip-*`). Obtenga más información sobre la sintaxis de la expresión regular [aquí](https://doc.qt.io/qt-5/qregularexpression.html#wildcardToRegularExpression)
* **Excluir extensión:** Los archivos que *extensión* incluye la cadena de texto de entrada *no* se muestran en la biblioteca. Las cadenas múltiples deben estar separadas por `;` puntos y comas. (E.g. `jpg;png;tif;fbx`)

Si se agregan paquetes SBS a la biblioteca, los **gráficos** y **recursos** que contiene se pueden *mostrar en la biblioteca* como entradas independientes, si su parámetro **Visible en biblioteca** está establecido en &#39;Sí&#39;.\
Hay opciones disponibles para definir si este parámetro debe establecerse en &#39;Sí&#39; *de forma predeterminada* al crear o agregar un nuevo gráfico o recurso en un paquete.

*Valor predeterminado: Comprobado*

Si un documento [Photoshop](https://www.adobe.com/products/photoshop.html) (\*.PSD file) incluido en la biblioteca tiene <b>varias capas</b>, una opción te permite mostrar el contenido de* cada capa como una entrada de imagen independiente* en la biblioteca.

*Valor predeterminado: Comprobado*

>[!NOTE]
>
> Aunque los recursos personalizados se agregarán a la biblioteca, es posible que *no esté visible* debido a las reglas de filtrado establecidas para las categorías de biblioteca existentes. Se recomienda crear *filtros propios* organizados en carpetas para garantizar que el contenido se pueda encontrar de manera fiable mientras se trabaja en los proyectos.\
> Consulte la sección [Administración de contenido y filtros personalizados](../../the-library/managing-custom-content/managing-custom-content-and-filters.md) de la documentación para obtener más información.

### Python

Substance 3D Designer cargará automáticamente todos los [complementos](../../../scripting/plugin-basics/plugin-basics.md) ubicados en las carpetas que agregue a la lista <b>Url</b>.

*Valor predeterminado: Ninguno*

>[!WARNING]
>
> Los cambios realizados en esta configuración surtirán efecto después de reiniciar Designer.\
> [Los paquetes de complementos](../../../scripting/plugins-packages/plugins-packages.md) aún deben instalarse *manualmente* con el [Administrador de complementos](../../../scripting/plugin-manager/plugin-manager.md).

### Scripts

>[!WARNING]
>
> Esta característica se *retirará* en una futura versión para favorecer la **API de Python**, que es más robusta. Por lo tanto, le recomendamos que modifique los scripts lo antes posible.\
> Puede ir a la página [Devoluciones de llamadas de aplicación](../../../scripting/application-callbacks/application-callbacks.md) en la sección [Secuencias de comandos](../../../scripting/scripting.md) de nuestra documentación para comenzar.

Esta sección te permite configurar y controlar *scripts* para que se ejecuten cuando se produzcan *eventos* específicos en Designer. Resulta especialmente útil cuando se usa junto con la integración de [Perforce](https://www.perforce.com/), que se puede configurar en la ficha Control de versiones de la configuración del proyecto.

|                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Acciones</b> | Designer tiene **desencadenadores de devolución de llamada** preconfigurados, que *ejecutarán el script* que proporciones mediante el intérprete configurado en la lista de **intérpretes** que se describe a continuación.Las devoluciones de llamada incluidas son las siguientes:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>onBeforeFileLoaded</strong>: ejecuta el script <em>antes</em> de que se cargue un paquete de SBS</li><li data-preserve-html="true"><strong>onAfterFileLoaded</strong>: ejecuta el script <em>after</em> después de cargar un paquete de SBS</li><li data-preserve-html="true"><strong>onBeforeFileSaved</strong>: ejecuta el script <em>antes</em> de que se guarde un paquete SBS</li><li data-preserve-html="true"><strong>onAfterFileSaved</strong>: ejecuta el script <em>después de</em> guardar un paquete SBS</li><li data-preserve-html="true"><strong>getGraphExportOptions</strong>: ejecuta el script cuando se llaman las opciones [Export Outputs](../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)</li></ul>Se incluye un script [Python](https://www.python.org/) en los archivos de instalación, con las funciones desencadenadas por cada devolución de llamada *ya configuradas* y listas para usarse. Puede utilizarlo como punto de partida y añadir funciones según sus necesidades. Este script es **functions.py**, que se encuentra en la carpeta **tools > scripting** de los archivos de instalación <br><br>*Predeterminado: Ninguno *<br><br>*Nota:* Al principio, al seleccionar un script para cualquiera de las devoluciones de llamada, se introducirá ese script en *todas las devoluciones de llamada* para mayor comodidad. Puede configurar libremente diferentes scripts para devoluciones de llamada específicas después de ese punto. |
| **Intérpretes** | En esta lista, puede proporcionar *intérpretes* específicos que Designer debe usar para ejecutar los scripts configurados en la lista **Actions** descrita anteriormente. Los intérpretes se identifican mediante un *alias personalizado* que puedes editar en el campo de texto de cada entrada de la lista.Un intérprete de [Python](https://www.python.org/) 3.6 se incluye con los archivos de instalación de Designer. Puedes encontrarlo en la carpeta **plugins > pythonsdk** de los archivos de instalación <br><br>*Predeterminado: Ninguno* |

### Control de versión

>[!WARNING]
>
> [Perforce](https://www.perforce.com/) es la herramienta *only* que se admite actualmente para el control de versiones.

Consulte la página [Control de versiones](../../../interface/preferences-window/version-control/version-control.md).

**¿Cómo deberías usar esto?**

Debe establecer todas las preferencias *específicas del proyecto* en un archivo de proyecto (\*.sbsprj) en Designer. Estas preferencias incluyen:

* Complemento de espacio de Tangent
* Biblioteca
* Alias
* Ajustes de vista 3D
* Configuración de horneado
* [Configuración de Control de versiones](../../../interface/preferences-window/version-control/version-control.md)

Todas las rutas de acceso se almacenan *en relación con* el archivo de proyecto (.spsprj). para que puedas tener una carpeta **library** en la misma ubicación que tu archivo de proyecto en Perforce, con el siguiente árbol de subcarpetas :

* mapas/
* mallas/
* sbs/
* sbsar/
* psd/
* Vista 3D/
* ...

En el mismo nivel que el archivo de proyecto, también puede almacenar un complemento de espacio tangente o un sombreador predeterminado.

El archivo de configuración (\*.sbscfg) debe colocarse en el espacio de trabajo de Perforce, junto al archivo de proyecto.

>[!NOTE]
>
> Para obtener más información sobre la configuración e integración de Substance 3D Designer en una **canalización de producción**, *recomendamos encarecidamente* que haga referencia a la sección [Configuración de canalización y proyecto](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) de la documentación.
