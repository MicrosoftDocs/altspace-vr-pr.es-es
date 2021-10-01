---
title: Preguntas más frecuentes sobre la aplicación AltspaceVR
description: Solución de problemas y compatibilidad con la aplicación AltspaceVR.
ms.date: 8/16/2021
author: qianw211
ms.author: v-qianwen
ms.topic: article
keywords: vr, AltspaceVR, solución de problemas, soporte técnico
ms.openlocfilehash: a0df1e100ef8511fe3c9129548529577964c2336
ms.sourcegitcommit: 5c452a9092297c0bfbc8efabebf395e7ee31853f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2021
ms.locfileid: "129311902"
---
# <a name="frequently-asked-questions-about-the-altspacevr-app"></a>Preguntas más frecuentes sobre la aplicación AltspaceVR

## <a name="finding-the-altspacevr-app-version"></a>Búsqueda de la versión de la aplicación AltspaceVR

En el transcurso de la solución de problemas, es posible que se le pregunte qué versión de la aplicación AltspaceVR está ejecutando actualmente.

### <a name="in-altspacevr"></a>En AltspaceVR

Para buscar la versión de la aplicación en AltspaceVR, vaya al menú **de** configuración y seleccione **Acerca de** en la barra de navegación izquierda. La "versión de la aplicación" se notifica aquí, como se muestra en la captura de pantalla siguiente.

![Configuración menú abierto con acerca del panel abierto](images/app-version-img-01.png)

### <a name="in-windows-system-settings"></a>En Windows system Configuración

Si instaló AltspaceVR a través del Microsoft Store, puede encontrar además la versión de la aplicación en la Windows configuración del sistema.  Este escenario es una buena opción al notificar la versión de la aplicación si no puede iniciar sesión correctamente en el cliente.

Para buscar la versión de la aplicación en Windows configuración del sistema, abra el menú Inicio **,** escriba Aplicaciones & **características y** seleccione el resultado. Vaya a **AltspaceVR en** la lista de aplicaciones. Haga clic con el botón izquierdo en AltspaceVR y **seleccione Opciones avanzadas** en el menú que aparece.

![Menú Aplicaciones y características abierto con la opción avanzada resaltada](images/app-version-img-02.png)

En Opciones avanzadas , **en** el encabezado **Especificaciones,** la **versión de** la aplicación debe aparecer a la derecha de la **etiqueta** Versión.

![Opciones avanzadas abiertas con la versión de la aplicación resaltada](images/app-version-img-03.png)

### <a name="app-version-in-client-logs"></a>Versión de la aplicación en los registros de cliente

AltspaceVR notifica la versión de la aplicación en el archivo de registros de cliente como "Altspace Version" durante el inicio de la aplicación. Esta sería una buena opción para obtener la versión de la aplicación si no se puede iniciar sesión correctamente en el cliente, pero se intentó iniciar antes de que se realizara el error.

### <a name="windows"></a>Windows

En Windows, el archivo de registros de cliente se puede encontrar a través Windows Explorer en:

```
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player.log
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player-prev.log
```

Este archivo se sobrescribe cada vez que se inicia AltspaceVR. "Player.log" representa la sesión más reciente y "Player-prev.log" representa la sesión anterior.

### <a name="via-powershell"></a>A través de PowerShell

Los usuarios avanzados pueden buscar esta cadena en los registros de cliente a través de PowerShell como se muestra a continuación:

Entrada:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Salida:

[2.047] AltspaceVR Versión: 3.2.23.e66c2

## <a name="how-do-i-upload-my-client-logs"></a>Cómo cargar los registros de cliente?

La aplicación cliente AltspaceVR mantiene un registro de los datos de diagnóstico y los eventos que se producen mientras se usa AltspaceVR. En el transcurso de la solución de problemas, es posible que se le pida que "cargue los registros" para que nuestro equipo pueda revisarlos. Se trata de una característica de AltspaceVR que le permite enviar a nuestro equipo el contenido del registro local para ayudarnos a solucionar el problema.

### <a name="in-altspacevr"></a>En AltspaceVR

Para cargar los registros de cliente en AltspaceVR, vaya al menú **de** configuración y **seleccione Soporte técnico** en la barra de navegación izquierda. Aquí hay varias opciones para cargar registros, como se muestra en la captura de pantalla siguiente.

![Configuración con el panel de soporte técnico abierto y los campos de registro resaltados](images/help-altvr-uploadlogs.png)

### <a name="fields"></a>Campos

**"¿Qué ha ido mal?"**
Describa lo que ha ocurrido; por ejemplo, si encuentra un error, describa lo que esperaba que ocurriera a diferencia de lo que realmente ha sucedido. Esta información se enviará junto con el registro al presionar cargar.

**"Upload registros"** Este botón cargará los registros de la sesión actual. Use esta opción si encuentra un problema en esta misma sesión (por ejemplo, si no ha cerrado el cliente AltspaceVR) y desea notificarlo.

**"Upload últimos registros"** Este botón cargará los registros de la sesión anterior.

**"Upload último registro de bloqueo"** Este botón cargará más contenido de registro desde el último bloqueo que ha experimentado.

### <a name="in-client-logs"></a>En los registros de cliente

También puede recuperar los archivos de registro del equipo. Puede encontrar instrucciones sobre cómo recuperar estos registros [aquí.](#app-version-in-client-logs)


Una vez que haya encontrado esos archivos, abra una vale [de soporte técnico](https://help.altvr.com/hc/en-us/requests/new) y cargue los registros en la solicitud de vale antes de hacer clic en Enviar.

## <a name="what-do-i-do-if-i-cant-launch-altspacevr"></a>¿Qué debo hacer si no puedo iniciar AltspaceVR?

Hay varias razones por las que Es posible que AltspaceVR no se inicie por usted. Pruebe los pasos siguientes para asegurarse de que la aplicación está instalada correctamente con el software de terceros necesario.

### <a name="if-youre-trying-to-launch-altspacevr-for-the-first-time"></a>Si intenta iniciar AltspaceVR por primera vez:

1. Compruebe que el dispositivo es compatible y cumple los [requisitos mínimos especificados.](../getting-started/system-requirements.md)
2. Asegúrese de que tiene instalada la versión más reciente de [Oculus Software](https://www.oculus.com/setup) y de que Configuración-> general-> Dispositivos desconocidos está establecido en ON. Si se inicia en modo 2D, no es necesario que Oculus esté instalado.
3. Asegúrese de que tiene una conexión a Internet en funcionamiento. Si intenta iniciar Altspace desde un firewall de red, abra los puertos UDP 5055 y 5056 y los puertos TCP 80 y 443. Si se encuentra dentro de la red de un firewall corporativo o educativo, es posible que tenga que ponerse en contacto con el administrador de red o el departamento de TI.
4. Consulte también:
    * [Instalación de AltspaceVR para Oculus Quest](../getting-started/oculus-installation.md)
    * [Instalación de AltspaceVR para Windows Mixed Reality](../getting-started/wmr-installation.md)

### <a name="if-altspacevr-reports-that-the-current-version-is-out-of-date"></a>Si AltspaceVR informa de que la versión actual no está actualizada:

* Ya no se admite la versión de la aplicación que está usando. Si descargó AltspaceVR a través de un escaparate, es posible que la actualización se haya iniciado recientemente antes de que la tienda pueda actualizar el cliente.
* Si desea forzar la actualización, puede hacerlo a través de los distintos escaparates:
    * **Microsoft Store: Microsoft Store** [de aplicaciones: obtener actualizaciones para aplicaciones y juegos en Microsoft Store](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f)
    * **Oculus:** Abra la biblioteca de Oculus y vaya a "Actualizaciones" en la barra de navegación izquierda.
    * **Steam: compatibilidad** [con Steam: actualización de & instalación](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

### <a name="if-the-program-was-working-but-ceased-to-launch-after-update"></a>Si el programa funcionaba, pero dejó de iniciarse después de la actualización:

* Realice una "Reinstalación limpia" del software. Esto requiere que desinstale o quite las versiones existentes de la aplicación. Una vez que se haya quitado por completo del sistema, instale Altspace a través de Steam, Oculus o Microsoft Store.
* Si tiene algún problema al iniciar AltspaceVR, háganoslo saber a través de una [vale de soporte técnico.](https://help.altvr.com/hc/requests/new) Incluya un [archivo de registro](altspacevr-app-faq.md#how-do-i-upload-my-client-logs) de la sesión.

### <a name="if-altspacevr-fails-to-launch-after-customizing-your-home-space"></a>Si AltspaceVR no se inicia después de personalizar el espacio principal:

* Vaya al sitio [web del espacio principal.](https://account.altvr.com/users/sign_in)
* Compruebe que la plantilla del mundo todavía existe. Si la plantilla se ha compartido con usted, es posible que el propietario la haya eliminado, lo que provocaría que el espacio principal no se cargara.
    * Si se ha eliminado la plantilla, basta con "Editar" el mundo en el panel izquierdo "World Tools", reemplazar la plantilla existente por otra plantilla y "Actualizar" para guardar los cambios.
* Quite los objetos que puedan no cargarse seleccionando "Objetos" en el panel izquierdo "World Tools". Los objetos problemáticos pueden incluir:
    * Objetos de kits eliminados o objetos eliminados de kits que todavía están presentes en su mundo.
    * GLTFs experimentales.
* Después de abordar los elementos anteriores, intente volver a escribir AltspaceVR.

Puede encontrar compatibilidad más avanzada con los administradores de red o los departamentos de TI, incluidos los intervalos ip de Azure y las etiquetas de servicio, en nuestros detalles [de descarga.](https://www.microsoft.com/en-us/download/details.aspx?id=56519)

## <a name="support"></a>Soporte técnico

¿Preguntas o comentarios del equipo de AltspaceVR? 

> [!div class="nextstepaction"]
> [Haga clic aquí para enviar una solicitud de soporte técnico.](https://help.altvr.com/hc/requests/new)