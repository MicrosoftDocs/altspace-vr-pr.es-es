---
title: Búsqueda de la versión de la aplicación AltspaceVR
description: Aprenda a usar la aplicación AltspaceVR, la configuración y los registros de cliente para encontrar la versión de AltspaceVR que está ejecutando actualmente.
ms.date: 02/10/2021
ms.topic: article
keywords: versión de la aplicación
ms.openlocfilehash: 5d503d3b89cd213696dd53616c5c7e3013aeef01
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213775"
---
# <a name="finding-the-altspacevr-app-version"></a>Búsqueda de la versión de la aplicación AltspaceVR

En el transcurso de la solución de un problema, es posible que se le pregunte qué versión de la aplicación AltspaceVR está ejecutando actualmente.

## <a name="in-altspacevr"></a>En AltspaceVR

Para buscar la versión de la aplicación en AltspaceVR, vaya al **menú configuración** y seleccione **acerca** de en la barra de navegación izquierda. Aquí se indica la versión de la aplicación, como se muestra en la captura de pantalla siguiente.

![Menú de configuración abrir con el panel de información abierto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a>En configuración del sistema de Windows

Si instaló AltspaceVR mediante el Microsoft Store, también puede buscar la versión de la aplicación en la configuración del sistema de Windows.  Este escenario es una buena opción para notificar la versión de la aplicación si no puede iniciar sesión correctamente en el cliente.

Para buscar la versión de la aplicación en la configuración del sistema de Windows, abra el **menú Inicio**, escriba en **aplicaciones & características** y seleccione el resultado. Vaya a **AltspaceVR** en la lista de aplicaciones. Haga clic con el botón izquierdo en AltspaceVR y seleccione **Opciones avanzadas** en el menú que aparece.

![Menú Aplicaciones y características abierto con la opción Opciones avanzadas resaltada](images/app-version-img-02.png)

En las **Opciones avanzadas**, en el encabezado de **Especificaciones** , la versión de la **aplicación** debe aparecer a la derecha de la etiqueta de **versión** .

![Opciones avanzadas abiertas con la versión de la aplicación resaltada](images/app-version-img-03.png)

## <a name="in-client-logs"></a>En registros de cliente

AltspaceVR informa de la versión de la aplicación en el archivo de registros de cliente como "versión de Altspace" durante el inicio de la aplicación. Esta sería una buena opción para obtener la versión de la aplicación si no puede iniciar sesión correctamente en el cliente, pero se ha intentado iniciar antes de que se produjera un error.

## <a name="windows"></a>Windows

En Windows, el archivo de registro de cliente se puede encontrar a través del explorador de Windows en:

```
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player.log
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player-prev.log
```

Este archivo se sobrescribe cada vez que se inicia AltspaceVR. ' Player. log ' representa la sesión más reciente y ' Player-Prev. log ' representa la sesión anterior.

## <a name="via-powershell"></a>A través de PowerShell

Los usuarios avanzados pueden buscar en los registros de cliente esta cadena a través de PowerShell de la siguiente manera:

Entrada:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Salida:

[2,047] versión de AltspaceVR: 3.2.23. e66c2