---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: Solución de problemas de scripts de Python en Substance 3D Designer, incluidos problemas de plugins y API.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemas de Python
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Problemas de Python

En esta página se enumeran los problemas técnicos relacionados con la [API Python](../../scripting/scripting.md) de Substance 3D Designer, así como las funciones implementadas en Python, y se ofrecen pasos de solución de problemas para cada uno.

Las características implementadas en Python incluyen las acciones [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Enviar a](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) en la barra de herramientas de [Explorer](../../interface/the-explorer-window/the-explorer-window.md), así como la herramienta para quitar los nodos no utilizados en los gráficos.

## El módulo &#39;QtForPython&#39; no se carga

<b>![(error)](../../assets/error.svg) Problema</b>

El módulo Python &#39;QtForPython&#39; no se carga, por lo que faltan características implementadas en Python, como las acciones [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Enviar a](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) en la barra de herramientas del [Explorador](../../interface/the-explorer-window/the-explorer-window.md), así como la herramienta para quitar los nodos no utilizados en los gráficos.

Además, muchos [complementos de Python](../../scripting/plugin-basics/plugin-basics.md) no se cargarán o no funcionarán del modo esperado.

<b>![(tick)](../../assets/check.svg) Pasos recomendados</b>

Es probable que haya un conflicto entre la instalación de QtForPython por parte de Designer y sus dependencias, y una instalación existente en el sistema.

Quite cualquier otra instalación del sistema de [QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/)) y [Shiboken2](https://pypi.org/project/shiboken2/).

Alternativamente, en lugar de una instalación de QtForPython en todo el sistema, puedes considerar usar Python *entornos virtuales* o un *administrador de paquetes* como [rez](https://github.com/AcademySoftwareFoundation/rez).
