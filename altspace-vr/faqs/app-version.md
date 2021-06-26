---
title: Búsqueda de la versión de la aplicación AltspaceVR
description: Aprenda a usar la aplicación AltspaceVR, la configuración y los registros de cliente para encontrar la versión de AltspaceVR que está ejecutando actualmente.
ms.date: 02/10/2021
ms.topic: article
keywords: versión de la aplicación
ms.openlocfilehash: 6b710e1724b890fa7ba0eecfcd774ef63128d5b7
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923182"
---
# <a name="finding-the-altspacevr-app-version"></a>Búsqueda de la versión de la aplicación AltspaceVR

En el transcurso de la solución de problemas de un problema, es posible que se le pregunte qué versión de la aplicación AltspaceVR está ejecutando actualmente.

## <a name="in-altspacevr"></a>En AltspaceVR

Para buscar la versión de la aplicación en AltspaceVR, vaya al menú **de configuración** y seleccione **Acerca de** en la barra de navegación izquierda. La "versión de la aplicación" se notifica aquí, como se muestra en la captura de pantalla siguiente.

![Menú Configuración abierto con acerca del panel abierto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a>En Configuración del sistema de Windows

Si instaló AltspaceVR a través del Microsoft Store, también puede encontrar la versión de la aplicación en la configuración del sistema de Windows.  Este escenario es una buena opción al notificar la versión de la aplicación si no puede iniciar sesión correctamente en el cliente.

Para buscar la versión de la aplicación en la configuración del sistema de Windows, abra el menú Inicio **,** escriba Aplicaciones **& características** y seleccione el resultado. Vaya a **AltspaceVR** en la lista de aplicaciones. Haga clic con el botón izquierdo en AltspaceVR y **seleccione Opciones avanzadas** en el menú que aparece.

![Menú Aplicaciones y características abierto con la opción avanzadas resaltada](images/app-version-img-02.png)

En Opciones avanzadas , **en** el encabezado **Especificaciones,** la versión **de** la aplicación debe aparecer a la derecha de la **etiqueta** Versión.

![Opciones avanzadas abiertas con la versión de la aplicación resaltada](images/app-version-img-03.png)

## <a name="in-client-logs"></a>En registros de cliente

AltspaceVR notifica la versión de la aplicación en el archivo de registros de cliente como "Altspace Version" durante el inicio de la aplicación. Esta sería una buena opción para obtener la versión de la aplicación si no se puede iniciar sesión correctamente en el cliente, pero se intentó iniciar antes de que se realizara el error.

## <a name="windows"></a>Windows

En Windows, el archivo de registros de cliente se puede encontrar a través Explorador de Windows en:

```
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player.log
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player-prev.log
```

Este archivo se sobrescribe cada vez que se inicia AltspaceVR. "Player.log" representa la sesión más reciente y "Player-prev.log" representa la sesión anterior.

## <a name="via-powershell"></a>A través de PowerShell

Los usuarios avanzados pueden buscar en los registros de cliente esta cadena a través de PowerShell como se muestra a continuación:

Entrada:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Salida:

[2.047] AltspaceVR Versión: 3.2.23.e66c2