---
title: Búsqueda de la versión de la aplicación AltspaceVR
description: Obtenga información sobre cómo usar la aplicación AltspaceVR, la configuración y los registros de cliente para encontrar la versión de AltspaceVR que está ejecutando actualmente.
ms.date: 02/10/2021
ms.topic: article
keywords: versión de la aplicación
ms.openlocfilehash: fbf67a8302a67ddb916772420949cf0509a0d4a60c472711975c651862438b93
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128259"
---
# <a name="finding-the-altspacevr-app-version"></a>Búsqueda de la versión de la aplicación AltspaceVR

En el transcurso de la solución de problemas, es posible que se le pregunte qué versión de la aplicación AltspaceVR está ejecutando actualmente.

## <a name="in-altspacevr"></a>En AltspaceVR

Para buscar la versión de la aplicación en AltspaceVR, vaya al menú **de** configuración y seleccione **Acerca de** en la barra de navegación izquierda. La "versión de la aplicación" se notifica aquí, como se muestra en la captura de pantalla siguiente.

![Configuración menú abierto con acerca del panel abierto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a>En Windows system Configuración

Si ha instalado AltspaceVR a través de la Microsoft Store, también puede encontrar la versión de la aplicación en la Windows configuración del sistema.  Este escenario es una buena opción al notificar la versión de la aplicación si no puede iniciar sesión correctamente en el cliente.

Para buscar la versión de la aplicación en Windows configuración del sistema, abra el menú Inicio **,** escriba Aplicaciones & **características y** seleccione el resultado. Vaya a **AltspaceVR en** la lista de aplicaciones. Haga clic con el botón izquierdo en AltspaceVR y **seleccione Opciones avanzadas** en el menú que aparece.

![Menú Aplicaciones y características abierto con la opción avanzada resaltada](images/app-version-img-02.png)

En Opciones avanzadas , **en** el encabezado **Especificaciones,** la **versión de** la aplicación debe aparecer a la derecha de la **etiqueta** Versión.

![Opciones avanzadas abiertas con la versión de la aplicación resaltada](images/app-version-img-03.png)

## <a name="in-client-logs"></a>En los registros de cliente

AltspaceVR notifica la versión de la aplicación en el archivo de registros de cliente como "Altspace Version" durante el inicio de la aplicación. Esta sería una buena opción para obtener la versión de la aplicación si no se puede iniciar sesión correctamente en el cliente, pero se intentó iniciar antes de que se realizara el error.

## <a name="windows"></a>Windows

En Windows, el archivo de registros de cliente se puede encontrar a través de Windows Explorer en:

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