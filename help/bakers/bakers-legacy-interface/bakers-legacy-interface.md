---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Obtenga más información sobre la interfaz heredada de los panaderos de Substance 3D Designer para usuarios familiarizados con las versiones anteriores.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interfaz heredada de Bakers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 3%

---


# Interfaz heredada de Bakers

Esta es la descripción de la interfaz baker disponible en las versiones de [Adobe Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) anteriores a la 6.0.4.

## Información general

![](../../assets/image2017-3-13-9-33-40.png)

El panel panadero se divide en 4 partes:

### 1: Escena

![](../../assets/image2017-3-13-9-35-53.png)

Permite definir qué parte de la malla participa en el proceso de cocción.

Nuevo en la versión 6, también puede seleccionar por material:

![](../../assets/image2017-3-13-9-45-26.png)

### 2: Panaderos

![](../../assets/image2017-3-13-9-46-26.png)

Pulsando el botón ![](../../assets/image2017-3-13-9-47-47.png), puede agregar los panaderos deseados a la lista de procesamiento

>[!NOTE]
>
> Las panificaciones se procesan siguiendo el orden de la lista (de arriba abajo): esto puede ser importante si desea reutilizar el resultado de una cocción (como el mapa normal) en otro proceso de cocción

Al hacer clic en el signo &quot;+&quot; en el diseño de los panaderos, puede añadir los panaderos en una pila (puede colocar tantos panaderos como desee en una pila).

.![](../../assets/image2017-3-13-9-52-8.png)

Puede quitar un proceso de procesamiento de la lista presionando ![](../../assets/image2017-3-13-9-54-33.png)

Puede reordenar la lista de procesos bancarios seleccionando un proceso bancario y usando ![](../../assets/image2017-3-13-9-55-33.png)

### 3: Parámetros de panaderos

![](../../assets/image2017-3-13-13-24-0.png)

En esta sección se muestran las opciones específicas para el panadero seleccionado actualmente.

### 4: Parámetros comunes

![](../../assets/image2017-3-13-13-28-12.png)

Muestra los parámetros que se comparten entre panaderos.

>[!NOTE]
>
> De forma predeterminada, cambiar uno de estos parámetros; afectará a todos los panaderos, excepto si marca Ignorar parámetros, común a todos los panaderos: en ese caso, los cambios serán locales para el panadero actual.

* **El campo Nombre del recurso** le permite cambiar el nombre del mapa de bits generado, si lo desea.
* **La lista desplegable Formato de archivo** le permite cambiar el formato de archivo predeterminado (formato de mapa de bits de Windows u OS/2, &quot;BMP&quot;).
* **La casilla de verificación** **Colocar** recurso en una carpeta específica de malla le permite elegir si el mapa de bits generado se almacena en el mismo nivel que el modelo o dentro de una nueva subcarpeta denominada &quot;Resources&quot;.
* **El método** le permite definir si el nuevo recurso de mapa de bits debe vincularse o incrustarse en el paquete de Substance.
* **La carpeta** le permite definir dónde guardar los mapas.

Pulsando el botón OK en la parte inferior derecha de la ventana de panadería se iniciará el proceso de panadería.

Novedad en la versión 6: ahora puede cancelar el proceso de procesamiento con el botón cancelar:

![](../../assets/image2017-3-13-13-50-4.png)
