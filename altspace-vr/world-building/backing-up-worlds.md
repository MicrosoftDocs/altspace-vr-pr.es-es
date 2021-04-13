---
title: Realización de copias de seguridad de los mundos
description: Aprenda a crear, administrar y solucionar problemas de las instantáneas de copia de seguridad de sus AltspaceVR mundos.
ms.date: 03/11/2021
ms.topic: article
keywords: guardar
ms.openlocfilehash: fdef692c737bf2f92db315e04556831d60c2f377
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213657"
---
# <a name="backing-up-your-worlds"></a>Realización de copias de seguridad de los mundos

Una copia de seguridad es una "instantánea" o un registro de todos los objetos de un mundo en un momento dado. Supongamos que está creando su casa de sueño y un día que ha eliminado accidentalmente el salón. Si ha creado una copia de seguridad de su mundo el día anterior, puede restaurar esa copia de seguridad concreta, restablecer su mundo y evitar un ataque de pánico. O quizás tenga una versión de su cabina en el medio para cada temporada y desea cambiar de una a otra, puede hacerlo con copias de seguridad de la misma manera. Cada copia de seguridad es específica de un solo mundo y contiene no solo las transformaciones (posición, rotación, escala), sino también otras opciones de los objetos. No hay ningún límite en el número de copias de seguridad que puede crear para un mundo.  

## <a name="whats-included-in-a-backup"></a>¿Qué se incluye en una copia de seguridad?

Actualmente, una copia de seguridad incluye la mayoría de las cosas que puede generar con el editor mundial:
* Artefactos (objetos del kit)
* Etiquetas
* Teletransportadores
* Puntos de generación
* Fotos
* Aplicaciones de SDK de MRE
* Aplicaciones nativas (por ejemplo, hologramas en realidad)

No se incluye lo siguiente:

* Invalidaciones de diseño
* Skyboxes y sonido ambiente
* Plantillas
* Instrucciones
* Roles del mundo y roles contextuales

## <a name="managing-backups"></a>Administrar copias de seguridad

Para crear una copia de seguridad, abra el editor del mundo/Altspace y haga clic en "copias de seguridad". El primer botón será el botón "nueva copia de seguridad". Al crear una copia de seguridad, se le pedirá que proporcione un nombre corto. Esto es opcional, pero se recomienda encarecidamente porque se verá confuso. Las copias de seguridad existentes se mostrarán después del botón "crear". Al hacer clic en una copia de seguridad existente se iniciará una restauración. Al restaurar una copia de seguridad, su mundo se restablecerá transcurridos unos minutos, pero es posible que no vea los cambios reflejados. Espere un minuto o dos y vuelva a restablecer su mundo. **Actualmente no hay ninguna manera de editar o eliminar una copia de seguridad en VR**. Tendrá que administrar las copias de seguridad en nuestro sitio web por ahora. (La administración de copias de seguridad en VR se mejorará pronto. Mientras tanto, lleve con nosotros).

Para administrar las copias de seguridad en nuestro sitio web:

1. Vaya a [mundos > mina](https://account.altvr.com/users/sign_in), busque su mundo y presione "copias de seguridad" en los controles de administrador:

![Controles de administrador en el sitio web de mundos con el panel copias de seguridad abierto](images/world-backup-img-01.png)

2. Puede crear, editar y eliminar las copias de seguridad, comprobar cuántos objetos hay dentro e incluso cargar una imagen de vista previa: 

![Ventana copias de seguridad con los comandos crear, editar y eliminar resaltados](images/world-backup-img-02.png)

No hay ningún límite en el número de copias de seguridad y tener más copias de seguridad no afectará al rendimiento de su mundo.

## <a name="other-ways-to-back-up-your-worlds"></a>Otras maneras de realizar copias de seguridad de los mundos

* Cree otro mundo, muestre opciones avanzadas e importe desde el mundo. Elija el mundo del que desea realizar una copia de seguridad en el menú desplegable en el nuevo. No hay límite para las importaciones.
* Si usa el cargador de Unity, le recomendamos encarecidamente que use el control de versiones. Por ejemplo, [GitHub para Unity](https://unity.github.com).

## <a name="troubleshooting"></a>Solución de problemas

**Ayuda. He restaurado accidentalmente una copia de seguridad y mi trabajo ya no se** preocupe. Se creará automáticamente una nueva copia de seguridad antes de restaurar una anterior. Busque una con un nombre que empiece por **auto** con la marca de tiempo correcta y restáurela (por ejemplo, **auto 2019-01-14T08:23:33-08:00**).  Si eso no funciona, envíe un [support request](https://help.altvr.com/hc/requests/new)

**He restaurado una copia de seguridad y faltan algunos objetos** Si alguna vez se tratara de fotografías, ¿se eliminaron esas fotos? No se pueden restaurar las fotos eliminadas por motivos de privacidad. Enviar una [support request](https://help.altvr.com/hc/requests/new) para que podamos investigar

**No veo ningún cambio** Las copias de seguridad se restauran de forma asincrónica, lo que significa que pueden tardar unos minutos en restaurarse en función del número de objetos. Recuerde restablecer su mundo y, si no ve nada después de unos minutos, intente volver a restablecerlo. En el futuro, podemos proporcionar más información sobre el estado del proceso de restauración.