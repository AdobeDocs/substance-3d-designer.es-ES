---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: Acceda a la ventana Preferencias de Substance 3D Designer para personalizar la configuración y el comportamiento de la aplicación.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Preferencias
user-guide-description: ''
user-guide-title: ''
source-git-commit: b1b28e909a4d3c19c1dbc28e5ed25b3adc327ac3
workflow-type: tm+mt
source-wordcount: '2030'
ht-degree: 1%

---


# Ventana Preferencias

![Ventana de preferencias](../../assets/image2021-6-22-20-56-1.png "Ventana de preferencias")

Esta página presenta la ventana <b>Preferencias</b> y toda su configuración.

Puedes encontrar la ventana Preferencias a través del menú <b>Editar</b> en la barra superior principal de la aplicación. Este cuadro de diálogo le permite ajustar una serie de ajustes. Se organiza en fichas que cubren diferentes áreas de comportamiento y funcionalidad.\
Se recomienda revisar todas estas opciones de configuración para obtener una mejor información sobre cómo funciona la aplicación y cómo se puede adaptar a su flujo de trabajo.

>[!NOTE]
>
> Para obtener más información sobre cómo se almacenan estas preferencias y cómo se pueden integrar en un entorno de producción, consulte la página [Preferencias de usuario - Automatización del programa de instalación](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) de la documentación.

## General

### Documentos recientes

|  |  |
| --- | --- |
| <b>La lista de documentos recientes contiene</b>  *Valor predeterminado: 10* | Esto le permite seleccionar el número de documentos que desea enumerar en la entrada <b>Paquetes recientes</b> del elemento <b>Archivo</b> en el [Menú principal](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html). |

### Historial

|  |  |
| --- | --- |
| **Tamaño de pila de historial** *Predeterminado: 200* | Indica el número de operaciones de deshacer disponibles en cualquier momento en el elemento <b>Editar > Deshacer</b> del [menú principal](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html).  **Precaución:** Cuantas más operaciones de deshacer necesite, más memoria necesitará la aplicación. |

### Idioma

|  |  |
| --- | --- |
| **Elegir el idioma de la aplicación** *Valor predeterminado: Sistema* | Esta configuración define el idioma utilizado en la interfaz de la aplicación. La opción &#39;*System*&#39; detecta automáticamente el idioma a partir de la configuración de idioma del sistema. Los idiomas disponibles se enumeran en [Requisitos del sistema](../../getting-started/system-requirements/system-requirements.md).  **Nota:** El cambio de esta configuración solo surtirá efecto después de reiniciar la aplicación. |

### Vistas

|  |  |
| --- | --- |
| <b>Invertir zoom en vistas</b>  *Valor predeterminado: Desmarcado* | Si se marca, los controles de zoom se invertirán en la [vista 2D](../../interface/2d-view/2d-view.md), la [vista 3D](../../interface/3d-view/3d-view.md) y los [gráficos](../../interface/the-graph-view/the-graph-view.md). |

### Rutas

|  |  |
| --- | --- |
| <b>Ruta para guardar/exportar</b>  *Valor predeterminado: Última ruta* | Determina si la ruta de acceso sugerida para guardar o exportar es la última ruta seleccionada o la ruta del [paquete SBS](../../getting-started/overview/overview.md). La última ruta seleccionada se guarda entre sesiones. |
| <b>Carpeta temporal</b>  *Valor predeterminado: Ruta de acceso según el sistema operativo* | Cuando los datos de imagen de un gráfico exceden el grupo de memoria asignado (vea a continuación <b>Memoria > Caché de imagen</b>), los datos desbordados se escriben en el disco. Esta configuración le permite definir la ubicación en la que se escriben los datos de caché de imágenes desbordantes.   Esta ubicación también se utiliza para almacenar una copia del paquete SBS abierto actualmente con las modificaciones más recientes desde el último guardado manual. |

### Memoria

#### Caché de imagen

La aplicación mantiene en la caché una *imagen sin comprimir de resolución completa* para cada nodo procesado en el gráfico actual.\
Los nodos de instancia generarán estas imágenes para todos los nodos del gráfico al que hacen referencia y las eliminarán una vez que se hayan calculado sus [salidas](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). En ese momento sólo se guardan en memoria las salidas.

Puede establecer el tamaño máximo de caché asignado a las miniaturas y las imágenes en la memoria del sistema, y ver el uso actual. Si los datos de la caché desbordan su grupo asignado, los datos sobrantes se escriben en la <b>carpeta temporal</b> (consulte la información anterior <b>Rutas > Carpeta temporal</b>).

|  |  |
| --- | --- |
| <b>Presupuesto de memoria</b>  *Valor predeterminado: Automático* | Esta asignación se calcula automáticamente a aproximadamente el 75% del total del grupo de memoria del sistema. Para establecer este valor manualmente, seleccione la opción &#39;*Custom*&#39; y establezca un valor en el campo de entrada adyacente. |

Tenga en cuenta que escribir en el disco es *órdenes de magnitud más lento* que escribir en la memoria del sistema. Por lo tanto, el tiempo de procesamiento del gráfico *aumentará exponencialmente*, ya que los datos desbordados deben escribirse en la carpeta temporal.\
Para evitar que esto suceda, recomendamos consultar las sugerencias para reducir el espacio de memoria de un gráfico en la sección [Directrices de optimización del rendimiento](../../best-practices/performance-optimization/performance-optimization-guidelines.md) de la documentación.

#### Programador de trabajos

Durante tareas específicas, como las conversiones de imágenes para miniaturas o la [vista 2D](../../interface/2d-view/2d-view.md), se crearán trabajos independientes y se distribuirán entre los núcleos de procesamiento del sistema para mejorar la eficiencia. Cada trabajo escribirá datos en la memoria del sistema para realizar sus operaciones.\
Esta configuración le permite definir el grupo de memoria asignado para *todos los trabajos simultáneos*. Cuando este grupo se utiliza por completo, los nuevos trabajos se pondrán en cola hasta que se hayan completado los actuales.

|  |  |
| --- | --- |
| <b>Presupuesto de memoria</b>  *Valor predeterminado: Automático* | Esta asignación se calcula automáticamente a aproximadamente el 10% del total del grupo de memoria del sistema. Para establecer este valor manualmente, seleccione la opción &#39;*Custom*&#39; y establezca un valor en el campo de entrada adyacente. |

### Interfaz de usuario

|  |  |
| --- | --- |
| **Deshabilitar ppp alta** *Valor predeterminado: Desmarcado* | El modo <b>ppp alto</b> mantendrá una escala coherente del texto y los elementos de la interfaz de usuario *independientemente* de la configuración de visualización y escala del sistema.   Al deshabilitar (es decir, la casilla de verificación *filled*), esta configuración permitirá escalar la interfaz, lo que dará como resultado texto más grande y legible en algunas pantallas, pero también puede crear incoherencias en el tamaño del texto, junto con otros problemas de diseño.  **Precaución:** Designer adquiere la escala específica de los elementos de la interfaz de usuario *del sistema operativo*. Por lo tanto, cualquier ajuste en la escala de la interfaz de usuario debe realizarse en la configuración de visualización del sistema operativo. Para garantizar que la configuración de visualización se aplique correctamente en Designer, *cierre sesión* de la sesión de usuario del sistema operativo y vuelva a iniciar sesión después de cambiar esta configuración.  **Nota:** El cambio de esta configuración solo surtirá efecto después de reiniciar la aplicación. |

### Copia de seguridad automática

De forma predeterminada, se incluye una función de guardado automático, que crea copias del estado actual de [paquetes SBS](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion) abiertos en períodos de tiempo establecidos. Los guardados automáticos se colocan en una carpeta <b>.autosave</b> en la ubicación del paquete SBS.

|  |  |
| --- | --- |
| <b>Copia de seguridad automática cada # minutos</b>  *Valor predeterminado: 5* | El período de tiempo entre cada guardado automático. |
| <b>Mantener hasta # versiones</b>  *Valor predeterminado: 6* | El número máximo de guardados automáticos que se pueden mantener en cualquier momento. |

Cuando se alcanza la cantidad máxima de versiones, las copias de seguridad más recientes eliminarán las más antiguas.\
Tenga en cuenta también que los guardados automáticos deben abrirse *después de moverlos* a la ubicación del paquete SBS original. *no* debe abrirse en su ubicación actual.

### Publicar y enviar archivos SBSAR

|  |  |
| --- | --- |
| <b>Guardar siempre el archivo .sbs al publicar en .sbsar o enviar a otra aplicación</b>  *Valor predeterminado: True* | Controla el guardado automático del paquete SBS al [publicarlo](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) o [enviarlo a otra aplicación](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html). |

### Cocina

|  |  |
| --- | --- |
| <b>Límite de tamaño de cocción</b>  *Valor predeterminado: 8192 píxeles* | Define la resolución máxima de píxeles permitida para todos los [nodos](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/sddoc/nodes-reference-129368078.html) en cualquier [gráfico](../../compositing-graphs/substance-compositing-graphs.md). Como las salidas de gráficos son siempre imágenes cuadradas de resoluciones de potencias de 2, el valor definido aquí define tanto la anchura como el height máximos, en píxeles. |

### Motor

|  |  |
| --- | --- |
| <b>Límite de caché de GPU</b>  *Valor predeterminado: 2048 MB* | Este ajuste permite definir la cantidad de memoria que se debe reservar para almacenar en caché las fases de procesamiento. Normalmente, el Substance Engine almacenará en caché el resultado de cada nodo en un gráfico del Substance. |

>[!NOTE]
>
> Recomendamos examinar las sugerencias para reducir el espacio de memoria de un gráfico en la sección [Performance Optimization Guidelines](../../best-practices/performance-optimization/performance-optimization-guidelines.md) de la documentación.

## Proyectos

Consulte la página [Configuración de proyectos](../../interface/preferences-window/project-settings/project-settings.md).

## Gráfico

### Común

|  |  |
| --- | --- |
| <b>La tecla de tabulación muestra el menú de nodos</b>  *Valor predeterminado: Comprobado* | Si se marca, la tecla &quot;Tab&quot; abrirá el menú <b>Nodo</b>, replicando la funcionalidad de la clave &quot;Space&quot;. |
| <b>Habilitar la creación de nodos haciendo clic y arrastrando conectores</b>  *Valor predeterminado: Comprobado* | Si está marcado, al hacer clic en cualquier conector, arrastre el cursor y suelte el vínculo creado en el espacio vacío del gráfico para mostrar el <b>menú Nodo</b>.   El menú también se *filtrará* según el tipo de conector en el que se haya hecho clic. Esto significa que sólo se mostrarán los nodos compatibles con el conector en el que se ha hecho clic. |
| <b>Ver resultados en vista 3D al abrir un gráfico</b>  *Valor predeterminado: Comprobado* | Si se marca, todas las salidas de gráficos se aplican automáticamente en la [vista 3D](../../interface/3d-view/3d-view.md) cuando se abre ese gráfico.   Esto también tiene el efecto de representar todos los nodos que forman parte de una secuencia que conduce a un nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |

### Gráfico de composición de Substance

|  |  |
| --- | --- |
| <b>Calcular automáticamente todas las miniaturas de nodos al abrir un gráfico</b>  *Valor predeterminado: Comprobado* | Si se selecciona, se procesan automáticamente todas las miniaturas de nodo al cargar el gráfico. |
| <b>Ver salida en vista 2D al abrir un gráfico</b>  *Valor predeterminado: Comprobado* | Si se marca, la primera salida del gráfico se muestra automáticamente en la [vista 2D](../../interface/2d-view/2d-view.md) cuando se abre ese gráfico. Esto también tiene el efecto de representar todos los nodos que forman parte de una secuencia que conduce a ese nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |
| <b>Mostrar automáticamente el nodo de composición recién creado</b>  *Valor predeterminado: Comprobado* | Si se marca, la [vista 2D](../../interface/2d-view/2d-view.md) se actualizará automáticamente para mostrar el resultado de un nodo recién creado. |
| <b>Insertar automáticamente nodo de conversión de color/escala de grises</b>  *Valor predeterminado: Desmarcado* | Si está marcado, resuelve automáticamente los desajustes de los tipos de conexión de color/escala de grises, *colocando nodos específicos* para realizar la conversión adecuada.   Cuando una salida *Grayscale* (conector gris) está conectada a una entrada *Color* (conector amarillo), se coloca automáticamente un nodo [Gradient Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) entre los dos conectores.   Cuando se conecta una salida de *Color* (conector amarillo) a una entrada de *Escala de grises* (conector gris), se coloca automáticamente un nodo de [Conversión de escala de grises](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) entre los dos conectores. |
| <b>Habilitar la edición de gráficos en contexto</b>  *Valor predeterminado: Desmarcado* | De forma predeterminada, al abrir un gráfico al que hace referencia un [nodo de instancia](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) haciendo clic con el botón derecho en el nodo y seleccionando <b>Abrir referencia</b>, ese gráfico se carga y se edita *de forma aislada*.   Si está marcado, puede editar gráficos a los que hacen referencia las instancias *utilizando la información pasada en la instancia* por el gráfico actual. Para ello, haga clic con el botón derecho en un nodo de instancia y seleccione <b>Abrir referencia en contexto</b>, o utilice la tecla Ctrl+E.   Esto significa que un gráfico instanciado se puede editar en el contexto del gráfico en el que se crea una instancia. Esto resulta muy útil para ver los efectos de las ediciones en el gráfico en el que estaba trabajando. Consulte el ejemplo siguiente.  **Nota:** Las pestañas <b>Vista previa</b> y <b>Ajustes preestablecidos</b> están *deshabilitadas* en las [propiedades del gráfico](../../compositing-graphs/graph-parameters/graph-parameters.md) al utilizar la edición en contexto. |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Edición en contexto deshabilitada](../../assets/substance3ddesigner_incontext_no.gif "Edición en contexto deshabilitada")

*Abrir referencia*

</td>
<td style="border: 0;" valign="top">

![Edición en contexto habilitada](../../assets/substance3ddesigner_incontext_yes.gif "Edición en contexto habilitada")

*Abrir Referencia En Contexto*

</td>
</tr>
</table>

## Vista 3D

### Varios

|  |  |
| --- | --- |
| <b>Entorno oculto de forma predeterminada</b>  *Valor predeterminado: Comprobado* | Determina la configuración de visibilidad predeterminada de [Entorno](../../interface/3d-view/3d-view.md). Cuando está oculto, el fondo de la vista 3D se reemplaza por un *color sólido*. |
| <b>Escala de ventana</b>  *Valor predeterminado: Automático* | Controla la escala de la resolución de procesamiento de la vista 3D cuando el sistema utiliza la escala de visualización.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Automático</i>: la resolución de representación se basa en la resolución de visualización <i>escalada</i></li> <li data-preserve-html="true"><i>Ninguno</i>: la resolución de representación se basa en la resolución de visualización <i>nativa</i></li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>Recuento de muestras</b>  *Valor predeterminado: 64* | Afecta al tamaño de la tabla de ejemplo de los sombreadores de vistas 3D. Un valor más alto producirá una mayor calidad de imagen a costa del rendimiento.  **Nota:** La tabla de ejemplos de sombreadores también se ve afectada por la GPU y el sistema operativo del sistema. |

## Bakers

|  |  |
| --- | --- |
| <b>Trazado de rayos de GPU</b>  *Valor predeterminado: Comprobado* | Si se marca, el trazado de rayos se realizará en la GPU para [panaderos compatibles](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing).   Los siguientes backends de Trazado de rayos de GPU serán los predeterminados según la arquitectura de GPU NVIDIA:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i>: Turing y más reciente</li> <li data-preserve-html="true"><i>Optix</i>: Pascal y Maxwell</li> </ul>  **Nota:** Encontrarás más información sobre panaderos impulsados por GPU en la sección [Trazado de rayos de GPU](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) de la documentación de [Substance Bakers](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home).  **Sugerencia:** Puede usar los siguientes *argumentos de línea de comandos* al iniciar la aplicación para *forzar* el uso de un motor de Trazado de rayos de GPU diferente: <ul data-preserve-html="true"> <li data-preserve-html="true"><code>: force-optix</code> : forzar el uso de Optix en Nvidia Turing o en GPU más nuevas</li> <li data-preserve-html="true"><code>: force-dxr</code> : forzar el uso de DXR en las GPU Nvidia Pascal</li> </ul> |

## Biblioteca

|  |  |
| --- | --- |
| <b>Reconstruir miniaturas</b> | La opción activará un nuevo cálculo de todas las miniaturas de [Library](../../interface/the-library/the-library.md), que reemplazará automáticamente las anteriores. |

## Mét. abrev.

Puede asignar métodos abreviados de teclado personalizados para crear nodos en gráficos.

Los accesos directos se pueden asignar a nodos en todos los tipos de gráficos: [Gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), [Gráficos de funciones de Substance](../../function-graphs/function-graphs.md) y [Gráficos FX-Map](../../function-graphs/fxmaps/fxmaps.md).

A cualquier nodo se le puede asignar un método abreviado, incluso nodos de biblioteca personalizados. Se puede asignar el mismo método abreviado en diferentes tipos de gráfica. No se asignan métodos abreviados de teclado de forma predeterminada, puede personalizarlos a su gusto.

En caso de conflicto con otro método abreviado de nodo o con un método abreviado de programa integrado, se resaltará la entrada y se mostrará una advertencia. El acceso directo no tendrá *ningún efecto* hasta que se resuelva el conflicto.

>[!IMPORTANT]
>
> Accesos directos anulados por complementos de Python
> 
> Cuando un complemento de Python define un método abreviado de teclado asignado a un nodo, el complemento sobrescribirá ese método abreviado. Esto significa que la clave activará la acción del complemento en lugar de crear un nodo.
> 
> Este ya es el caso de las claves H, S y V utilizadas por las [herramientas de alineación de nodos](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md).
