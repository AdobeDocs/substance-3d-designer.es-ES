---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: Utilice la función Enviar a interoperabilidad de Substance 3D Designer para exportar materiales a otras aplicaciones.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Enviar a...  Interoperabilidad
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 1%

---


# Enviar a...  Interoperabilidad

![Enviar desde Designer a aplicaciones de Substance 3D](../../../assets/explorer-interop.png "Enviar desde Designer a aplicaciones de Substance 3D"){width="512px"}

Adobe Substance 3D Designer tiene interoperabilidad con [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) y [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html). Te permite *enviar* y *reenviar* el trabajo rápidamente, lo que facilita la iteración en el ecosistema de Substance 3D.

El flujo de trabajo suele ser el siguiente:

1. Establezca el atributo <b>Type</b> en las propiedades de un gráfico de [Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md)
1. En el panel [Explorer](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), seleccione el paquete que desea enviar
1. En el menú desplegable <b>Publish/Send</b> del Explorador, seleccione la aplicación de destino
1. Realizar cambios en los gráficos
1. Repita el paso 3 para volver a enviar el paquete y actualizar el activo enviado existente con sus cambios

>[!WARNING]
>
> Las características de interoperabilidad *no* están disponibles en la versión de <b>Steam</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Definición del tipo de gráfica

Los gráficos de Substance pueden tener muchas funcionalidades. Tendrá que definir de antemano cuál es la funcionalidad exacta de un gráfico para asegurarse de que se pueda enviar correctamente.

En la sección <b>Atributos </b>de las propiedades de un gráfico de [Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md), hay una opción <b>Type</b>, con un menú desplegable que tiene las siguientes opciones:

</td>
<td style="border: 0;" valign="top">

![Atributo de tipo de gráfico de Substance](../../../assets/type-attribute.jpg "Atributo de tipo de gráfico de Substance")

</td>
</tr>
</table>

* **No especificado** es el tipo predeterminado si no lo ha establecido. Dependiendo de la aplicación a la que envíe, puede interpretarse de forma diferente. [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) utilizará Material de forma predeterminada, por ejemplo;
* **El material estándar** es para materiales PBR multicanal, con [salidas](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) etiquetadas correctamente;
* **Material de pegatina** es para un material PBR multicanal con canal alfa, que se aplicará como pegatina en [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html);
* **Atlas Material** es para un material PBR multicanal que consta de varias imágenes atlas, para su uso con el [nodo de Atlas scatter](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md) en Designer o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html);
* **Filter** es para filtros de uso general, ambos usados en [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html);
* **El generador basado en malla** es para generadores de máscaras de entrada múltiple. Solo lo usa [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html);
* El **generador de texturas** es para mapas de un solo canal, como ruidos y procedimientos 2D;
* **Luz de ambiente** es para un entorno de iluminación de un solo canal, que se usa para iluminar escenas y objetos;
* **Textura clara** es para una textura de un solo canal aplicada a una luz física.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Menú &quot;Enviar a&quot;

El proceso de envío implicó [publicar](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) uno o más paquetes en archivos de recursos de Substance 3D (SBSAR) en segundo plano.

El envío de contenido se puede realizar de las siguientes maneras:

* Haga clic con el botón derecho en un paquete y abra <b>Enviar a...Submenú </b> en el menú contextual y, a continuación, seleccione <b>Enviar a...Opción </b> para la aplicación de destino;
* Haz clic en el botón ![](../../../assets/sendto-icon.jpg) <b>Publish/Send</b> situado en la parte superior del panel [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html) y, a continuación, elige <b>Enviar a...Opción </b> para la aplicación de destino.

</td>
<td style="border: 0;" valign="top">

Menú ![Publish/Enviar a en el Explorador](../../../assets/explorer-sendto-displayed.jpg "Menú Publish/Enviar a en el Explorador")

</td>
</tr>
</table>

### Reenvío

Al volver a enviar un paquete que *ya se envió una vez* a la aplicación *same target*, el activo se *actualizará* en la aplicación de destino con la nueva versión.

## Enviar a Player

[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) admite *tanto* archivos Substance 3D<b> (SBS) como <b>activos de Substance 3D</b> (SBSAR).</b>

El envío a Player requiere que el usuario *ubique manualmente* el ejecutable del Substance Player, lo que se puede hacer:

* Cuando se le pregunte si el Reproductor *nunca se encontró* desde que se instaló Designer;
* En cualquier momento en el menú <b>Herramientas</b>, usando <b>Substance Player > Buscar...Opción </b>.

En Player, la recepción desde Designer requiere que el usuario localice manualmente el *directorio de instalación* de Substance 3D Designer, lo que se puede hacer:

* Cuando se le pregunte si Designer *nunca se encontró* desde que se instaló el Reproductor;
* En cualquier momento en el menú <b>Opciones</b>, usando la opción <b>Localizar Adobe Substance 3D Designer</b>.

>[!NOTE]
>
> Al enviar archivos Substance 3D (SBS) al Reproductor, se publica un recurso de Substance 3D (SBSAR) como *archivo temporal*.

## Problemas

Es posible que aparezcan errores al enviar paquetes, como:

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


Esto suele deberse a errores y advertencias estándar, y corríjalos para resolver el problema:

* No hay [nodos de salida](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) definidos en el gráfico. Agregar nodos de salida y conectar algo a ellos;
* Variables faltantes o rotas en [Obtener nodos](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) en [gráficos de funciones](../../../function-graphs/function-graphs.md). Rastrearlos con el *distintivo de advertencia amarillo* en los nodos afectados.
