---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: Utilice el nodo Mapa de bits a luz de material para convertir rápidamente imágenes de mapa de bits en materiales con iluminación optimizada para flujos de trabajo rápidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap para luz de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# Bitmap para luz de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bitmap-to-material-light.resources/b2m-light.png)

<b>En:</b> Filtros de material > 1-Clic

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo convierte una sola entrada Diffuse/Basecolor en un material completo. Como la versión simple y &quot;ligera&quot; de [Allegorithmic&#39;s fully fledged Bitmap2Material, que se puede comprar por separado](https://www.allegorithmic.com/products/bitmap2material), te da una idea de la versión completa. Puede funcionar bien para casos más sencillos.

Aunque no se garantiza que dé como resultado materiales perfectos y correctos para la PBR, es una forma buena y rápida de empezar si solo tienes una imagen y quieres un material completo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Global</b> |  |
| <b>Saldo de Profundidad</b> <i>-1.0 - 1.0</i> | Define un sesgo/desplazamiento para el mapa de altura. |
| <b>Difusión</b> |  |
| <b>Perfilar</b> <i>0.0 - 1.0</i> | Añade enfoque al resultado de difusión. |
| <b>Tono</b> <i>0.0 - 1.0</i> | Los Matices se difuminan con un cambio de tono seleccionado por el usuario. |
| <b>Saturación</b> <i>0.0 - 1.0</i> | Modifica la saturación del resultado de la Difuso. |
| <b>Brillo</b> <i>0.0 - 1.0</i> | Ajusta el brillo del resultado de Difuso. |
| <b>Contraste</b> <i>-1.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Relieve</b> | El grupo Relieve controla las salidas Normal y Height. |
| <b>Formato Normal De Salida</b> <i>DirectX, OpenGL</i> | Cambia entre los formatos Normal (voltea el verde). |
| <b>Invertir Relieve generado</b> <i>Falso/Verdadero</i> | Invierte la interpretación del height. |
| <b>Intensidad normal</b> <i>0.0 - 20.0</i> | Establece la intensidad del mapa normal generado. |
| <b>Ecualizador de Relieve</b> <i>0.0 - 1.0</i> | Define los saldos de conversión para diferentes escalas de detalle. |
| <b>Intensidad De Pellizque</b> <i>0.0 - 1.0</i> | Mejora el enfoque de las transiciones normales. Añade de forma efectiva un filtro de enfoque antes de convertir a normal, lo que hace que los bordes sean más pronunciados. |
| <b>Enfoque normal</b> <i>0.0 - 1.0</i> | Enfoca el mapa normal después de la conversión, resalta los detalles. |
| <b>Suavizar normal</b> <i>0.0 - 1.0</i> | Suaviza el mapa normal después de la conversión y oculta los detalles. |
| <b>Specular</b> |  |
| <b>Influencia del Difuso de Specular</b> <i>0.0 - 1.0</i> | Establece la influencia de la difusión en el Specular. Afecta también a las salidas de brillo y rugosidad. |
| <b>Saturación del Specular</b> <i>0.0 - 1.0</i> | Cambia la saturación de la salida del Specular. |
| <b>Enfoque de Specular</b> <i>0.0 - 1.0</i> | Enfoca la salida de Specular. |
| <b>Speculares leveles En</b> <i>0.0 - 1.0</i> | Define los niveles de entrada para la interpretación del Specular. |
| <b>Salida de Speculares leveles</b> <i>0.0 - 1.0</i> | Modifica los niveles de salida del Specular. |
| <b>Influencia de Speculares metálicos</b> <i>0.0 - 1.0</i> | Determina la influencia de la entrada metálica opcional en el mapa del Specular. |
| <b>Brillo</b> |  |
| <b>Niveles De Brillo En</b> <i>0.0 - 1.0</i> | Define los niveles de entrada para la interpretación del Brillo. |
| <b>Salida de niveles de Brillo</b> <i>0.0 - 1.0</i> | Modifica los niveles de salida del Brillo. |
| <b>Influencia de Brillo metálico</b> <i>0.0 - 1.0</i> | Determina la influencia de la entrada metálica opcional en el mapa de Brillo. |
| <b>Rugosidad</b> |  |
| <b>Niveles De Rugosidad En</b> <i>0.0 - 1.0</i> | Define los niveles de entrada para la interpretación de Rugosidad. |
| <b>Salida de niveles de rugosidad</b> <i>0.0 - 1.0</i> | Modifica los niveles de salida de Rugosidad. |
| <b>Influencia de Rugosidad metálica</b> <i>0.0 - 1.0</i> | Determina la influencia de la entrada metálica opcional en el mapa de Brillo. |
| <b>Oclusión de ambiente</b> |  |
| <b>Oclusión ambiental En El Difuso</b> <i>0.0 - 1.0</i> | Fusiones en el AO generado en la salida de Difuso. |
| <b>Difusión de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define el grado de propagación del AO generado. |
| <b>Distancia de luz de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define la interpretación de &quot;profundidad&quot; de AO. Tiene menos influencia cuando hay un pliego grande. |
| <b>Ángulo claro de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define el ángulo de proyección de iluminación falsa AO. Se puede utilizar para compensar cualquier AO direccional que ya esté en la difusión, si se define en un ángulo opuesto. |
| <b>Niveles de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Modifica los niveles de salida de AO. |
