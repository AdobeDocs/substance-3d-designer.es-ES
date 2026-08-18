---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: Utilice el nodo Mapeado de flujo de spline para crear patrones de textura fluida a lo largo de trazados de spline para obtener efectos orgánicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Flow Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Spline Flow Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-flow-mapper-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja un mapa de flujo donde se dibujan los datos vectoriales de flujo a lo largo de las splines de entrada.

Esto permite utilizar splines para controlar la dirección, trayectoria, intensidad y thickness del flujo, así como la pendiente de degradado utilizada para atenuar los datos dibujados en el fondo neutro.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> El resultado puede incluir artefactos no deseados fuera del envolvente de la spline cuando se utilizan valores de thickness muy bajos. Se trata de un problema conocido.

## Conectores de entrada

<b>Códigos polinómicos</b> *Color* Coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen en color:\
Posición <b> R</b> - X\
<b> G</b> - Posición Y\
<b> B</b> - Height\
    <b>A</b> - Datos empaquetados:\
        * Firmar: La spline está cerrada (negativa) o abierta (positiva);\
        * Valor absoluto: Thickness + 1.

<b>Datos de spline</b> *Color* Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - No utilizado\
<b> A</b> - No utilizado

<b>Cantidad de spline</b> *Entero* Número de splines de entrada.

<b>Curva de perfiles de atenuación</b> *Escala de grises*<span id="_Hlk135812146"></span> Imagen que describe una curva utilizando los valores de su primera fila de píxeles.\
Cuando el parámetro Perfil de atenuación se define en Curva de perfil de entrada, esta entrada se utiliza para controlar la pendiente de degradado para la atenuación de los datos del vector de flujo dibujados a lo largo de la spline.\
Puede utilizar un nodo [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para crear la curva.

## Conectores de salida

<b>Salida</b> *Color* Mapa de flujo de salida codificado en una imagen en color.

## Parámetros

<b>Cantidad de segmentos</b> *Entero* Las splines se simplifican en segmentos antes de que los datos de flujo vectorial los atraviesen.\
Una mayor cantidad de segmentos produce una asignación de flujo más fluida a lo largo de las curvas.

<b>Modo</b> *Entero* Método de selección de las splines a lo largo de las cuales se deben dibujar los datos de flujo vectorial:\
*- Dibujar lista de spline*: Se utilizan todas las splines de la lista de entrada;\
*: dibujar una spline*: Sólo se utiliza la spline con el índice especificado;\
*- Dibujar rango de spline*: Sólo se utilizan las splines cuyo índice se incluye en el rango especificado.

<b>Dibujar índice de spline</b> *Entero* (disponible cuando &quot;Modo&quot; está establecido en &quot;Dibujar una spline&quot;)El índice de la spline a lo largo de la cual se deben dibujar los datos de flujo vectorial.

<b>Dibujar rango de spline</b> *Entero2* (disponible cuando &quot;Modo&quot; está establecido en &quot;Dibujar rango de spline&quot;)Intervalo de índices de las splines a lo largo de las cuales se deben dibujar datos de flujo vectorial.

<b>Modo de Thickness</b> *Integer* Método para establecer el thickness de los datos de flujo vectorial dibujados\
*- Manual*: Establezca el thickness explícitamente con un valor arbitrario;\
*- Desde spline*: Utilice el thickness de la spline.

<b>Thickness</b> *Float* (Disponible cuando &quot;Modo de Thickness&quot; está establecido en &quot;Manual&quot;)El valor arbitrario para el thickness de los datos de flujo vectorial dibujados a lo largo de las splines.<b></b>

<b>Multiplicador de Thickness</b> *Float* (Disponible cuando &quot;Modo de Thickness&quot; está establecido en &quot;Desde spline&quot;) Un multiplicador global para el thickness de los datos de flujo vectorial dibujados a lo largo de las splines, cuando ese thickness está controlado por el de las splines.

<b>Dirección</b> *Entero* Dirección del flujo vectorial en relación con la spline.\
*- Tangente*: Utilizar el vector tangente de la spline;\
*- Normal*: Utilizar el vector normal de la spline;\
*: reflejo normal*: Utilice la versión reflejada del vector normal de la spline.

<b>Voltear dirección</b> *Boolean* Invierte la dirección de las splines, lo que también afecta a la dirección del vector de flujo.

<b>Perfil de atenuación</b> *Entero* La rampa de degradado utilizada para dibujar la atenuación de los datos del vector de flujo dibujados a lo largo de la spline:\
*- Lineal*: Utilice una rampa de degradado lineal;\
*- Gaussiano*: Utilizar una rampa de degradado gaussiana\
*- Curva de perfiles de entrada*: Utilice la curva proporcionada en la entrada Curva de perfil de atenuación como rampa de degradado.

<b>Iniciar atenuación</b> *Booleano*<span id="_Hlk135769398"></span> Agrega un semicírculo al comienzo de la spline. El semicírculo utiliza la misma atenuación que la spline.

<b>Finalizar atenuación</b> *Boolean* Agrega un semicírculo al final de la spline. El semicírculo utiliza la misma atenuación que la spline.

<b>Atenuación de Height spline</b> *Flotante* La intensidad de los datos del vector de flujo dibujados a lo largo de la spline se multiplica frente al height de la spline, donde los datos dibujados se desvanecen hasta el color neutro del fondo (0,5, 0,5, 0) a medida que el height se acerca a 0.

<b>Corrección no cuadrada </b>*Booleano* Ajusta la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones no cuadradas.\
Esto también afecta a la distribución uniforme.

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineFlowMapper-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
