---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: Aplique efectos de posprocesamiento a la cámara de vista 3D para mejorar la previsualización y visualización de materiales.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Efectos de posprocesamiento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Efectos de posprocesamiento

![Efectos de posprocesamiento](../../../../assets/postEffects.png "Efectos de posprocesamiento"){zoomable="yes"}

En las propiedades de la cámara, puede activar efectos de posprocesamiento para mejorar los renderizados o comprobar propiedades específicas del material.

Estos efectos se desarrollan internamente y solo están disponibles para los procesadores Rasterizer y de Trazador de ruta de GPU [renderers](../../../../interface/3d-view/3d-renderers/3d-renderers.md).

Cualquier efecto de publicación habilitado al guardar [recursos de escena 3D](../../../../resources/3d-scene-resource/3d-scene-resource.md) o [archivos de estado de escena](../../../../working-with-3d-scenes/working-with-3d-scenes.md) se guardará como parte del estado de escena.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Asignación de tonos

</td>
<td style="border: 0;" valign="top">

### Resplandor

</td>
<td style="border: 0;" valign="top">

### Profundidad de campo

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Asignación de tonos

Reasigna los colores del procesamiento según algoritmos específicos o tablas de búsqueda (LUT).

Esto permite mejorar la coherencia de color entre aplicaciones. Por ejemplo, el mapeador de tonos AgX también está disponible en Blender.

+++Reinhard


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++Registro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Neutral Pbr


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisdisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Resplandor

Simula el efecto en la cámara de halos de luz que sangran hacia fuera desde áreas muy brillantes a áreas que reciben menos luz.

El efecto se ve influenciado por la iluminación de la escena, la exposición de la cámara y los materiales emisores.

+++Umbral
El valor de luminancia por encima del cual la floración debe ser visible.

*Izquierda: 1.0 / Derecha: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Difuminación
La rampa de atenuación de la floración, donde un valor más bajo da como resultado un radio de floración más corto.

*Izquierda: 1.0 / Derecha: 0,6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Nivel
La intensidad de la floración. Un valor más alto da como resultado unos halos de luz más brillantes y pronunciados.

*Izquierda: 8.0 / Derecha: 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++Cambio de color
Desplaza el tono de las áreas afectadas por la floración hacia colores más cálidos.

*Izquierda: 0,0 / Derecha: 0,8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## Profundidad de campo

Simula el fenómeno óptico causado por los objetivos de la cámara en el que los objetos más cercanos y más lejanos a la distancia de enfoque se desenfocan.

El efecto se ve afectado por los parámetros &quot;F-Stop&quot; y &quot;Distancia de enfoque&quot; de la cámara.

>[!TIP]
>
> Para ajustar rápidamente el enfoque de la cámara, coloque el cursor en la ubicación de la escena que desea enfocar y presione Ctrl+LMB (Windows) o Cmd+LMB (macOS) para establecer automáticamente la distancia de enfoque a esa ubicación.

+++Radio máximo
Radio máximo del efecto de desenfoque.

*Izquierda: 32.0 / Derecha: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Intensidad de la composición
Magnitud del efecto de desenfoque desde la distancia de enfoque hacia fuera.

*Izquierda: 0.2 / Derecha: 0,05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Aberración longitudinal
Intensidad de la aberración que se produce lejos de la distancia de enfoque.

La aberración simula el modo en que las diferentes longitudes de onda de la luz tienen distancias focales ligeramente diferentes, lo que da lugar a que los colores parezcan estar desplazados y tengan diferencias sutiles en el enfoque.

*Izquierda: 0,0 / Recto: 1.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Aberración acromática
Especifica si la aberración debe ser acromática, lo que significa que algunos o todos los colores tienen la misma distancia focal.

Esto hace que el efecto de desenfoque parezca estar distribuido de forma más equitativa.

*Izquierda: Verdadero / Derecho: False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Ojo de gato
Activa el efecto del ojo del gato en la escena, lo que simula cómo la luz que entra en un ángulo oblicuo no entra en un disco, sino en un óvalo irregular, lo que provoca distorsión.

Este efecto es más pronunciado en aperturas más altas, es decir, valores de punto F más bajos.

*Izquierda: Verdadero / Derecho: False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
