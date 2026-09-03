---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/preferences-window/version-control.html"
breadcrumb-title: ''
description: Configure los ajustes de control de versiones en las preferencias de Substance 3D Designer para integrarlos con Git y otros sistemas.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Version control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Control de versiones
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Control de versiones

>[!IMPORTANT]
>
> La versión de Substance 3D Designer <b>14.0.0</b> actualiza la compatibilidad con Perforce a <b>Python 3</b>.
> 
> Asegúrese de que las demás secuencias de comandos y el entorno de control de versiones se ajusten en consecuencia.

Designer ofrece una integración en Python del sistema de control de versiones [Perforce](https://www.perforce.com/) (P4).

La integración agrega un submenú personalizado &#39;Control de versiones&#39; al menú contextual de los paquetes en el [Explorador](../../../interface/the-explorer-window/the-explorer-window.md), así como iconos personalizados para que coincidan con el estado de un paquete en P4.

## Preparando P4

En [P4V](https://www.perforce.com/products/helix-core-apps/helix-visual-client-p4v), anote el nombre y la ruta del área de trabajo, como se muestra a continuación:

![Información del área de trabajo P4V](version-control.resources/version-control-01.jpg "Información del área de trabajo P4V"){zoomable="yes"}

En cualquier editor de texto o IDE, abra esta secuencia de comandos ubicada en la instalación de Designer: &#39;*tools/version\_control/perforce.py*&#39;.

En la línea 19, edite la ruta de acceso a la ubicación del ejecutable <b>&#39;p4&#39;</b> en su sistema.\
En el ejemplo siguiente, esta ruta es &#39;*c:/Program Files/Perforce/p4.exe*&#39;.

```
## Editable variables

cPerforceP4AbsPath = os.path.abspath("c:/Program Files/Perforce/p4.exe")

cVerbose = False
```


## Configuración en Designer

El control de versiones está configurado en [Configuración del proyecto](../../../interface/preferences-window/project-settings/project-settings.md), que están disponibles en [Preferencias](../../../interface/preferences-window/preferences-window.md) de Designer.

Ficha ![&#39;Control de versiones&#39; en la configuración del proyecto](version-control.resources/version-control-02.jpg "&#39;Ficha Control de versiones&#39; en la configuración del proyecto"){zoomable="yes"}

1. Vaya a &quot;Editar > Preferencias&quot;
1. Vaya a &quot;Proyectos&quot;, seleccione el [archivo de proyecto](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) de destino y vaya a la pestaña &quot;Control de versiones&quot;
1. Marque &quot;Control de versiones habilitado&quot;
1. Rellene esta información en la sección &quot;Espacio de trabajo&quot;:

   * <b>Nombre:</b> Escriba el &#39;Nombre del área de trabajo&#39; que recuperó anteriormente de P4V
   * <b>Ruta de acceso:</b> escriba la &#39;Ruta de acceso del área de trabajo&#39; que recuperó anteriormente de P4V

Configuración de ![P4 en Designer: área de trabajo](version-control.resources/version-control-03.jpg "configuración P4 en Designer: área de trabajo"){zoomable="yes"}

### Configuración de acciones

Las acciones estarán disponibles en el menú contextual de un paquete en el Explorador. Hay acciones predefinidas que coinciden con la mayoría de los conceptos de la herramienta Control de versiones:

* Todas las etiquetas de acción se pueden cambiar según sea necesario.
* Todas las acciones necesitan un script para ser válidas.

Puede utilizar:

* una acción de script *por*
* un script para *todas* las acciones

Hay disponible una secuencia de inicio para todas las acciones en la instalación de Designer: &#39;*tools/version\_control/perforce.py*&#39;.

>[!IMPORTANT]
>
> Para que esté disponible, el paquete debe guardarse en la &#39;ruta del espacio de trabajo&#39; (p. ej., en &#39;*f:/Dev/perforce*&#39;)

1. En el grupo <b>Acciones</b>, haga clic en el icono &#39;...&#39; de la acción <b>Agregar</b>
1. Seleccione el siguiente script en la instalación de Designer: &#39;*tools/version\_control/perforce.py*&#39;
1. El script debe configurarse automáticamente para todas las demás acciones.

Configuración de ![P4 en Designer: acciones](version-control.resources/version-control-04.jpg "Configuración de P4 en Designer: acciones"){zoomable="yes"}

### Configuración de acciones personalizadas

Como todas las herramientas de control de versiones son diferentes e incluyen muchas características, permitimos que el usuario agregue acciones personalizadas.

1. Haga clic en &#39;Agregar elemento&#39;
1. Rellene la etiqueta de la nueva acción y defina su ruta de script

### Configuración del intérprete de secuencias de comandos

1. En la sección &quot;Intérpretes&quot;, haga clic en &quot;Agregar elemento&quot;
1. Establezca una extensión de archivo de script o un sufijo, y la ruta de acceso al ejecutable del intérprete
1. Edite el script perforce.py para actualizar la ubicación del binario &#39;p4&#39;

Configuración de ![P4 en Designer: intérprete](version-control.resources/version-control-05.jpg "Configuración de P4 en Designer: intérprete"){zoomable="yes"}

## Cómo utilizar el control de versiones

1. Crear un nuevo paquete
1. Guarde el paquete en el directorio &#39;Workspace path&#39;
1. Haga clic en RMB en el paquete: ahora tiene acceso al submenú &quot;Control de versiones&quot;
1. Hay varias acciones disponibles, en función del estado del archivo del paquete en el espacio de trabajo:

   * <b>Agregar:</b> Marque los archivos como &#39;Para agregar&#39;
   * <b>Enviar:</b> Envíe los paquetes seleccionados. Esta acción muestra un cuadro de diálogo para especificar un mensaje de cambio (véase a continuación)
   * <b>Revertir:</b> Revierta las modificaciones. Esta acción muestra un cuadro de diálogo para seleccionar los archivos que desea revertir (consulte a continuación)
   * <b>Retirar:</b> Desproteger el archivo de la estación de almacenamiento
   * <b>Obtener última versión:</b> Recuperar la última versión del almacén
   * <b>Actualizar estado:</b> Actualizar el estado del archivo del paquete

   <table>
   <tr style="border: 0;">
   <td style="border: 0;" valign="top">

   Cuadro de diálogo ![&#39;Enviar&#39;](version-control.resources/version-control-06.jpg "&#39;Enviar&#39;"){zoomable="yes"}

   </td>
   <td style="border: 0;" valign="top">

   Cuadro de diálogo ![&#39;Revertir&#39;](version-control.resources/version-control-07.jpg "&#39;Revertir&#39;"){zoomable="yes"}

   </td>
   </tr>
   </table>

>[!NOTE]
>
> Todas las acciones admiten la selección múltiple
> 
> Para P4 y otras herramientas de Control de versiones que utilizan permisos de archivo de solo lectura para restringir las modificaciones, el usuario deberá retirar el paquete antes de modificarlo.
> 
> Los archivos de paquete de solo lectura no se pueden modificar en SD.

El paquete tendrá los siguientes iconos, dependiendo de su estado:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Icono de paquete: Actualizado](version-control.resources/version-control-08.png "Icono de paquete: Actualizado")

Actualizado

</td>
<td style="border: 0;" valign="top">

![Icono de paquete: Retirado](version-control.resources/version-control-09.png "Icono de paquete: Desprotegido")

Desprotegido

</td>
<td style="border: 0;" valign="top">

![Icono de paquete: Añadido](version-control.resources/version-control-10.png "icono de paquete: Agregado")

Marcado para agregar

</td>
<td style="border: 0;" valign="top">

![Icono de paquete: No está en depósito](version-control.resources/version-control-11.png "Icono de paquete: No está en el almacén")

No en depósito

</td>
</tr>
</table>

Tenga en cuenta que un paquete que no está actualizado está marcado con un signo de advertencia.

## Scripts de acción

El comando ejecutado por cada acción se genera de este modo:

my\_script <b>*WorkspaceName WorkspacePath ActionName[ActionArgs]*</b>

<b>WorkspaceName:</b> el nombre del área de trabajo

<b>WorkspacePath:</b> la ruta de acceso del directorio raíz del área de trabajo

<b>ActionName:</b> el nombre de la acción:

* *agregar:* para la acción &quot;Agregar&quot;
* *desprotección:* para la acción &quot;Desprotección&quot;
* *enviar:* para la acción &quot;Enviar&quot;
* *revertir:* para la acción &quot;Revertir&quot;
* *get\_last\_version:* para la acción &quot;Obtener última versión&quot;
* *get\_status:* para la acción &quot;Obtener estado&quot;

La etiqueta se configura en la configuración del proyecto, con el carácter &#39; &#39; reemplazado por &#39;\_&#39;, por ejemplo: &quot;Mi acción&quot; => &quot;Mi\_acción&quot;.

<b>ActionArgs:</b> argumentos de la acción:

* *-desc*: Una cadena de descripción utilizada por la acción &#39;Enviar&#39;
* *-archivos:* Una lista de archivos
* *-files\_list:* Archivo de texto que contiene una lista de archivos por línea

<b>get\_status</b>: Devuelve un valor en función del estado del archivo especificado:

* 0: Estado no definido
* 1: no en el depósito
* 2: versión anterior (no actualizada)
* 3: última versión (actualizada)
* 4: retirado
* 5: marcado para adición
* otras acciones:
  * 0: éxito
  * otros: error
