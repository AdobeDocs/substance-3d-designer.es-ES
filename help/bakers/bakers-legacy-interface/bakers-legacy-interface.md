---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Obtenga más información sobre la interfaz heredada de Substance 3D Designer baker para usuarios familiarizados con las versiones anteriores.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interfaz heredada de Baker
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 4%

---


# Interfaz heredada de Baker

Esta es la descripción de la interfaz de baker disponible en [Adobe Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) versiones anteriores a la 6.0.4.

## Información general

![](bakers-legacy-interface.resources/image2017-3-13-9-33-40.png)

El panel baker se divide en 4 partes:

### 1: Escena

![](bakers-legacy-interface.resources/image2017-3-13-9-35-53.png)

Permite definir qué parte de la malla está implicada en el proceso de hacer un bake.

Nuevo en la versión 6, también puede seleccionar por material:

![](bakers-legacy-interface.resources/image2017-3-13-9-45-26.png)

### 2: Bakeres

![](bakers-legacy-interface.resources/image2017-3-13-9-46-26.png)

Pulsando el botón ![](bakers-legacy-interface.resources/image2017-3-13-9-47-47.png), puede agregar los bakeres deseados a la lista de procesamiento

>[!NOTE]
>
> Las panificaciones se procesan siguiendo el orden de la lista (de arriba abajo): esto puede ser importante si desea reutilizar el resultado de una hace un bake (como el mapa de normales) en otro proceso de hace un bake

Al hacer clic en el signo &quot;+&quot; en el diseño de bakeres, puede añadir los bakeres en una pila (puede colocar tantos bakeres como desee en una pila).

.![](bakers-legacy-interface.resources/image2017-3-13-9-52-8.png)

Puede quitar un proceso de hacer un bake de la lista presionando ![](bakers-legacy-interface.resources/image2017-3-13-9-54-33.png)

Puede reordenar la lista de procesos de hacer un bake seleccionando un proceso de hacer un bake y utilizando ![](bakers-legacy-interface.resources/image2017-3-13-9-55-33.png)

### 3: Parámetros de bakeres

![](bakers-legacy-interface.resources/image2017-3-13-13-24-0.png)

Esta sección muestra las opciones específicas del baker seleccionado actualmente.

### 4: Parámetros comunes

![](bakers-legacy-interface.resources/image2017-3-13-13-28-12.png)

Muestra los parámetros compartidos entre bakeres.

>[!NOTE]
>
> De forma predeterminada, cambiar uno de estos parámetros; afectará a todos los bakeres, excepto si marca la casilla Sustituir parámetros, común a todos los bakeres: en ese caso, los cambios serán locales para el baker actual.

* **El campo Nombre del recurso** le permite cambiar el nombre del mapa de bits generado, si lo desea.
* **La lista desplegable Formato de archivo** le permite cambiar el formato de archivo predeterminado (formato de mapa de bits de Windows u OS/2, &quot;BMP&quot;).
* **La casilla de verificación** **Colocar** recurso en una carpeta específica de malla le permite elegir si el mapa de bits generado se almacena en el mismo nivel que el modelo o dentro de una nueva subcarpeta denominada &quot;Resources&quot;.
* **El método** le permite definir si el nuevo recurso de mapa de bits debe vincularse o incrustarse en el paquete de Substance.
* **La carpeta** le permite definir dónde guardar los mapas.

Al pulsar el botón Aceptar en la parte inferior derecha de la ventana bakeres, se iniciará el proceso de hace un bake.

Novedad en la versión 6: ahora puede cancelar el proceso de hacer un bake con el botón cancelar:

![](bakers-legacy-interface.resources/image2017-3-13-13-50-4.png)
