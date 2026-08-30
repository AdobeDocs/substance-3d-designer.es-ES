---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/color-management/spot-colors-pantone.html"
breadcrumb-title: ''
description: Aprenda a utilizar las tintas planas de Pantone en Substance 3D Designer para conseguir una coincidencia de color precisa en los flujos de trabajo de impresión y diseño.
helpx_creative_field: ""
helpx_description: Designer > Color Management > Spot Colors (Pantone)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tintas planas (Pantone)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# Tintas planas (Pantone)

Las tintas planas son un modo alternativo para elegir colores. En lugar del RGB estándar o el selector de color HSV, Substance 3D Designer le permite elegir colores de Libros de color, ajustándose a los sistemas de gestión y reproducción de color existentes. Esto le permite garantizar que los colores digitales utilizados en Designer coinciden con los de los productos fabricados.

Actualmente Spot Colors ofrece diecisiete libros de Pantone.

## Gestión de colores

Dado que las tintas planas están diseñadas para una reproducción y coincidencia de color precisas, es esencial que configures la[gestión de color](../../color-management/color-management.md) para Designer antes de empezar a trabajar. Las tintas planas funcionan mejor con la administración de color de <b>Adobe Color Engine (ACE)</b>, no con OCIO. Funcionarán en modo heredado, pero no puede estar seguro de que se muestren correctamente si el monitor no está calibrado para sRGB.

En resumen, la configuración de la gestión de color para tintas planas implica lo siguiente:

* Calibrar el monitor generando u obteniendo el perfil ICC adecuado.
* Active la gestión de color con Adobe Color Engine (ACE) en las preferencias de Designer.
* Configure la vista 2D y 3D para utilizar el perfil adecuado de su monitor.
* Reinicie para que los cambios surtan efecto.
* Verificar la coincidencia de color entre Designer y otra aplicación de Adobe como Adobe Illustrator o Photoshop. El color &quot;<b>Pantone Rhodamine Red C</b>&quot; del primer libro de Pantone, Solid Coated, es un buen caso de prueba, ya que puede variar significativamente si la gestión de color no es correcta.

>[!WARNING]
>
> **Colores de miniatura**
> 
> Las miniaturas de nodo *no tienen administración de color predeterminada*, por lo que solo se confía en la visualización de color en la vista 2D con el perfil correcto. La gestión de color de miniatura se puede activar en las preferencias de la gestión de color del proyecto, pero tiene un ligero coste de rendimiento.

## Uso de tintas planas

### Cambiar a tinta plana desde RGB

Incluso si configura la gestión de color, los selectores de color seguirán teniendo como valor predeterminado los selectores de color RGB o HSV. Debe cambiarlos a tintas planas manualmente. Este ajuste se almacena por parámetro e incluso se prolonga al exponer un parámetro.

1. Haga clic en el botón ![](spot-colors-pantone.resources/image2021-1-25-9-40-40.png) <b>Tipo de selector de color</b> situado junto a la muestra de color del RGB.
1. En lugar de <b>colores de RGB</b>, elige cualquier <b>libro de colores</b> de la lista desplegable.
1. El icono del ![](spot-colors-pantone.resources/image2021-1-25-9-40-25.png) <b>tipo de selector de color</b> cambia y su interfaz cambia al modo <b>Mancha de color</b>.

![Cambiar al modo de tinta plana](spot-colors-pantone.resources/spot-switch.gif "Cambiar al modo de tinta plana"){width="512px"}

### Selección y búsqueda de tintas planas

Hay varias formas de buscar y elegir tintas planas en un libro de colores.

* Puedes usar las ![](spot-colors-pantone.resources/image2021-1-25-10-40-28.png) ![](spot-colors-pantone.resources/image2021-1-25-10-40-53.png) <b>flechas izquierda y derecha</b> a cada lado de las páginas del libro para cambiar de página. También puede hacer clic y arrastrar en la presentación de la página para desplazarse por las páginas.
* Puede hacer clic en cualquier color de la página actual para seleccionarlo. A menudo, hay más colores disponibles y es necesario desplazarse un poco hacia abajo.
* Puede utilizar la barra de búsqueda para buscar colores por nombre o número. Esta búsqueda solo coincide con los nombres de los colores del libro, no hay una lógica compleja; buscar &quot;gris&quot; solo producirá resultados con la palabra &quot;gris&quot; en su nombre, no verá ningún color gris que solo tenga números en su nombre.
* Para obtener una interfaz más grande y fácil de usar para el libro de colores, haz clic en el cuadro de vista previa de color entre el icono ![](spot-colors-pantone.resources/image2021-1-25-10-39-18.png) <b>Cuentagotas</b> y la ![](spot-colors-pantone.resources/image2021-1-25-10-40-28.png) <b>flecha izquierda</b>.

![Examinar tintas planas](spot-colors-pantone.resources/spot-choose.gif "Examinar tintas planas"){width="512px"}

### Selección y conversión de colores planos

Las tintas planas se pueden seleccionar con la herramienta ![](spot-colors-pantone.resources/image2021-1-25-10-39-18.png) <b>Cuentagotas</b>. En el modo de tinta plana, el color del RGB muestreado se convertirá a la tinta plana que más se asemeje del libro seleccionado.

La herramienta <b>Cuentagotas</b> de Designer se puede usar en cualquier parte de la pantalla sin limitaciones, por lo que puedes usar Designer como herramienta de conversión de tinta plana,

Si cambia Libros o incluso vuelve a cambiar a RGB desde un libro de tintas planas, el color actual se convertirá en la coincidencia más cercana. Esto significa que puede convertir los colores entre libros y volver a RGB.

>[!WARNING]
>
> La conversión de tintas planas entre libros es una operación con pérdidas. Hacer una conversión de ida y vuelta a menudo no llevará al mismo color que el que comenzó con!

![Selección y conversión de tintas planas](spot-colors-pantone.resources/spot-pick.gif "Selección y conversión de tintas planas"){width="512px"}
