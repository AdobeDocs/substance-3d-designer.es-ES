---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: Obtenga información sobre las directrices para reducir el tamaño de los archivos de gráficos Substance y optimizar el rendimiento y los requisitos de almacenamiento.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Directrices de reducción de tamaño de archivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# Información general

En algunos casos, el tamaño total del archivo de [Substance 3D Assets (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) puede ser un factor importante. Esta página cubre algunas áreas críticas y configuraciones que se deben tener en cuenta al intentar reducir el tamaño del archivo.

El tamaño del archivo está determinado principalmente por [mapas de bits incrustados.](../../resources/bitmap-resource/bitmap-resource.md) Son archivos que están vinculados, incrustados o hechos un bake y agregados al archivo (SBS) [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) como recurso. En el recurso de Substance 3D solo se publican los mapas de bits que se utilizan en un gráfico, es decir, que están conectados a una salida, ya sea directamente o a través de la cadena de nodos. En un archivo de Substance 3D, los mapas de bits no afectan al tamaño del archivo, ya que todos los recursos de mapas de bits se almacenan fuera del archivo.

>[!IMPORTANT]
>
> Asegúrese de que la propiedad [Output size](../../compositing-graphs/output-size/output-size.md) de todos los nodos [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) esté establecida en el *método de herencia [Absolute*](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Si no es así, su [recurso de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) al que se hace referencia se guardará con la resolución predeterminada de 256\*256 en el archivo de recursos de Substance 3D publicado, lo que* afectará a la calidad* de una o más salidas.

## Factores de tamaño de archivo

Hay varios factores que afectan al tamaño total de archivo de SBSAR. Se enumeran a continuación con una breve explicación.

+++Resolución
Obviamente tiene un gran efecto. Utilice la resolución más pequeña posible, teniendo en cuenta que es posible que también desee que el archivo de Substance funcione en resoluciones grandes. Puede utilizar trucos de máscara de resolución estándar para hacer que los mapas de bits más pequeños parezcan más grandes.

*Encontrado en: o importar o volver a exportar mapa de bits en Designer.*

+++

+++Modo de color de archivo
Si se establece en el Editor de imágenes antes de la exportación, el modo de color también afecta al tamaño del archivo cuando se utiliza el formato de mapa de bits sin procesar. Los mapas de bits de solo escala de grises son más pequeños que las imágenes de RGB (A).

*Encontrado en: o importar o volver a exportar mapa de bits en Designer al configurar [nodos de salida](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) correctamente.*

+++

+++Formato del archivo
El formato de archivo de las imágenes marca la diferencia, aunque puede ignorarse en algunos casos. Un programa como Photoshop permite un poco más de control sobre la compresión JPG y a veces puede ofrecer un camino medio decente.

*Encontrado en: o importar o volver a exportar mapa de bits en Designer.*

+++

+++Uso en el gráfico
El modo en que se establece el nodo Mapa de bits también afecta a la forma en que Designer comprimirá el archivo. El uso de un archivo en modo Escala de grises como mapa de bits de color en el gráfico generará archivos más grandes. ¡Asegúrese de configurarlas correctamente!

*Encontrado en:[Propiedades de nodo de mapa de bits.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++Formato de mapa de bits en el paquete
En las propiedades del recurso puede elegir entre la compresión &quot;Raw&quot; y &quot;JPEG&quot;. Esto puede tener un efecto considerable en el resultado final.

*Encontrado en: Propiedades del recurso de mapa de bits, a través de la ventana del explorador.*

+++

+++Calidad de compresión de mapa de bits en el paquete
Al utilizar el formato de mapa de bits &quot;JPEG&quot;, el regulador que aparece a continuación puede afectar a la calidad y al tamaño del archivo. Este regulador no se comporta de forma muy predecible, pero 1 tiende a corresponder a la mayor calidad JPG compresión más alta y 0,5 tiende a dar el tamaño más pequeño.

*Encontrado en: Propiedades del recurso de mapa de bits, a través de la ventana del explorador.*

+++

+++Modo de compresión al publicar
Al publicar en SBSAR, puede elegir entre &quot;Automático&quot;, &quot;Óptimo&quot; y &quot;Ninguno&quot; para la compresión, lo que puede marcar una diferencia considerable si utiliza el formato de mapa de bits &quot;Raw&quot;. También tiene un gran impacto en la velocidad de exportación. Por lo general no se recomienda utilizar &quot;ninguno, ya que no ofrece ningún aumento de la calidad.

*Encontrado en: configuración de publicación final para un paquete SBSAR.*

+++

## Comparación de tamaño de archivo

La siguiente tabla muestra la influencia de todas las configuraciones entre sí. El mapa de bits utilizado es una imagen 4096x4096 de ruido generado, exportada de Photoshop como TGA de 24 bits o JPG de calidad 8. Los TGA también se exportaron en modo Escala de grises y RGBA.

El gráfico solo coloca un único nodo de mapa de bits conectado a una única salida. El modo Mapa de bits se establece según el modo de archivo de origen.

Aunque la tabla de la derecha no es totalmente concluyente, se puede aprender lo siguiente al comparar los resultados visuales y los tamaños de archivo:

* Mapa de bits sin formato + Compresión óptima proporciona la mejor calidad con un tamaño de archivo aceptable.
* Los archivos de origen precomprimidos pueden reducir el tamaño de los archivos en la mayoría de los casos, pero a un coste de calidad.
* Los tamaños de archivo más pequeños, pero la peor calidad se obtiene con JPG formato de paquete  en la calidad 0.5.
* La escala de grises no siempre es más pequeña en el tamaño de archivo, pero tendrá una calidad superior que el color en configuraciones similares.

>[!NOTE]
>
> **Formato De Mapa De Bits Jpeg**
> 
> Es importante tener en cuenta que los mapas especiales que requieren una alta precisión, como los mapas normales, los mapas vectoriales y otros, probablemente no deben establecerse en compresión JPEG, ya que esto dará lugar a artefactos mucho más visibles!

| Imagen de origen | Color TGA | JPG de color | Escala de grises TGA |  de JPG de escala de grises |
| --- | --- | --- | --- | --- |
| <b>Formato de mapa de bits sin procesar</b>, modo de compresión: *Ninguno* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>Formato de mapa de bits sin procesar</b>, modo de compresión: *Mejores* | 9.11 MB | 3,37 MB | 5,06 MB | 4,75 MB |
| <b>Formato De Mapa De Bits Jpeg</b> Calidad De Compresión: *1* | 5,09 MB | 1,94 MB | 6,30 MB | 2,49 MB |
| <b>Formato De Mapa De Bits Jpeg</b> Calidad De Compresión: *0,5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>Formato De Mapa De Bits Jpeg</b> Calidad De Compresión: *0* | 407 KB | 433 KB | 990 KB | 808 KB |
