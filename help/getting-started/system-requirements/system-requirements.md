---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Revise los requisitos del sistema de Substance 3D Designer para asegurarse de que su equipo cumple las especificaciones necesarias.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Requisitos del sistema
user-guide-description: ''
user-guide-title: ''
source-git-commit: ec787363bab8318804a71d6cf7c5484fc67a987e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# Sistemas compatibles

A continuación se muestra una lista de hardware y sistemas compatibles con la aplicación:

## Windows

|  | Mínimo | Recomendado | Óptimo |
| --- | --- | --- | --- |
| <b>SO</b> | Windows 11 de 64 bits, versión 23H2 | Windows 11 Versión de 64 bits 24H1 | Windows 11 de 64 bits, versión 24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Almacenamiento</b> | SSD con 30 GB de espacio disponible | SSD con 50 GB de espacio disponible | SSD con 70 GB de espacio disponible |

### macos

|  | Mínimo | Recomendado | Óptimo |
| --- | --- | --- | --- |
| <b>SO</b> | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Almacenamiento</b> | SSD con 30 GB de espacio disponible | SSD con 50 GB de espacio disponible | SSD con 70 GB de espacio disponible |

### Linux

| Empresas | Vapor |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## Recomendaciones generales

* Para trabajar en condiciones cómodas, recomendamos un monitor con una resolución superior a 1 megapíxel y más ancho que 1280 píxeles.
* Muchas aplicaciones de Substance dependen de OpenSSL 1.1.1 para la compatibilidad con RHEL8/9. Para los sistemas con versiones más recientes de OpenSSL, deberá proporcionarlo manualmente.
* *Solo se han notarizado* versiones <b>2019.x</b> y superiores para poder ejecutarse en <b>MacOS 10.15</b> (Catalina).
* <b>Es posible establecer una conexión de Escritorio remoto</b> si hay disponible un contexto de OpenGL 3.3. Funcionará en <b>Nvidia Quadro</b>, pero *no* en Nvidia GeForce porque solo proporciona un contexto OpenGL 1.4. Si se trata de un problema, recomendamos usar soluciones alternativas como <b>VNC</b>/<b>Teamviewer</b>.
* Los usuarios de la versión <b>Steam</b> deben *deshabilitar* la <b>superposición de Steam</b> para Designer, ya que puede causar problemas de rendimiento cuando está activa.

## GPU compatibles

A continuación se muestra una lista de GPU compatibles con la aplicación:

* NVIDIA GeForce GTX 1060 y superior
* NVIDIA Quadro P2200 y superior
* AMD Radeon RX 580 y superior
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR (solo Windows)**
> 
> Para obtener la mejor estabilidad general al realizar cálculos pesados en la GPU, por ejemplo, procesar gráficos complejos, procesar en la vista 3D, exportar una escena de la vista 3D, etc., se recomienda encarecidamente asegurarse de que los valores de <b>Detección y recuperación de tiempo de espera (TDR)</b> coincidan con las recomendaciones de [esta página](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) de nuestra documentación.

## Configuraciones no compatibles

<b>Windows</b>

* No se admiten máquinas virtuales.
* Windows Server no es compatible.

<b>macOS</b>

* Los sistemas macOS basados en Intel no son compatibles.
* Solo se admiten configuraciones oficiales de Apple.
* Las eGPU no son compatibles actualmente y pueden presentar problemas de estabilidad.

<b>Linux</b>

* Los controladores Mesa en Linux no son compatibles.

<b>Cualquier plataforma</b>

* Las GPU integradas no son compatibles con las CPU x86-64 (Intel, AMD).
* No se admite el uso de Designer en combinación con software de terceros que intercepte llamadas de Designer a los controladores gráficos. Dicho software incluye:
  * Inyectores de proceso posterior, como los reshaders que aplican gradación de color, efectos de cámara, ...
  * Superposiciones en pantalla como cruces personalizadas, métricas de rendimiento de GPU, máscaras para streaming de vídeo...

## Versiones mínimas del controlador de GPU

A continuación se muestra una lista de las versiones mínimas del controlador de la GPU necesarias para que la aplicación se ejecute sin problemas. Esta lista está sujeta a cambios a medida que se lancen nuevas versiones.

Para descargar nuevos controladores, consulte: [La GPU tiene controladores obsoletos](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| SO | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | No admitido |

>[!NOTE]
>
> En **Mac OS**, el controlador de la GPU lo proporciona el propio sistema operativo. Actualice a la versión más reciente del sistema operativo para acceder al controlador más reciente.

## Trazado de rayos de GPU para hornear

Para habilitar el Trazado de rayos de GPU a través de Optix o DXR, deben instalarse los controladores recomendados anteriormente.

<b>DXR</b> requiere la siguiente configuración mínima:

* <b>Windows 10</b> versión 1809, consulte [esta página](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) para obtener más información
* <b>GPU con arquitectura Pascal</b> (NVIDIA GeForce 10XX)

>[!TIP]
>
> Trazado de rayos de GPU funciona de forma óptima con hardware de trazado de rayos como las GPU NVIDIA GeForce RTX o NVIDIA Quadro RTX.

## Uso de tabletas

Los usuarios de tabletas en <b>Windows</b> deben aplicar la configuración descrita en la página siguiente para obtener la experiencia más confiable: [Configurando bolígrafos y tablets](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

## Idiomas

La interfaz de software está disponible en los siguientes idiomas:

* Deutsch (Deutschland)
* Inglés (Estados Unidos)
* Español (España)
* Français (Francia)
* Italiano (Italia)
* Português (Brasil)
* 日 本 語(日 本)
* 한 국 어(한 국)
* 简 体 中 文(中 国)
