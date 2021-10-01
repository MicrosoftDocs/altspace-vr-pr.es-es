---
title: Preguntas más frecuentes sobre el audio altspaceVR
description: Solución de problemas y compatibilidad con problemas relacionados con el audio.
ms.date: 8/23/2021
author: qianw211
ms.author: v-qianwen
ms.topic: article
keywords: vr, audio, solución de problemas, soporte técnico
ms.openlocfilehash: 05c8a477b9e50b5067e62b934fe2ff8bd656f06c
ms.sourcegitcommit: 5c452a9092297c0bfbc8efabebf395e7ee31853f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2021
ms.locfileid: "129311905"
---
# <a name="frequently-asked-questions-about-audio"></a>Preguntas más frecuentes sobre audio

## <a name="does-my-vr-headset-have-a-built-in-mic"></a>¿Mi casco de realidad virtual tiene un micrófono integrado?

### <a name="oculus-riftrift-s-oculus-questquest-2-windows-mixed-reality-and-htc-vive"></a>OculusThusTheso s, Oculus Quest/Quest 2, Windows Mixed Reality y ASÍNCULO

Sí, estos cascos vr tienen micrófonos integrados.

### <a name="windows"></a>Windows

En el caso de los cascos Windows, debería poder encontrar  el micrófono que aparece en los dispositivos de grabación mientras tiene el casco conectado.

### <a name="further-troubleshooting"></a>Solución de problemas adicional

* [Compatibilidad con AltspaceVR: otros usuarios no pueden escucharme](#what-do-i-do-if-other-users-cant-hear-me)
* [Compatibilidad con AltspaceVR: administración de permisos para Oculus Quest](../getting-started/oculus-controls.md#managing-permissions)

## <a name="is-there-a-push-to-talk-button"></a>¿Hay un botón de pulsar para hablar?

No hay ningún botón de inserción para hablar.  Si mira a la parte inferior izquierda de la vista, hay un icono de micrófono que se puede usar para alternar la voz. Como alternativa, puede usar el método abreviado de teclado Barra espaciadoa para silenciar o desactivar el micrófono.

Si el icono parpadea al hablar, el micrófono funciona.
 
## <a name="what-do-i-do-if-my-audio-is-choppy"></a>¿Qué debo hacer si el audio es descuado?

Algunos usuarios han observado que, cuando otro avatar habla, el audio aparece como descuido o con abandonos normales. En otras instancias, otros usuarios pueden informar a los usuarios de que su propio audio llega a través de un sonido toráctico o robotizado.

Lo primero que hay que intentar es volver a escribir siempre el espacio en el que se encuentra o incluso reiniciar AltspaceVR si se produce un error. Los problemas de audio no son comunes, pero cuando se producen esto suele ser una corrección sencilla. 

Si se produce un error, estas son algunas otras cosas, puede investigar:

#### <a name="cpu-performance-for-desktop-users"></a>Rendimiento de CPU para usuarios de escritorio

Revise nuestras [especificaciones recomendadas del sistema](../getting-started/system-requirements.md) para el hardware que se recomienda para ejecutar AltspaceVR. Hemos descubierto que las CPU i3 o inferiores provocan problemas no solo con las velocidades de fotogramas del vídeo, sino que pueden contribuir a problemas de audio, como abandonos y baja calidad.

#### <a name="internet-bandwidth-and-network-connection"></a>Ancho de banda de Internet y conexión de red

Los usuarios con conexiones lentas a Internet (menos de 5 Mbps) o en Wi-Fi pueden tener problemas de audio, como entregas. Se recomienda la conexión de línea dura de un cable Ethernet al equipo y una conexión más rápida de 5 Mbps. Es posible que quiera salir de cualquier programa que pueda estar usando la conectividad a Internet en segundo plano.

## <a name="what-do-i-do-if-other-users-cant-hear-me"></a>¿Qué debo hacer si otros usuarios no pueden escucharme?

En primer lugar, determine si AltspaceVR detecta el audio del micrófono. Puede determinarlo si el icono de micrófono de la parte inferior izquierda de la vista parpadea cuando está hablando. Si el icono parpadea al hablar, el micrófono funciona. Si el icono es rojo, está silenciado. Seleccione el icono para silenciar o desenmuesar usted mismo.

Si no ve el icono del micrófono parpadeando después de unmuting, es posible que tenga que ajustar la configuración del micrófono en AltspaceVR, vaya a Menú/ Configuración / Audio / Audio Input Selection (Selección de entrada de audio/ audio). A continuación, use los botones de flecha para seleccionar el micrófono que quiere usar.
 
### <a name="oculus-questquest-2"></a>Oculus Quest/Quest 2

Asegúrese de conceder permisos para usar el audio mic al instalar AltspaceVR. Otra comprobación que puede hacer es buscar en: Menú / Configuración / Audio / Selección de entrada de audio y asegurarse de que está establecido en entrada de audio de Android, que es el micrófono predeterminado de La misión/Misión2.
 
### <a name="windows-mixed-reality-oculus-riftrift-s-htc-vive-or-2d-mode"></a>Windows Mixed Reality, Oculus Sesos/ÁnimaS, NID Vive o Modo 2D

Asegúrese de que tiene la configuración correcta del micrófono en AltspaceVR: Menú / Configuración / Audio / Selección de entrada de audio. A continuación, use los botones de flecha para seleccionar el micrófono que quiere usar.

Antes de iniciar AltspaceVR, asegúrese de que el micrófono adecuado esté establecido como el dispositivo de grabación predeterminado en Windows. Oculus Dimensional/Dimensional S y CTRL Vive tienen un micrófono integrado, si tiene otro micrófono conectado en AltspaceVR puede estar intentando usar ese dispositivo.
 
Para cambiar el dispositivo de grabación predeterminado en Windows:

* Haga clic con el botón derecho en el icono del hablante Windows seleccione **Abrir configuración de sonido.**
* Vaya a la **lista desplegable Entrada/Elija** el dispositivo de entrada.
* Elija el micrófono que desea usar en el menú desplegable: 
    * El micrófono de LANS vive se **etiquetará como Micrófono: dispositivo de audio USB.**
    * El micrófono Oculus Microphone se etiquetará **como Headset Microphone (Oculus Virtual Audio Device)**(Micrófono de casco [dispositivo de audio virtual de Oculus]).
* Después de reiniciar AltspaceVR, ahora se seleccionará el micrófono.
 
Si después de seguir estos pasos sigue teniendo problemas, las cosas que pueden afectar a usted pueden ser:

* Si no Alt-Tab más de 30 segundos, AltspaceVR le silenciará automáticamente. Puede deshabilitarlo en **Menú -> Configuración -> Audio -> Mute cuando AltspaceVR está inactivo.**
* El sistema de audio AltspaceVR tiene un umbral de volumen que puede estar por debajo. Establezca los niveles de micrófono en max, establezca el micrófono más cerca de la sensibilidad y hable en el volumen normal.
* Salga de VR e intente conectar el cable USB del casco a un puerto USB 3.0 alternativo. En nuestra experiencia, algunos puertos USB 3.0 provocan problemas.

Es posible que AltspaceVR no reconozca los cambios de configuración de sonido realizados durante el juego, por lo que es posible que tenga que reiniciar AltspaceVR para que los cambios de micrófono anteriores suenen efecto.  Cuando vuelva a entrar en el juego, mire el icono del micrófono y vea si parpadea al hablar. Si el icono parpadea, el micrófono funciona.

## <a name="support"></a>Soporte técnico

¿Preguntas o comentarios del equipo de AltspaceVR? 

> [!div class="nextstepaction"]
> [Haga clic aquí para enviar una solicitud de soporte técnico.](https://help.altvr.com/hc/requests/new)