---
title: Otros usuarios no me oyen
description: Obtenga información acerca de cómo identificar y corregir problemas relacionados con otros usuarios que no pueden escucharme en AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: faq
ms.openlocfilehash: b6248e46b62e1a29324e831e686aee7b1de4505a
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213830"
---
# <a name="other-users-cant-hear-me"></a>Otros usuarios no me oyen

En primer lugar, determine si AltspaceVR está detectando el audio desde el micrófono. Puede determinar si el icono del micrófono en la parte inferior izquierda de la vista parpadea cuando está hablando. Si el icono parpadea al hablar, el micrófono funciona. Si el icono está en rojo, está silenciado. Seleccione el icono para silenciar o desactivarse.

Si no ve el icono del micrófono parpadeando después de deshacer el silenciado, puede que necesite ajustar la configuración del micrófono en AltspaceVR, ir a menú/configuración/audio/audio selección de entrada. A continuación, use los botones de flecha para seleccionar el micrófono que le gustaría usar.
 
## <a name="oculus-quest"></a>Oculus Quest 

Asegúrese de conceder permisos para usar el audio MIC al instalar AltspaceVR. Otra comprobación que puede realizar es buscar en la entrada de menú/configuración/audio/audio y asegurarse de que está establecida en entrada de audio de Android (es decir, el micrófono predeterminado de Quest/Quest2's).
 
## <a name="windows-mixed-reality-oculus-rift-htc-vive-or-2d-mode"></a>Windows Mixed Reality, Oculus Rift, HTC Naopak o 2D

Asegúrese de que tiene la configuración de micrófono correcta en AltspaceVR: menú/configuración/selección de entrada de audio/audio. A continuación, use los botones de flecha para seleccionar el micrófono que le gustaría usar.

Antes de iniciar AltspaceVR, asegúrese de que el micrófono adecuado se establece como el dispositivo de grabación predeterminado en Windows. Los Oculus Rift y HTC Naopak tienen un micrófono integrado, si tiene otro micrófono conectado en AltspaceVR puede estar intentando usar ese dispositivo.
 
Para cambiar el dispositivo de grabación predeterminado en Windows:
* Haga clic con el botón derecho en el icono de altavoz en Windows y seleccione **dispositivos de reproducción** .
* Vaya a la pestaña **grabación**
* Busque el micrófono que le gustaría usar. El micrófono HTC Naopak se etiquetará como **dispositivo de audio USB de micrófono** y el micrófono Oculus Rift se etiquetará como **micrófono-Rift audio**.
* Haga clic con el botón derecho en el micrófono y seleccione **establecer como dispositivo predeterminado** .
* Después de reiniciar AltspaceVR, ahora se seleccionará el micrófono.
 
Si después de seguir estos pasos sigue teniendo problemas, hay algunos otros problemas que pueden estar afectando a usted:
* Si Alt-Tab fuera de más de 30 segundos, AltspaceVR lo silenciará automáticamente; puede deshabilitarlo mediante el uso del método abreviado de teclado: barra espaciadora para activar o desactivar silenciar.
* El sistema de audio AltspaceVR tiene un umbral de volumen que puede encontrarse a continuación. Establezca los niveles de MIC en Max, establezca el micrófono más cerca de la boca y hable en el volumen normal.
* Salga de VR, conecte el cable USB desde los auriculares a un puerto USB 3,0 alternativo. En nuestra experiencia, algunos puertos USB 3,0 causan problemas.

Es posible que AltspaceVR no reconozca los cambios de configuración de sonido realizados durante el juego, por lo que es posible que tenga que reiniciar el AltspaceVR de los cambios de micrófono anteriores para que surtan efecto.  Cuando vuelva a entrar en el juego, mire el icono del micrófono y compruebe si parpadea. Si el icono parpadea, el micrófono funciona.