---
title: No puedo iniciar AltspaceVR
description: Obtenga información sobre cómo identificar, notificar y corregir cualquier problema relacionado con el inicio del entorno altspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: faq
ms.openlocfilehash: 50edddef669aca14640fd6e910c12c15864cf46a099e54bceed40494e9817de4
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127936"
---
# <a name="i-cant-launch-altspacevr"></a>No puedo iniciar AltspaceVR

Existen varias razones por las que Es posible que AltspaceVR no se inicie por usted. Pruebe los pasos siguientes para asegurarse de que la aplicación está instalada correctamente con el software de terceros necesario.

## <a name="if-youre-trying-to-launch-altspacevr-for-the-first-time"></a>Si intenta iniciar AltspaceVR por primera vez:

1. Compruebe que el dispositivo es compatible y cumple los [requisitos mínimos especificados.](../getting-started/system-requirements.md)
2. Asegúrese de que tiene instalado el [software de Oculus](https://www.oculus.com/setup) más reciente y de que Configuración-> General-> Desconocidos está establecido en ON. Si se inicia en modo 2D, no es necesario que esté instalado Oculus.
3. Asegúrese de que tiene una conexión a Internet en funcionamiento. Si está intentando iniciar Altspace desde un firewall de red, abra los puertos UDP 5055 y 5056 y los puertos TCP 80 y 443. Si está dentro de la red de un firewall corporativo o educativo, es posible que tenga que ponerse en contacto con el administrador de red o el departamento de TI.
4. Consulte también:
    * [Instalación de AltspaceVR para Oculus Quest](../getting-started/oculus-installation.md)
    * [Instalación de AltspaceVR para Windows Mixed Reality](../getting-started/wmr-installation.md)

## <a name="if-altspacevr-reports-that-the-current-version-is-out-of-date"></a>Si AltspaceVR informa de que la versión actual no está actualizada:

* La versión de la aplicación que usa ya no se admite. Si descargó AltspaceVR a través de un escaparate, es posible que la actualización se haya iniciado recientemente antes de que la tienda pueda actualizar el cliente.
* Si desea forzar la actualización, puede hacerlo a través de los distintos escaparates:
    * **Microsoft Store: Microsoft Store** [soporte técnico: obtener actualizaciones](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f) para aplicaciones y juegos en Microsoft Store
    * **Oculus:** Abra la biblioteca de Oculus y vaya a "Actualizaciones" en la barra de navegación izquierda.
    * **Steam: compatibilidad** [con Steam: actualización de & de instalación](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

## <a name="if-the-program-was-working-but-ceased-to-launch-after-update"></a>Si el programa funcionaba, pero dejó de iniciarse después de la actualización:

* Realice una "Limpieza de la reinstalación" del software. Esto requiere que desinstale o quite las versiones existentes de la aplicación. Una vez que se haya quitado por completo del sistema, instale Altspace a través de Steam, Oculus o Microsoft Store.
* Si tiene algún problema al iniciar AltspaceVR, háganoslo saber a través de una vale [de soporte técnico.](https://help.altvr.com/hc/requests/new) Incluya un [archivo de registro](uploading-client-logs.md) de la sesión.

## <a name="if-altspacevr-fails-to-launch-after-customizing-your-home-space"></a>Si AltspaceVR no se inicia después de personalizar el espacio principal:

* Vaya al sitio [web del espacio principal.](https://account.altvr.com/users/sign_in)
* Compruebe que la plantilla del mundo todavía existe. Si la plantilla se ha compartido con usted, es posible que el propietario la haya eliminado, lo que provocaría que el espacio de inicio no se cargara.
    * Si se ha eliminado la plantilla, simplemente "Editar" el mundo en el panel izquierdo "Herramientas del mundo", reemplace la plantilla existente por otra plantilla y "Actualizar" para guardar los cambios.
* Quite todos los objetos que puedan no cargarse; para ello, seleccione "Objetos" en el panel izquierdo "Herramientas del mundo". Los objetos problemáticos pueden incluir:
    * Objetos de kits eliminados o objetos eliminados de los kits que todavía están presentes en su mundo.
    * GLTFs experimentales.
* Después de abordar los elementos anteriores, intente volver a escribir AltspaceVR.

Puede encontrar compatibilidad más avanzada con los administradores de red o los departamentos de TI, incluidos los intervalos IP de Azure y las etiquetas de servicio, en nuestros detalles [de descarga.](https://www.microsoft.com/en-us/download/details.aspx?id=56519)