---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/camera/post-effects.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Efectos de posprocesamiento

![Efectos de posprocesamiento](post-effects.resources/post-effects-01.png "Efectos de posprocesamiento"){zoomable="yes"}

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
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-03.jpg" alt="PostFXReinhard">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXReinhard](post-effects.resources/post-effects-03.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-04.jpg" alt="PostFXAtan">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXAtan](post-effects.resources/post-effects-04.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-05.jpg" alt="PostFXExp">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXExp](post-effects.resources/post-effects-05.jpg "PostFXExp")

+++

+++Registro


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-06.jpg" alt="PostFXLog">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXLog](post-effects.resources/post-effects-06.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-07.jpg" alt="PostFXAces">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXAces](post-effects.resources/post-effects-07.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-08.jpg" alt="PostFXHejl">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXHejl](post-effects.resources/post-effects-08.jpg "PostFXHejl")

+++

+++Neutro


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-09.jpg" alt="PostFXNeutral">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXNeutral](post-effects.resources/post-effects-09.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-10.jpg" alt="PostFXAgx">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXAgx](post-effects.resources/post-effects-10.jpg "PostFXAgx")

+++

+++Neutral Pbr


<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-02.jpg" alt="PostFXDisdisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-11.jpg" alt="PostFXPbrNeutral">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![PostFXDisdisabled](post-effects.resources/post-effects-02.jpg "PostFXDisdisabled")

![PostFXPbrNeutral](post-effects.resources/post-effects-11.jpg "PostFXPbrNeutral")

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
      <img src="post-effects.resources/post-effects-12.jpg" alt="bloomThreshold1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-13.jpg" alt="bloomThreshold4">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomThreshold1](post-effects.resources/post-effects-12.jpg "bloomThreshold1")

![bloomThreshold4](post-effects.resources/post-effects-13.jpg "bloomThreshold4")

+++

+++Difuminación
La rampa de atenuación de la floración, donde un valor más bajo da como resultado un radio de floración más corto.

*Izquierda: 1.0 / Derecha: 0,6*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-14.jpg" alt="bloomFalloff1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-15.jpg" alt="bloomFalloff0-6">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomFalloff1](post-effects.resources/post-effects-14.jpg "bloomFalloff1")

![bloomFalloff0-6](post-effects.resources/post-effects-15.jpg "bloomFalloff0-6")

+++

+++Nivel
La intensidad de la floración. Un valor más alto da como resultado unos halos de luz más brillantes y pronunciados.

*Izquierda: 8.0 / Derecha: 2.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-16.jpg" alt="bloomLevel8">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-17.jpg" alt="bloomLevel2">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomLevel8](post-effects.resources/post-effects-16.jpg "bloomLevel8")

![bloomLevel2](post-effects.resources/post-effects-17.jpg "bloomLevel2")

+++

+++Cambio de color
Desplaza el tono de las áreas afectadas por la floración hacia colores más cálidos.

*Izquierda: 0,0 / Derecha: 0,8*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-18.jpg" alt="bloomColorShift0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-19.jpg" alt="bloomColorShift0-8">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![bloomColorShift0](post-effects.resources/post-effects-18.jpg "bloomColorShift0")

![bloomColorShift0-8](post-effects.resources/post-effects-19.jpg "bloomColorShift0-8")

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
      <img src="post-effects.resources/post-effects-20.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-21.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](post-effects.resources/post-effects-20.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](post-effects.resources/post-effects-21.jpg "depthOfFieldMaxRadius4")

+++

+++Intensidad de la composición
Magnitud del efecto de desenfoque desde la distancia de enfoque hacia fuera.

*Izquierda: 0.2 / Derecha: 0,05*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-22.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-23.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](post-effects.resources/post-effects-22.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](post-effects.resources/post-effects-23.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Aberración longitudinal
Intensidad de la aberración que se produce lejos de la distancia de enfoque.

La aberración simula el modo en que las diferentes longitudes de onda de la luz tienen distancias focales ligeramente diferentes, lo que da lugar a que los colores parezcan estar desplazados y tengan diferencias sutiles en el enfoque.

*Izquierda: 0,0 / Recto: 1.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-24.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-25.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](post-effects.resources/post-effects-24.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](post-effects.resources/post-effects-25.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Aberración acromática
Especifica si la aberración debe ser acromática, lo que significa que algunos o todos los colores tienen la misma distancia focal.

Esto hace que el efecto de desenfoque parezca estar distribuido de forma más equitativa.

*Izquierda: Verdadero / Derecho: False*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-26.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-27.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](post-effects.resources/post-effects-26.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](post-effects.resources/post-effects-27.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Ojo de gato
Activa el efecto del ojo del gato en la escena, lo que simula cómo la luz que entra en un ángulo oblicuo no entra en un disco, sino en un óvalo irregular, lo que provoca distorsión.

Este efecto es más pronunciado en aperturas más altas, es decir, valores de punto F más bajos.

*Izquierda: Verdadero / Derecho: False*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/post-effects-28.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/post-effects-29.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Después De</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](post-effects.resources/post-effects-28.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](post-effects.resources/post-effects-29.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
