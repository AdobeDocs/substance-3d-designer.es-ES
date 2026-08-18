---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Utilice el nodo Material base para crear propiedades de material base para crear materiales basados en la física desde cero.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material de base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# Material de base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## Material de base

**En:** *Utilidades de filtros de materiales/PBR*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

La forma más rápida y sencilla de crear un material multicanal en [Adobe Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html). Este nodo devuelve un paquete de material completo basado en valores y ajustes de color simples y sólidos. A continuación, se puede utilizar como marcador de posición o para refinar en un material complejo.

El nodo es muy útil cuando se texturizan accesorios completos y se mezclan varios materiales. De hecho, puedes iniciar cada material desde este nodo, sin necesidad de una base de materiales compleja.

## Parámetros

### Entradas

* Entradas opcionales para cada canal que se pueden activar con los interruptores en &quot;Entradas definidas por el usuario&quot;.

### Parámetros

* **Flujo de trabajo de PBR**: *Metal - Rugosidad, Specular - Brillo* Define el modelo de PBR utilizado.
* **Ajuste preestablecido de material**: *Personalizado, Dieléctrico, Oro, Plata, Aluminio, Hierro, Cobre, Titanio, Níquel, Cobalto, Platino* Método abreviado rápido para crear ciertos metales. Deshabilita las opciones irrelevantes.
* **Color base**: *(Valor de color)*Color sólido utilizado para el color base.
* **Metálico**: *(Valor de escala de grises)*Valor sólido utilizado para Metálico.
* **Color de difusión**: *(Valor de color)*Color sólido utilizado para Difusión.
* **Specular**: *(Valor de color)*Color sólido utilizado para el Specular.
* **Ajustes preestablecidos de Specular**: *Plástico, Madera, Piedra, Ladrillo, Arena, Hormigón, Tela, Metal oxidado, Agua, Hielo, Vidrio* Ajustes preestablecidos rápidos opcionales para establecer valores de Specular correctos para PBR.
* **Rango de Speculares**: *0.0 - 1.0* Ajusta el rango de Specular.
* **Rugosidad - Brillo**
  * **Valor de rugosidad**: *(Valor de escala de grises)*Establezca el valor de rugosidad base global, si el canal está activo.
  * **Valor de brillo**: *(Valor de escala de grises)*Color sólido utilizado para Brillo, si el canal está activo.
  * **Cantidad de Suciedades**: *0.0 - 1.0* Grado en el que la entrada del mapa de Suciedades opcional se mezcla en Brillo o Rugosidad.
  * **Mosaico de Suciedades**: *1 - 16* Extensión para estructurar el mapa de Suciedades opcional.
  * **Entrada de Suciedad personalizada**: *Falso/Verdadero* Habilita o deshabilita el mapa de Suciedad personalizado opcional.
* **Normal**
  * **Normal a partir de la Intensidad del Height**: *0.0 - 16.0* Convierte opcionalmente el mapa de altura personalizado a normal y lo devuelve como el mapa normal del material.
* **Height**
  * **Posición del Height**: *0.0 - 1.0* Valor sólido utilizado para la salida de Height.
  * **Intervalo de Height**: *0.0 - 1.0* Establece la influencia del mapa de altura definido por el usuario, si está habilitado.
* **Asignaciones definidas por el usuario**
  * Activa o desactiva todas las asignaciones definidas por el usuario y las devuelve en lugar de valores sólidos.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
