---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Solucione problemas al crear o cargar proyectos en Substance 3D Designer y encuentre soluciones.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: No se puede crear un proyecto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# No se puede crear o cargar un proyecto

En esta página se enumeran las causas comunes por las que no se pueden crear o cargar proyectos en Substance 3D Designer, y se ofrecen pasos de solución de problemas para cada una de ellas.

## La aplicación es demasiado antigua para abrir la URL

**![(error)](../../assets/error.svg) Problema**

El **archivo Substance 3D (SBS)** se está cargando en una versión de Substance 3D Designer que *no admite su formato*. Es probable que el archivo de Substance 3D *se haya guardado en una versión más reciente* del software que usa un formato actualizado para estos archivos.

**![(marca)](../../assets/check.svg) Pasos recomendados**

A medida que Substance 3D Designer evoluciona, también lo hace el formato de archivo Substance 3D (SBS). La mayoría de las veces, una nueva versión del software tendrá que *actualizar tus archivos* para que puedan admitir las funciones más recientes.

*Se le solicita* que realice esta actualización al *cargar el archivo por primera vez* en una nueva versión.

>[!WARNING]
>
> Si el archivo se guarda *después de* que se aplicó la actualización, su versión de formato también cambia. En este momento, *ya no se puede cargar en versiones anteriores* de Substance 3D Designer.
> 
> Esta limitación también se aplica al [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

En primer lugar, compruebe que utiliza la versión más reciente de Substance 3D Designer que permita su licencia actual. Estos son los puntos de acceso a las actualizaciones para cada edición:

* <b>Suscripción de Substance 3D de Adobe:</b> vaya a la sección Actualizaciones de la pestaña Aplicaciones en la aplicación [Adobe Creative Cloud Desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud)
* <b>[Substance3d.com](http://Substance3d.com) suscripción:</b> actualice cuando se le solicite en Substance 3D Designer o descargue el instalador más reciente en la sección [Mis licencias](https://store.substance3d.com/user) del sitio web [Substance3d.com](http://substance3d.com)
* <b>Steam:</b> la aplicación se actualizará automáticamente de forma predeterminada. Puede activar la actualización manualmente iniciando Substance 3D Designer o yendo a la pantalla Descargas

>[!WARNING]
>
> Asegúrate de que no tienes que cargar tus archivos en una versión anterior de Substance 3D Designer *antes de guardar* un archivo que se actualizó.
> 
> También puedes *hacer una copia* del archivo *antes* de cargarlo en una nueva versión de Substance 3D Designer, de modo que siempre tengas un archivo al que volver si necesitas usar una versión anterior del software.

## Bloqueo al crear o cargar un proyecto

<b>![(error)](../../assets/error.svg) Problema</b>

A menudo, un bloqueo al crear o cargar un proyecto se debe a un error durante la inicialización de la [vista 3D](../../interface/3d-view/3d-view.md), que se produce cuando se configura el área de trabajo.

Si el sistema es un portátil, una aplicación de terceros puede aplicar un *plan de administración de energía* que impida que la vista 3D use la GPU del sistema. Esto puede provocar un bloqueo si ningún otro dispositivo de GPU puede realizar la tarea en su lugar.

También puede producirse un bloqueo al cambiar la configuración de visualización o la escala *entre sesiones, de modo que el marco de procesamiento de la vista 3D se cree en coordenadas no válidas.*

<b>![(tick)](../../assets/check.svg) Pasos recomendados</b>

Teniendo en cuenta las múltiples causas posibles de este bloqueo, le recomendamos que siga estos pasos de solución de problemas en orden:

Actualizar controladores gráficos

En primer lugar, asegúrese de que los controladores gráficos estén actualizados. Puedes encontrar la versión más reciente de tu GPU [aquí](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA), [aquí](https://www.amd.com/en/support) (AMD) o [aquí](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel).

Exigir el mejor rendimiento

Busque cualquier software que administre el *plan de energía* del sistema (p. ej., la caja de la armería ASUS), especialmente cuando el sistema sea un portátil.

Algunas aplicaciones de administración de energía pueden limitar el acceso de otras aplicaciones a la GPU del sistema o afectar al rendimiento de la GPU, lo que puede producir bloqueos. Si ya existe una aplicación de administración de energía y está activa, cambie al plan que ofrezca el mejor rendimiento.

Forzar uso de GPU discreta

Si tu sistema tiene *gráficos intercambiables*, plantéate forzar el uso de la GPU discreta (dGPU) para las aplicaciones de Substance 3D.

En la mayoría de los casos, esto se consigue en una aplicación dedicada que controla la configuración de la GPU. Por ejemplo, para las GPU NVIDIA puede hacerlo en la aplicación &quot;Panel de control de NVIDIA&quot;.

Restablecer la interfaz de usuario guardada en el Registro

Si el bloqueo se debe a un cambio en la configuración de visualización o la escala, puede intentar eliminar las entradas del registro existentes para Designer para restablecer por completo la interfaz de usuario, entre otras opciones.

El procedimiento para realizar este restablecimiento por sistema operativo se describe a continuación:

+++Windows
* Cerrar Designer

Cerrar Designer

* Abra la aplicación <b>Command prompt</b>

Abra la aplicación <b>Command prompt</b>

* Escriba el comando siguiente y pulse <b>Intro</b>:

  <b>Escritorio del Creative Cloud</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Steam/Substance edition</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


Escriba el comando siguiente y pulse <b>Intro</b>:

<b>Escritorio del Creative Cloud</b>

<b>Steam/Substance edition</b>

* Desconecte el segundo monitor del sistema y conéctelo de nuevo (omita este paso si *no* tiene varias pantallas adjuntas)

Desconecte el segundo monitor del sistema y conéctelo de nuevo (omita este paso si *no* tiene varias pantallas adjuntas)

* Inicie Designer, pero *no* cree o abra ningún proyecto

Inicie Designer, pero *no* cree o abra ningún proyecto

* En la barra superior, abre el menú <b>Windows</b> y selecciona la opción <b>Nueva vista 3D</b>

En la barra superior, abre el menú <b>Windows</b> y selecciona la opción <b>Nueva vista 3D</b>

* Compruebe que la <b>Vista 3D</b> está inicializada correctamente y pruebe con diferentes mallas de vista previa en el menú <b>Escena</b> de la barra superior del panel

Compruebe que la <b>Vista 3D</b> está inicializada correctamente y pruebe con diferentes mallas de vista previa en el menú <b>Escena</b> de la barra superior del panel

* Crear o abrir un material

Crear o abrir un material

+++

+++macOS
* Cerrar Designer

Cerrar Designer

* Abra la aplicación <b>Terminal</b>

Abra la aplicación <b>Terminal</b>

* Escriba el comando siguiente y pulse <b>Intro</b>:

  <b>Escritorio del Creative Cloud</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Steam/Substance edition</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


Escriba el comando siguiente y pulse <b>Intro</b>:

<b>Escritorio del Creative Cloud</b>

<b>Steam/Substance edition</b>

* Desconecte el segundo monitor del sistema y conéctelo de nuevo (omita este paso si *no* tiene varias pantallas adjuntas)

Desconecte el segundo monitor del sistema y conéctelo de nuevo (omita este paso si *no* tiene varias pantallas adjuntas)

* Inicie Designer, pero *no* cree o abra ningún proyecto

Inicie Designer, pero *no* cree o abra ningún proyecto

* En la barra superior, abre el menú <b>Windows</b> y selecciona la opción <b>Nueva vista 3D</b>

En la barra superior, abre el menú <b>Windows</b> y selecciona la opción <b>Nueva vista 3D</b>

* Compruebe que la <b>Vista 3D</b> está inicializada correctamente y pruebe con diferentes mallas de vista previa en el menú <b>Escena</b> de la barra superior del panel

Compruebe que la <b>Vista 3D</b> está inicializada correctamente y pruebe con diferentes mallas de vista previa en el menú <b>Escena</b> de la barra superior del panel

* Crear o abrir un material

Crear o abrir un material

+++
