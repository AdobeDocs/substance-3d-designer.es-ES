---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Bitmap para luz de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## Bitmap para luz de material

**En:** *Filtros De Materiales/1 Clic*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo convierte una sola entrada Diffuse/Basecolor en un material completo. Como la versión simple y &quot;ligera&quot; de [Allegorithmic&#39;s fully fledged Bitmap2Material, que se puede comprar por separado](https://www.allegorithmic.com/products/bitmap2material), te da una idea de la versión completa. Puede funcionar bien para casos más sencillos.

Aunque no se garantiza que dé como resultado materiales perfectos y correctos para la PBR, es una forma buena y rápida de empezar si solo tienes una imagen y quieres un material completo.

## Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Global**
  * **Saldo de Profundidad**: *-1.0 - 1.0* Establece un sesgo/cambio para el mapa de altura.
* **Difusión**
  * **Perfilar**: *0.0 - 1.0* Agrega enfoque al resultado de difusión.
  * **Tono**: *0.0 - 1.0* Los matices se difuminan con un cambio de tono seleccionado por el usuario.
  * **Saturación**: *0.0 - 1.0* Modifica la saturación del resultado de difusión.
  * **Brillo**: *0.0 - 1.0* Ajusta el brillo del resultado de difusión.
  * **Contraste**: *-1.0 - 1.0*\
    Ajusta el contraste del resultado.
* **Relieve**\
  El grupo Relieve controla las salidas Normal y Height.
  * **Formato Normal De Salida**: *DirectX, OpenGL* Cambia entre los formatos Normal (voltea el verde).
  * **Invertir Relieve generado**: *Falso/Verdadero* Invierte la interpretación del height.
  * **Intensidad normal**: *0.0 - 20.0* Establece la intensidad del mapa normal generado.
  * **Ecualizador de Relieve**: *0.0 - 1.0* Establece saldos de conversión para escalas de detalle diferentes.
  * **Intensidad De Pellizque**: *0.0 - 1.0* Hace que las transiciones normales sean más nítidas. Añade de forma efectiva un filtro de enfoque antes de convertir a normal, lo que hace que los bordes sean más pronunciados.
  * **Enfoque normal**: *0.0 - 1.0* Enfoca el mapa normal después de la conversión y resalta los detalles.
  * **Suavizado normal**: *0.0 - 1.0* Suaviza el mapa normal después de la conversión y oculta los detalles.
* **Specular**
  * **Influencia De Difusión De Specular**: *0.0 - 1.0* Establece la influencia de la difusión en el Specular. Afecta también a las salidas de brillo y rugosidad.
  * **Saturación del Specular**: *0.0 - 1.0* Cambia la saturación de la salida del Specular.
  * **Enfoque de Specular**: *0.0 - 1.0* Enfoca la salida del Specular.
  * **Speculares leveles En**: *0.0 - 1.0* Define los niveles de entrada para la interpretación del Specular.
  * **Salida de Speculares leveles**: *0.0 - 1.0* Modifica los niveles de salida del Specular.
  * **Influencia De Speculares Metálicos**: *0.0 - 1.0* Determina la influencia de la entrada metálica opcional en el mapa de Speculares.
* **Brillo**
  * **Niveles De Brillo En**: *0.0 - 1.0* Define los niveles de entrada para la interpretación de Brillo.
  * **Salida de niveles de brillo**: *0.0 - 1.0* Modifica los niveles de salida de Brillo.
  * **Influencia de brillo metálico**: *0.0 - 1.0* Determina la influencia de la entrada metálica opcional en el mapa de brillo.
* **Rugosidad**
  * **Niveles De Rugosidad En**: *0.0 - 1.0* Define los niveles de entrada para la interpretación de Rugosidad.
  * **Salida de niveles de rugosidad**: *0.0 - 1.0* Modifica los niveles de salida de Rugosidad.
  * **Influencia De Rugosidad Metálica**: *0.0 - 1.0* Determina la influencia de la entrada metálica opcional en el mapa de brillo.
* **Oclusión de ambiente**
  * **Oclusión De Ambiente En Difusión**: *0.0 - 1.0* Fusiona el AO generado en la salida de difusión.
  * **Extensión de Oclusión ambiental**: *0.0 - 1.0* Establece hasta dónde se extiende el AO generado.
  * **Distancia de luz de la Oclusión ambiente**: *0.0 - 1.0* Define la interpretación de &quot;profundidad&quot; de AO. Tiene menos influencia cuando hay un pliego grande.
  * **Ángulo de luz de la Oclusión ambiente**: *0.0 - 1.0* Establece un ángulo de proyección de AO de iluminación falsa. Se puede utilizar para compensar cualquier AO direccional que ya esté en la difusión, si se define en un ángulo opuesto.
  * **Niveles De Oclusión Ambiental**: *0.0 - 1.0* Modifica los niveles de salida de AO.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
