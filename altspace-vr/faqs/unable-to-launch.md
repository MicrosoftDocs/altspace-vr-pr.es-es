---
title: No puedo iniciar AltspaceVR
description: Obtenga información acerca de cómo identificar, informar y corregir los problemas relacionados con el inicio del entorno de AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: faq
ms.openlocfilehash: fc49b5b7ed708e43a12616d782a397a364b2264e
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213765"
---
# <a name="i-cant-launch-altspacevr"></a>No puedo iniciar AltspaceVR

Hay varias razones por las que AltspaceVR no puede iniciarse automáticamente. Pruebe los pasos siguientes para asegurarse de que la aplicación se instala correctamente con el software de terceros necesario.

## <a name="if-youre-trying-to-launch-altspacevr-for-the-first-time"></a>Si está intentando iniciar AltspaceVR por primera vez:

1. Compruebe que el dispositivo es compatible y cumple los [requisitos mínimos especificados](../getting-started/system-requirements.md).
2. Asegúrese de que tiene instalado el [software de Oculus](https://www.oculus.com/setup) más reciente y que la configuración > General-> dispositivos desconocidos esté establecida en activado. Si se inicia en modo 2D, no es necesario que Oculus esté instalado.
3. Asegúrese de que tiene una conexión a Internet que funciona. Si está intentando iniciar Altspace desde dentro de un firewall de red, abra los puertos UDP 5055 y 5056, y los puertos TCP 80 y 443. Si se encuentra en la red de un Firewall corporativo o educativo, es posible que deba ponerse en contacto con el administrador de red o el Departamento de ti.
4. Consulte también:
    * [Instalación de AltspaceVR para Oculus Quest](../getting-started/oculus-installation.md)
    * [Instalación de AltspaceVR para Windows Mixed Reality](../getting-started/wmr-installation.md)

## <a name="if-altspacevr-reports-that-the-current-version-is-out-of-date"></a>Si AltspaceVR informa de que la versión actual no está actualizada:

* La versión de la aplicación que está usando ya no se admite. Si descargó AltspaceVR a través de un escaparate, es posible que la actualización se haya iniciado recientemente antes de que el almacén pudiera actualizar el cliente.
* Si desea forzar la actualización, puede hacerlo a través de los distintos escaparates:
    * **Microsoft Store:** [compatibilidad de Microsoft Store-obtener actualizaciones para aplicaciones y juegos en Microsoft Store](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f)
    * **Oculus:** Abra la biblioteca de Oculus y vaya a "actualizaciones" en la barra de navegación izquierda.
    * **Vapor:** [compatibilidad con vapor: actualización & problemas de instalación](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

## <a name="if-the-program-was-working-but-ceased-to-launch-after-update"></a>Si el programa estaba funcionando, pero dejó de iniciarse después de la actualización:

* Realice una reinstalación limpia del software. Esto requiere la desinstalación o eliminación de las versiones existentes de la aplicación. Una vez que se haya quitado completamente del sistema, instale Altspace a través de vapor, Oculus o Microsoft Store.
* Si tiene un problema al iniciar AltspaceVR, háganoslo saber a través de una [incidencia de soporte técnico](https://help.altvr.com/hc/requests/new). Incluya un [archivo de registro](uploading-client-logs.md) de la sesión.

## <a name="if-altspacevr-fails-to-launch-after-customizing-your-home-space"></a>Si AltspaceVR no se puede iniciar después de personalizar el espacio de Inicio:

* Vaya al [sitio web del espacio de inicio](https://account.altvr.com/users/sign_in).
* Compruebe que la plantilla del mundo sigue existiendo. Si la plantilla se ha compartido con usted, es posible que la haya eliminado el propietario, lo que provocaría un error en la carga del espacio de inicio.
    * Si la plantilla se ha eliminado, simplemente edite el mundo en el panel izquierdo ' herramientas del mundo ', reemplace la plantilla existente por otra y ' update ' para guardar los cambios.
* Quite todos los objetos que no se puedan cargar; para ello, seleccione ' objetos ' en el panel izquierdo ' herramientas del mundo '. Los objetos problemáticos pueden incluir:
    * Objetos de kits eliminados u objetos eliminados de los kits que todavía están presentes en su mundo.
    * GLTFs experimental.
* Después de direccionar los elementos anteriores, intente volver a escribir AltspaceVR.

La compatibilidad más avanzada con los administradores de red o los departamentos de ti, incluidos los intervalos IP de Azure y las etiquetas de servicio, se puede encontrar en nuestros detalles de la [descarga](https://www.microsoft.com/en-us/download/details.aspx?id=56519).