---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: Solucione los problemas que impiden que Substance 3D Designer se inicie y busque soluciones para iniciar la aplicación.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La aplicación no se inicia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 734525cdd187aac666168f8a9e1f9e49f3dad03e
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---


# La aplicación no se inicia

En esta página se enumeran las causas comunes por las que Substance 3D Designer no se inicia correctamente y se ofrecen pasos de solución de problemas para cada una de ellas, agrupadas por sistema operativo:

[Designer 15.0 y superior](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## Designer 15.0 y superior

<b>![(error)](application-does-not-start.resources/error.svg) Problema</b>

Las versiones 15.0 y superiores de Designer no se inician en sistemas con una GPU integrada (iGPU) y una GPU independiente (dGPU).

<b>![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados</b>

Actualice los controladores gráficos de la GPU. Puede encontrar los últimos controladores aquí:  [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![(error)](application-does-not-start.resources/error.svg) Problema**

Substance 3D Designer no se inicia en sistemas que usan Windows 10 o Windows 11.

**![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados**

Es posible que las versiones anteriores de Designer no se inicien en Windows 10 o Windows 11 debido a una biblioteca *obsoleta* `libeay32.dll` utilizada en el proceso de validación de licencias.

Puedes intentar reemplazar la biblioteca por una *versión actualizada*, como la que se distribuye [aquí](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows) (selecciona el archivo para Windows de 32 bits), siguiendo estos pasos:

1. Busque el archivo `libeay32.dll` en el directorio de instalación de Designer
1. Haga una copia de seguridad del archivo en una ubicación segura si necesita restaurarlo en el futuro
1. Reemplazar el archivo por la versión actualizada
1. Iniciar Designer

>[!WARNING]
>
> Configuraciones no compatibles
> 
> Windows 10 no es compatible. Puede obtener más información en la página [Requisitos del sistema](../../getting-started/system-requirements/system-requirements.md).
> 
> Las versiones de Designer que no estén dentro de su período de mantenimiento no son compatibles. Es posible que estas versiones ya no se ejecuten de forma fiable si se realizan cambios importantes en el sistema, como actualizaciones del sistema operativo.

## Windows 7/8/8.1

**![(error)](application-does-not-start.resources/error.svg) Problema**

Substance 3D Designer no se inicia en sistemas que utilizan Windows 7, Windows 8 o Windows 8.1.

**![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados**

Como parte de la actualización de la versión **11.3.0**, actualizamos varias bibliotecas, herramientas y SDK que *rompieron la compatibilidad* con versiones de Windows anteriores a Windows 10.

*Recomendamos encarecidamente* actualizar a Windows 10, ya que el propio Microsoft ya no admite versiones anteriores de Windows para uso general (consulta [aquí](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information) y [aquí](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)). Por lo tanto, el uso continuado de estas versiones presenta un *problema de seguridad*.\
Si no es posible actualizar a Windows 10, *no actualice* su instalación de Designer *versión anterior* **11.2.2**.

>[!WARNING]
>
> Configuraciones no compatibles
> 
> Tenga en cuenta que Windows 7, Windows 8 y Windows 8.1 *no son compatibles oficialmente*. Puede obtener más información en la página [Requisitos del sistema](../../getting-started/system-requirements/system-requirements.md).

## Linux

<b>![(error)](application-does-not-start.resources/error.svg) Problema</b>

Bloqueo al cerrar la pantalla Inicio y mostrar la ventana principal.

<b>![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados</b>

Designer no puede cargar los componentes de Python porque carga la biblioteca <b>libffi.so</b> del sistema en lugar de la suya propia.

Para asegurarse de que Designer carga su propia biblioteca, use este comando en el directorio de instalación de Designer, reemplazando `%command%` con su comando para ejecutar Designer:

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


Tenga en cuenta que el número de versión de Python depende de la versión de Designer que se ejecute:

* Inferior a 14.0.0: python3.9
* Inferior a 12.1.0: python3.7

+++Opciones de inicio de Steam
Los usuarios de Linux que inicien Designer desde Steam pueden configurar el comando LD\_PRELOAD en las opciones de inicio de Designer, como se muestra a continuación.

Una vez hecho esto, es posible que Designer se inicie desde Steam normalmente para todas las sesiones futuras.

![Opciones de inicio de Steam](application-does-not-start.resources/steam_linux_launch_option.jpg "Opciones de inicio de Steam")



+++

**![(error)](application-does-not-start.resources/error.svg) Problema**

La edición de Steam de Designer no se inicia y no genera ningún mensaje de error.

**![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados**

Puede obtener mensajes de error si registra la aplicación Steam en su lugar.

Como se recomienda [aquí](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260), cierre completamente Steam y ejecute el siguiente comando desde un terminal (o cree un método abreviado para este comando):

```
steam 2>&1 | tee /path/to/logfile
```


<b>![(error)](application-does-not-start.resources/error.svg) Problema</b><b>e</b>

No se puede cargar el complemento `<b>xcb</b>`. El siguiente mensaje se muestra en la línea de comandos:

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados**

Faltan algunos paquetes necesarios. Ejecute el siguiente comando desde el directorio de instalación de Designer :

```
ldd libQt5XcbQpa.so.5
```


Compruebe la lista impresa de los paquetes notificados como `not found` y, a continuación, ejecute el siguiente comando para cada uno de los paquetes que faltan:

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![(error)](application-does-not-start.resources/error.svg) Problema</b>

Este error se produce al iniciar Designer:

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Una biblioteca del sistema cargada por Designer no es compatible con la biblioteca <b>libcrypto.so.1.1</b> propia de Designer.

<b>![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados</b>

Quite la biblioteca <b>`libcrypto.so.1.1`</b> del directorio de instalación de Designer, de modo que se utilice en su lugar la biblioteca del sistema.

>[!NOTE]
>
> Esta solución alternativa solo funciona cuando el sistema tiene su propia biblioteca libcrypto.so.1. En distribuciones recientes, puede ser necesario instalar un paquete de compatibilidad como <b>libxcrypt-compat</b>.

<b>![(error)](application-does-not-start.resources/error.svg) Problema</b>

Substance 3D Designer no se inicia en sistemas que usan distribuciones de Linux *basadas en Arch*.

**![(marca)](application-does-not-start.resources/check.svg) Pasos recomendados *(![(advertencia)](application-does-not-start.resources/warning.svg) Inestable, solo GPU AMD)***

Intente instalar **progl** (parte de los controladores [AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO)) e inicie Designer a través de él. Puede hacer esto usando el prefijo `progl` en el comando de inicio de la aplicación:

```
progl <designer-application-path>
```


Ten en cuenta que `progl` puede ser inestable. Por lo tanto, se debe intentar *como último recurso*.

>[!WARNING]
>
> Tenga en cuenta que las distribuciones basadas en Arch de Linux *no son compatibles*. Puede obtener más información en la página [Requisitos del sistema](../../getting-started/system-requirements/system-requirements.md).
