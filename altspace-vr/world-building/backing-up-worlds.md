---
title: Realización de una copia de seguridad de los mundos
description: Aprenda a crear, administrar y solucionar problemas de instantáneas de copia de seguridad de los mundos altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: guardar
ms.openlocfilehash: 2f4f232fd843b612563b2d7425de2b5d17720c539cc02a1493bc4b118de4f117
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125479"
---
# <a name="backing-up-your-worlds"></a>Realización de una copia de seguridad de los mundos

Una copia de seguridad es una "instantánea" o un registro de todos los objetos de un mundo en un momento específico en el tiempo. Imagine que va a crear la casa de los veranos y que un día eliminó accidentalmente la sala de estar. Si había creado una copia de seguridad de su mundo el día anterior, podría restaurar esa copia de seguridad en particular, restablecer el mundo y evitar un ataque de miedo. O quizás tenga una versión de la cocina de cada estación y le gustaría cambiar de una a otra: puede hacerlo con copias de seguridad. Cada copia de seguridad es específica de un único mundo y contiene no solo las transformaciones (posición, rotación, escala), sino también otras configuraciones de los objetos. No hay ningún límite en el número de copias de seguridad que puede crear para un mundo.  

## <a name="whats-included-in-a-backup"></a>¿Qué se incluye en una copia de seguridad?

Actualmente, una copia de seguridad incluye la mayoría de las cosas que puede generar con el Editor del mundo:
* Artifacts (objetos kit)
* Etiquetas
* Teletransportadores
* Puntos de generación
* Fotos
* Aplicaciones del SDK de MRE
* Aplicaciones nativas (por ejemplo, Hologramas Contra la realidad)

No se incluye lo siguiente:

* Invalidaciones de diseño
* Skyboxes y sonido ambiente
* Plantillas
* Instructions
* Roles del mundo y roles contextuales

## <a name="managing-backups"></a>Administrar copias de seguridad

Para crear una copia de seguridad, abra el Editor del mundo o Altspace y haga clic en "Copias de seguridad". El primer botón será el botón "Nueva copia de seguridad". Al crear una copia de seguridad, se le pedirá que proporcione un nombre corto. Esto es opcional, pero muy recomendable, ya que se volverá confuso rápidamente. Las copias de seguridad existentes aparecerán después del botón "Crear". Al hacer clic en una copia de seguridad existente, se iniciará una restauración. Al restaurar una copia de seguridad, el mundo se restablecerá transcurridos unos instantes, pero es posible que no vea los cambios reflejados. Espere uno o dos minutos y vuelva a restablecer el mundo. **Actualmente no hay ninguna manera de editar o eliminar una copia de seguridad en VR.** Por ahora, deberá administrar las copias de seguridad en nuestro sitio web. (La administración de copias de seguridad en VR se mejorará pronto. Mientras tanto, óngase con nosotros).

Para administrar las copias de seguridad en nuestro sitio web:

1. Vaya a [Worlds > Mine,](https://account.altvr.com/users/sign_in)busque su mundo y presione "Copias de seguridad" en los controles de administrador:

![Controles de administrador en el sitio web de worlds con el panel de copias de seguridad abierto](images/world-backup-img-01.png)

2. Puede crear, editar y eliminar las copias de seguridad, comprobar cuántos objetos hay dentro e incluso cargar una imagen de vista previa: 

![Ventana Copias de seguridad con comandos de creación, edición y eliminación resaltados](images/world-backup-img-02.png)

No hay ningún límite en el número de copias de seguridad y tener más copias de seguridad no afectará al rendimiento de su mundo.

## <a name="other-ways-to-back-up-your-worlds"></a>Otras formas de hacer una copia de seguridad de los mundos

* Crear otro mundo, Mostrar opciones avanzadas e Importar desde el mundo. Elija el mundo del que desea hacer una copia de seguridad en el menú desplegable en el nuevo. No hay ningún límite para las importaciones.
* Si usa el uploader de Unity, se recomienda encarecidamente usar el control de versiones. Por ejemplo, [GitHub para Unity.](https://unity.github.com)

## <a name="troubleshooting"></a>Solución de problemas

**Ayuda. He restaurado accidentalmente una copia de seguridad y mi trabajo ha desaparecido,** no se preocupe. Creamos automáticamente una nueva copia de seguridad antes de restaurar la anterior. Busque uno con un nombre que comience por **Auto** con la marca de tiempo correcta y restáurelo (por ejemplo, **Auto 2019-01-14T08:23:33-08:00**).  Si eso no funciona, envíe [un](https://help.altvr.com/hc/requests/new) Support Request

**He restaurado una copia de seguridad y faltan algunos objetos** Si alguna fuera fotos, ¿se eliminaron esas fotos? No se pueden restaurar las fotos eliminadas por motivos de privacidad. Enviar una [Support Request](https://help.altvr.com/hc/requests/new) para que podamos investigar

**No veo ningún cambio** Las copias de seguridad se restauran de forma asincrónica, lo que significa que pueden tardar unos minutos en restaurarse en función del número de objetos. No olvide restablecer el mundo y, si no ve nada después de unos minutos, intente restablecerlo de nuevo. En el futuro, podemos proporcionar más comentarios sobre el estado del proceso de restauración.