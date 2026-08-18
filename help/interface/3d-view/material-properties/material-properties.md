---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/material-properties.html"
breadcrumb-title: ''
description: Configure las propiedades de los materiales en la vista 3D para previsualizar y ajustar el aspecto de los materiales de Substance en los objetos 3D.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Material properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Propiedades de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 29%

---


# Propiedades de material

La [vista 3D](../../../interface/3d-view/3d-view.md) representa la superficie de los modelos mediante un programa llamado *sombreador*. El sombreador define el material
se aplica al modelo mediante una lista de propiedades que afectan a varios aspectos de la apariencia del modelo.

El menú **Materiales** de la vista 3D le permite comprobar qué sombreador se utiliza para cada uno de los materiales de la escena.

<a name="openpbr"></a>

## OpenPBR

Designer utiliza el modelo de material [OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/) de forma predeterminada, que admite varios efectos complejos como anisotropía,
transmisión y fuzz.

Las [plantillas de gráficos](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#graph-templates) predeterminadas y las [muestras de materiales](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#material-samples) incluidas en Designer se basan en el modelo de OpenPBR.

Las propiedades de este sombreador siguen la [referencia de parámetro de OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/#parameterreference) y se *comparten* en el rasterizador,
Trazador de ruta de GPU y OpenGL [procesadores 3D](../3d-renderers/3d-renderers.md).

+++ UV

| Parámetro | Tipo | Predeterminado | Descripción |
|---------------------------------|---------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mosaico | Flotante | 1.0 | La cantidad de repeticiones de textura en una celda UV, donde un valor más alto<br/>produce más repeticiones de textura. |
| Habilitar tamaño físico desde gráfico | Booleano | False | Ajusta automáticamente el mosaico de acuerdo con el [Tamaño físico](../../../compositing-graphs/graph-parameters/graph-parameters.md)<br/> del gráfico para representar el material a la escala adecuada. |
| Escala de UV | Flotante 2 | 1.0, 1.0 | Ajusta la escala del mosaico por un factor distinto para U y V, donde <br/>un valor más alto produce más repeticiones de textura. |

+++

+++ Base

| Parámetro | Tipo | Predeterminado | Descripción |
|-------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 1.0 | Multiplicador sobre la intensidad del reflejo de la base difusa y metálica. |
| Color | Float3 (RGB) | 0.8, 0.8, 0.8 | Color del reflejo de la base difusa y metálica. |
| Metalicidad | Flotante | 0.0 | Especifica el aspecto metálico del material base. (Marca la base de dieléctrico puro a metal puro) |
| Rugosidad difusa | Flotante | 0.0 | Rugosidad del reflejo difuso. Los valores más altos hacen que la superficie aparezca más plana. |

+++

+++ Especular

| Parámetro | Tipo | Predeterminado | Descripción |
|------------|--------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 1.0 | Multiplica la reflectividad especular. |
| Color | Float3 (RGB) | 1.0, 1.0, 1.0 | Color del reflejo del specular. (Controla el matiz de borde físico para metales,<br/> y un matiz global no físico para dieléctricos) |
| Rugosidad | Flotante | 0.3 | La rugosidad del reflejo del specular. Los números más bajos producen reflejos <br/>más nítidos, mientras que los números más altos producen reflejos más borrosos. |
| Anisotropía | Flotante | 0.0 | El sesgo direccional de la rugosidad de la base metal/dieléctrica, que resulta<br/> en iluminaciones cada vez más estiradas a lo largo de la dirección tangente. |
| IOR | Flotante | 1.5 | Índice de refracción de la base dieléctrica. |

+++

+++ Transmisión

| Parámetro | Tipo | Predeterminado | Descripción |
|------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 0.0 | Peso de la mezcla entre la base dieléctrica transparente y opaca.<br/>Cuanto mayor sea el valor, más transparente será el material. |
| Color | Float3 (RGB) | 1.0, 1.0, 1.0 | Controla el color de la base transparente debido a la absorción volumétrica <br/>de la ley de Beer bajo la superficie. |
| Profundidad | Flotante | 0.0 | Especifica la distancia que recorre la luz dentro de la base transparente antes de<br/> que se convierta exactamente en `transmission_color` según la ley de Beer. |
| Dispersión | Float3 (RGB) | 0.0, 0.0, 0.0 | Controla el color de la luz dispersada volumétricamente dentro de la base transparente. |
| Anisotropía | Flotante | 0.0 | Cantidad de sesgo direccional o anisotropía de la dispersión volumétrica <br/> en la base transparente. |
| Escala de dispersión | Flotante | 0.0 | Escala linealmente la cantidad de dispersión. |
| Número Abbe | Flotante | 20.0 | Número Abbe físico del medio dieléctrico, que describe en qué medida<br/>el índice dieléctrico de refracción varía en las longitudes de onda. |

+++

+++ Subsuperficie

| Parámetro | Tipo | Predeterminado | Descripción |
|--------------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 0.0 | Peso de la mezcla que marca la base dieléctrica opaca entre el reflejo difuso y la dispersión subsuperficial.<br/> |
| Color | Float3 (RGB) | 0.8, 0.8, 0.8 | Color de reflejo observado del medio de dispersión subsuperficial. |
| Radio | Flotante | 1.0 | Escala de longitud del recorrido libre medio de la dispersión subsuperficial. |
| Escala de radio | Float3 (RGB) | 1.0, 0.5, 0.25 | RGB el multiplicador a subsurface_radius, que proporciona la dispersión por canal<br/>medias-libres-trazados. |
| Anisotropía | Flotante | 0.0 | Controla la función de fase de la dispersión subsuperficial, donde cero<br/>dispersiones se iluminan uniformemente, valores positivos dispersión hacia adelante y valores <br/>negativos dispersión hacia atrás. |

+++

+++ Capa

| Parámetro | Tipo | Predeterminado | Descripción |
|------------|--------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 0.0 | El peso de presencia de una capa transparente reflectante en la parte superior del material.<br/>Úsalo para materiales como pintura de auto o una capa aceitosa. |
| Color | Float3 (RGB) | 1.0, 1.0, 1.0 | Color de la transparencia de la capa de revestimiento transparente, debido a la absorción en la capa. |
| Rugosidad | Flotante | 0.0 | La rugosidad de los reflejos claros.<br/>Cuanto menor sea el valor, más nítido será el reflejo. |
| Anisotropía | Flotante | 0.0 | El sesgo direccional de la rugosidad de la capa transparente<br/> produce iluminaciones cada vez más estiradas a lo largo de la dirección de la tangente del revestimiento. |
| IOR | Flotante | 1.6 | Índice de refracción de la capa de revestimiento transparente. |
| Oscurecimiento | Flotante | 1.0 | Modula el efecto de oscurecimiento físico de la capa. |

+++

+++ Pelusa

| Parámetro | Tipo | Predeterminado | Descripción |
|-----------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 1.0 | El peso de presencia de una capa de pelusa que se puede usar para aproximar microfibras,<br/>para telas como terciopelo y satén, así como granos de dust. |
| Color | Float3 (RGB) | 1.0, 1.0, 1.0 | Color de la capa de pelusa. |
| Rugosidad | Flotante | 0.5 | Rugosidad de la capa de pelusa. |

+++

+++ Emisión

| Parámetro | Tipo | Predeterminado | Descripción |
|-----------|--------------|---------------|------------------------------------------------------|
| Luminancia | Flotante | 0.0 | Cantidad de luz emitida, como luminancia en nits. |
| Color | Float3 (RGB) | 1.0, 0.0, 0.0 | Color de la luz emitida. |

+++

+++ Película fina

| Parámetro | Tipo | Predeterminado | Descripción |
|-----------|-------|---------|-------------------------------------------------------------------------------------------------------|
| Peso | Flotante | 0.0 | Peso de cobertura de la película delgada.<br/>Utilícelo para materiales como pintura de automóviles multitono o burbujas de jabón. |
| Grosor | Flotante | 0.5 | El thickness de la capa de película fina en la base. (En micrómetros) |
| IOR | Flotante | 1.4 | Índice de refracción de la película fina. |

+++

+++ Geometría

| Parámetro | Tipo | Predeterminado | Descripción |
|-------------------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opacidad | Flotante | 1.0 | Opacidad de todo el material. |
| Con paredes finas | Booleano | False | Si es verdadero, la superficie es de doble cara y representa una carcasa infinitesimalmente delgada.<br/>Adecuado para objetos geométricamente muy finos, como hojas o papel. |
| Normal | Float3 (RGB) | 0.5, 0.5, 1.0 | Entrada normal geométrica para la superficie. |
| Tangente | Float3 (RGB) | 1.0, 0.5, 0.0 | Tangente geométrica de entrada. |
| Capa normal | Float3 (RGB) | 0.5, 0.5, 1.0 | Entrada normal para capa de revestimiento. |
| Tangente de capa | Float3 (RGB) | 1.0, 0.5, 0.0 | Tangente geométrica de entrada para capa de revestimiento. |
| Altura | Flotante | 0.5 | Desplazamiento (o relieve) en la dirección de la normal.<br/>Cuando el height es igual al nivel de height, no hay desplazamiento.El Desplazamiento <br/>es un cambio escalar en la posición de la superficie hacia una superficie normal sin perturbaciones<br/>mezclada.<br/>En los casos en que no sea posible o no se desee utilizar el desplazamiento teselado,<br/>el height se puede implementar como un mapa de relieve. |
| Nivel de altura | Flotante | 0.5 | Valor de height correspondiente a sin desplazamiento (valor de nivel cero).<br/>El nivel de Height desplaza (pero no escala ni voltea) el desplazamiento relativo<br/> a la superficie del objeto no desplazado.<br/>Si el nivel de height es 0, todo el desplazamiento está por encima.<br/>Si el nivel de height es 1, todo el desplazamiento está por debajo de la superficie, pero conserva<br/> la misma escala y dirección. |
| Escala de altura | Flotante | 1.0 | Escala de desplazamiento o relieve en las unidades de espacio de escena.<br/>La magnitud y la dirección de la escala son independientes del valor del nivel de height. |
| Oclusión ambiental | Flotante | 1.0 | Mapa de oclusión ambiental para oscurecer áreas ocluidas.<br/>Blanco (1.0) significa completamente iluminado, negro (0.0) significa completamente ocluido. |

+++

### Compatibilidad con gráficos existentes

Algunas de las propiedades de materiales de OpenPBR tienen identificadores de uso diferentes en comparación con otros modelos incluidos en Designer.
Designer hace coincidir automáticamente algunos identificadores para garantizar la compatibilidad con OpenPBR como modelo predeterminado.

+++ Asignaciones de uso de heredado a OpenPBR

| Heredada | OpenPBR |
|-------------------------|-----------------------------|
| metálico | metalidad |
| specularEdgeColor | specularColor |
| rugosidad | Rugosidad especular |
| anisotropíaNivel | specularRoughnessAnisotropy |
| IOR | specularIOR |
| absorptionColor | transmisiónColor |
| absorptionDistance | transmisiónProfundidad |
| translucidez | subsurfaceWeight |
| scatteringColor | subsurfaceColor |
| distanciaDeDispersión | subsurfaceRadius |
| scatteringDistanceScale | subsurfaceRadiusScale |
| coatOpacity | coatWeight |
| brilloOpacidad | fuzzWeight |
| sheenColor | fuzzColor |
| brilloRugosidad | fuzzRoughness |
| emisivo | issueColor |

+++

### Lectura posterior

Para obtener más información sobre el OpenPBR, aquí tiene algunos recursos:

* [artículo del blog de Adobe](https://blog.adobe.com/en/publish/2023/08/08/openpbr-strengthens-interoperability-enabling-enhanced-creativity)
* [Documentación técnica](https://academysoftwarefoundation.github.io/OpenPBR/)
* [OpenPBR BSDF de Adobe en GitHub](https://github.com/adobe/openpbr-bsdf)
* [Designer 16.0: Apoyo de OpenPBR](../../../release-notes/version-16-0/version-16-0.md#openpbr-support)

<a name="adobe-standard-material"></a>

## Adobe Standard Material

El modelo Adobe Standard Material (ASM) se introdujo en Designer 11.2 y ha sido el sombreador predeterminado de Designer
hasta la versión 15.1.

Aunque Designer se ha trasladado a OpenPBR como su nuevo modelo predeterminado, ASM se sigue incluyendo y sus propiedades también se comparten
a través de Rasterizer, Trazador de ruta de GPU y OpenGL [procesadores 3D](../3d-renderers/3d-renderers.md).

El modelo está documentado [aquí](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/asm/adobe-standard-material).

<a name="usdpreviewsurface"></a>

## UsdPreviewSurface

La finalidad del modelo UsdPreviewSurface es previsualizar materiales con un conjunto de funciones básicas que promuevan la compatibilidad
en renderizadores que incluyen USD y/o Hydra.

En Designer, este modelo de material solo es compatible con los procesadores Rasterizer y Trazador de ruta de GPU [3D](../3d-renderers/3d-renderers.md).

El modelo está documentado [aquí](https://openusd.org/dev/spec_usdpreviewsurface.html).
