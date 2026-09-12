---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: Aprenda a activar Substance 3D Designer y administrar licencias para acceder a todas las funciones y capacidades.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Activación y licencias
user-guide-description: ''
user-guide-title: ''
source-git-commit: 65a0ec6dc38e7595406c0c531be72ad1670dfb86
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---


# Proceso de activación por tipo de aplicación

El proceso de activación depende de dónde haya comprado Designer o tenga acceso a él:

| Edición | Proceso de activación |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creative Cloud de sobremesa (CCD) | Instale el producto desde la aplicación de CCD y, a continuación, inícielo. Vaya a estas páginas si tiene problemas con su licencia: [Las aplicaciones no se iniciarán debido al error de suscripción](https://helpx.adobe.com/es/creative-cloud/apps/troubleshoot/launch-issues/apps-wont-launch-due-to-subscription-error.html) / [Ayuda de cuenta, planes y facturación](https://helpx.adobe.com/es/account/individual.html) |
| Vapor | Inicie el producto directamente desde su biblioteca de Steam. |
| Substance (independiente) | Consulte el proceso de activación que se describe a continuación. |

## Pasos de activación (edición de Substance)

### USO DEL ASISTENTE DE ACTIVACIÓN

Hay tres opciones disponibles:

* <b>Evaluar este producto</b>: Las pruebas heredadas ya no están disponibles. En su lugar, puedes iniciar una versión de prueba de 30 días para cada aplicación de Substance 3D [aquí](https://www.adobe.com/creativecloud/3d-augmented-reality.html) o con Creative Cloud Desktop. Cada versión de prueba es independiente de las demás aplicaciones de Substance 3D, por lo que puede probarlas una a una o todas a la vez.
* <b>Activar usando un archivo de licencia</b>: active el producto con un archivo de licencia (<b>\*.key</b>) descargado de la página de su cuenta en el [sitio web de Substance 3D](https://store.substance3d.com/user) antes del 30 de septiembre de 2022.
* <b>Activar usando tu cuenta</b>: Las cuentas de sustancias heredadas ya no se pueden utilizar para la activación.

>[!IMPORTANT]
>
> Para instalar el archivo de licencia con el Asistente de activación, asegúrese de ejecutar Designer como administrador y desactive temporalmente el antivirus.

![Asistente de activación](activation-and-licenses.resources/activation-wizard.png "Asistente de activación")

### Activación manual

Puede activar Designer manualmente colocando el archivo license.key en la carpeta siguiente:

<table data-preserve-html="true">
<colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th style="text-align: left;">Platform</th>
<th style="text-align: left;">Versión</th>
<th colspan="2" style="text-align: left;">Ruta</th>
</tr><tr><td rowspan="4" style="text-align: left;"><b>Windows</b></td>
<td rowspan="2" style="text-align: left;"><b>11.2</b> o superior</td>
<td style="text-align: left;">AppData &gt; Local</td>
<td style="text-align: left;">C:\Users\[nombre de usuario]\AppData\Local\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Roaming</td>
<td style="text-align: left;">C:\Users\[nombre de usuario]\AppData\Roaming\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>11.1</b> o inferior</td>
<td style="text-align: left;">AppData &gt; Local</td>
<td style="text-align: left;">C:\Users\[nombre de usuario]\AppData\Local\Allegorithmic\Substance Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Roaming</td>
<td style="text-align: left;">C:\Users\[nombre de usuario]\AppData\Roaming\Allegorithmic\Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Mac</b></td>
<td style="text-align: left;"><b>11.2</b> o superior<br/>
</td>
<td colspan="2" style="text-align: left;">/Usuarios/[nombre de usuario]/Librería/Application Support/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> o inferior<br/>
</td>
<td colspan="2" style="text-align: left;">/Usuarios/[nombre de usuario]/Library/Application Support/Allegorithmic/Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Linux</b></td>
<td style="text-align: left;"><b>11.2</b> o superior</td>
<td colspan="2" style="text-align: left;">/home/[nombre de usuario]/.local/share/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> o inferior<br/>
</td>
<td colspan="2" style="text-align: left;">/home/[nombre de usuario]/.local/share/Allegorithmic/Substance Designer</td>
</tr></tbody></table>

>[!NOTE]
>
> Algunos de los directorios de las rutas mencionadas anteriormente pueden estar ocultos de forma predeterminada. Escriba la ruta de acceso manualmente en el explorador de archivos o muestre los archivos ocultos para verlos.

>[!IMPORTANT]
>
> Asegúrese de que el archivo se llama **license.key**; de lo contrario, la aplicación no podrá encontrarlo.

### VARIABLE DE ENTORNO

Puede invalidar la ubicación en la que Designer comprueba el archivo <b>license.key</b> con una [variable de entorno](../../pipeline-and-project-con/environment-variables/environment-variables.md).
