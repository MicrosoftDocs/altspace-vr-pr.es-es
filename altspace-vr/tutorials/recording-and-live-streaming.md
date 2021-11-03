---
title: Grabación y streaming en vivo
description: Obtenga información sobre cómo grabar y transmitir en vivo los eventos AltspaceVR desde el equipo para promocionar y compartir con los usuarios.
author: qianw211
ms.author: v-qianwen
ms.date: 11/1/2021
ms.topic: article
keywords: streaming, grabación, vídeo, audio, youtube, obs, live
ms.openlocfilehash: e82960097103df25c50f0b03b76d21e10b1cbbd6
ms.sourcegitcommit: 20605c50a93852f93a3464c5c339f6a7da67a047
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2021
ms.locfileid: "131278986"
---
# <a name="recording-and-live-streaming"></a>Grabación y streaming en vivo

Grabar y transmitir en vivo la experiencia altspaceVR para mostrar a otros usuarios de todo el mundo es una excelente manera de promocionar el evento, AltspaceVR y VR en general. Echa un vistazo a continuación para ver cómo empezar.

En este artículo, aprenderá a:

* [Grabar AltspaceVR en modo 2D en pc](#recording-altspacevr-in-2d-mode-on-pc)
* [Streaming en vivo a YouTube en AltspaceVR en modo 2D en PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## <a name="recording-altspacevr-in-2d-mode-on-pc"></a>Grabación de AltspaceVR en modo 2D en pc

### <a name="the-short-version"></a>La versión corta

1. Tener Instalados AltspaceVR y OBS (Software Open Difuso). Inicie AltspaceVR en modo 2D, inicie OBS, configure OBS para grabar AltspaceVR y grabarlo.

### <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

1. Visite [https://obsproject.com/](https://obsproject.com/).
2. Seleccione **Windows** descargar OBS. Esta publicación usa **OBS v26.1.1**
3. Instalación de OBS

### <a name="have-altspacevr-running-before-you-run-obs"></a>Hacer que AltspaceVR se ejecute ANTES de ejecutar OBS

1. Descargue e instale AltspaceVR desde nuestro sitio web: [altvr.com/get](https://altvr.com/getaltspacevr)
2. Si quiere estabilizar el vídeo de realidad virtual y eliminar los movimientos de cabeza, asegúrese de usar el cliente 2D o inicie AltspaceVR en modo 2D desconectando el cable USB del casco del equipo. Si tiene un objeto Desenlazar, presione Ctrl+Alt+Supr, seleccione **Servicios**, Servicio en tiempo de ejecución **de Oculus VR,** haga clic con el botón derecho y **seleccione Detener**. Esto deshabilitará Oculus e iniciará AltspaceVR en modo 2D. Repita estos pasos y use Iniciar para volver a obtener el modo VR.
3. También puede grabar su experiencia en modo VR mediante Game Capture con OBS.

Ahora, Alt-Tab a OBS:

1. En **Escenas,** seleccione **+** y asigne un nombre a la nueva escena.
2. A continuación, **en Orígenes,** seleccione: **+ > Game Capture > Crear nuevo.**
2. Edite el texto a "AltspaceVR Capture", marque **Hacer visible el origen** y seleccione **Aceptar.**
3. Haga doble clic en **Altspace CaptureVR en** **Orígenes.**
4. Cambiar **el modo** a La ventana específica de **captura**
5. Ventana: [AltspaceVR.exe]: AltspaceVR
6. Prioridad de coincidencia de ventana: coincide con el título; de lo contrario, busque la ventana del mismo archivo ejecutable.
7. Desplácese hacia abajo hasta Capture Cursor : untick **(Cursor** de captura: untick)
8. Seleccione **Aceptar**.
9. Esto debería hacer que AltspaceVR se muestre en OBS.

Ahora, para establecer las siguientes propiedades en OBS, vaya **a Archivo > Configuración**:

|Pestaña|Configuración|
|---|---|
| **General** | Deje el valor predeterminado. |
| **Stream** | Deje el valor predeterminado. |
| **Salida** | Cambiar a Avanzado |
| **Pestaña -Streaming** | Pista de audio 1 <br> Codificador: x264 <br> Volver a escalar la salida: sin troncalar <br> Control de velocidad: CBR <br> Velocidad de bits: 6000 (6000 para 30 fps o 9000 para 60 fps) <br> Intervalo de fotogramas clave = 2 <br> Valor preestablecido de uso de CPU = muy rápido |
| **Pestaña -Recording (Grabación)** | Tipo: Estándar. <br> Ruta de acceso de grabación: D:/Video (Vaya a donde desea que se guarden los archivos de vídeo) <br> Formato de grabación: mp4 (si se produce algún bloqueo durante la grabación, pruebe aquí, en lugar de mp4, si se bloquea, el vídeo seguirá siendo utilizable con el disco). <br> Pista de audio 1 <br> Codificador: Uso del codificador de secuencia |
| **Pestaña -Audio** | Velocidad de bits de audio: 160 (para todas las pistas) |
| **Pestaña -Replay buffer (Búfer de reproducción)** | Deje el valor predeterminado. |
| **Audio** | Frecuencia de muestreo: 44,1 khz <br> Canales: Estéreo <br> Audio de escritorio: valor predeterminado <br> Audio de escritorio 2: Deshabilitar <br> Audio micrófono/auxiliar: valor predeterminado |
| **Vídeo** | Resolución base (lienzo): 1920 x 1080 <br> Resolución de salida (escalado): 1920 x 1080 <br> Filtro de escalabilidad vertical: bicúbica (escalado con aumento, 16 ejemplos) <br> Valores comunes de FPS: 30 (o 60) |
| **Teclas de acceso rápido** | Deje el valor predeterminado. |
| **Avanzadas** | Prioridad del proceso: Normal | <br>

<br>Ahora, asegúrese de seleccionar **Aplicar** y, a **continuación,** aceptar para guardar toda la configuración de OBS. 

1. Alt-Tab a AltspaceVR, entra en el espacio, el mundo o el evento correctos y alinea la cámara (es decir, tu Avatar), estamos a punto de grabar un vídeo.
2. Alt-Tab a OBS y, cuando esté listo, haga clic **en Iniciar grabación.**

Verá en la parte inferior derecha de OBS que **REC:** empezará a contar hacia arriba y el punto es rojo, lo que significa que está grabando.

Realice una grabación de prueba de esto: 
1. En AltspaceVR, abra, cierre o suba los menús para hacer sonidos de la interfaz de usuario.
2. Asegúrese de que no está conmutado, diga "Sibilance, Sibilance" u haga que otro usuario hable con usted en un volumen normal.
3. Mire los **niveles Audio de escritorio** y **Micrófono/Auxiliar** mientras lo hace para ver si está seleccionando el audio correctamente.

Normalmente se silencia el micrófono o auxiliar al grabar. Vaya y seleccione el icono del hablante para Mic/Aux y se volverá rojo con una X.

* Es muy difícil hacer coincidir los niveles de audio del micrófono con el audio del otro usuario, por lo que el micrófono se silencia mejor cuando se graba un evento.
* Otro problema con el audio es la forma en que se configura OBS. Captura TODO el audio del equipo, por lo que si está viendo YouTube u recibe sonidos de notificación en el equipo, grabará ese audio.
* Para grabar solo el audio desde AltspaceVR, vaya al mezclador Abrir volumen **(haga** clic con el botón derecho en el icono del hablante en la parte inferior derecha de Windows) y silencie los sonidos del sistema, los exploradores, y así sucesivamente, pero no mute OBS ni AltspaceVR.

> [IMPORTANTE] No olvide desenmuesar esta configuración del mezclador de volumen después de la grabación.

Ahora, vuelva a OBS y seleccione **Detener grabación.** Para encontrar el vídeo que acaba de grabar, vaya **a File>Show Recordings (Mostrar grabaciones).** Se abrirá la carpeta con los archivos de vídeo de OBS y se hace doble clic en el vídeo de prueba.

A veces, la grabación es bastante alta, así que reduzca el control deslizante de Audio de escritorio en OBS y realice otra grabación para probar.

Pro de texto: use Ctrl+Alt+P para activar el modo de fotografía; quitará la interfaz de usuario de la vista para obtener una buena imagen limpia.

Le complace que sea una grabadora de vídeo AltspaceVR.

## <a name="live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc"></a>Streaming en vivo a YouTube en modo AltspaceVR 2D en PC

### <a name="the-short-version"></a>La versión corta

Tener AltspaceVR y OBS instalados. Inicie AltspaceVR y OBS. Puede transmitir en vivo "Ahora mismo" o en una "Fecha posterior". En YouTube, configure OBS con la clave de secuencia de YouTube. Comience a transmitir en OBS y en YouTube, y ya va a las carreras.

### <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

Consulte la sección [Recording AltspaceVR in 2D mode on PC](#recording-altspacevr-in-2d-mode-on-pc) (Grabación de AltspaceVR en modo 2D en PC) en la parte superior de esta página para obtener instrucciones sobre cómo probar la grabación mediante una grabación local en lugar de la secuencia en directo y cómo configurar la toma de cámara.

## <a name="setting-up-live-streaming-on-youtube"></a>Configuración del streaming en vivo en YouTube

Puede obtener un streaming en directo que vaya a "Right Now" o configurar un streaming en directo futuro con "Fecha posterior".

1. Abra el explorador, inicie sesión [https://www.youtube.com/](https://www.youtube.com/) y, a continuación, vaya a [https://studio.youtube.com/](https://studio.youtube.com/)
2. Busque en la parte superior derecha y seleccione **CREAR y,** a **continuación, En directo.**

**Método "Ahora** mismo":

1. Seleccione **Right now /START (Ahora/ INICIAR).**
1. Seleccione **Software de streaming/GO.**
1. Elija **EDITAR,** en la parte superior derecha, para editar los detalles y personalizaciones del vídeo.
1. En **Stream Configuración**, mantenga los valores predeterminados.
1. Junto **a la tecla Stream (pegar en el codificador),** **copie** la clave para poder pegarla en OBS.
1. Abrir OBS/Configuración   /  **Stream**
1. En el **menú** desplegable Servicio, seleccione **YouTube - RTMPS.**
1. Pegue la clave stream de YouTube en el **campo Stream Key (Clave de** secuencia) en OBS.
1. Haga clic **en Aplicar** y, a **continuación, en Aceptar.**
1. Seleccione **Start Streaming** in OBS (Iniciar streaming en OBS).
1. Cambie a YouTube y verá que ahora está en directo en YouTube.
1. Para ver la página de vídeo real de YouTube Live Stream, deberá seleccionar el icono COMPARTIR en la parte superior derecha.
1. Haga clic en el "Vínculo de vídeo" y verá y escuchará la transmisión en vivo de YouTube. 
1. Esta dirección URL es el vínculo de streaming en vivo y se puede compartir con todos los canales de redes sociales :)
1. Para detener la transmisión en vivo, seleccione END STREAM on YouTube (END STREAM en YouTube) y Stop Streaming on OBS (Detener streaming en OBS).

'**Later date**' (Método):
1. En la parte superior izquierda, elija el **icono** Administrar.
1. Seleccione **SCHEDULE STREAM (PROGRAMAR FLUJO),** en la parte superior derecha.
1. Agregar título, descripción, categoría, miniatura (1280 x 720) y, a continuación, **siguiente**
1. Opciones de chat en directo y, a **continuación, SIGUIENTE**
1. Privado, No incluido en la lista o Público (elija Público)
1. Programe la fecha y hora en que desea que se haga la publicación y, a continuación, **LISTO.**

 **Cuando esté listo para iniciar la transmisión en vivo en el futuro:**
1. En Stream Configuración, mantenga los valores predeterminados.
1. Junto **a la tecla Stream (pegar en el codificador),** **copie** la clave para poder pegarla en OBS.
1. Abrir OBS/Configuración   /  **Stream**
* En el **menú** desplegable Servicio, seleccione **YouTube - RTMPS.**
1. Pegue la clave stream de YouTube en el **campo Stream Key (Clave de** secuencia) en OBS.
1. Haga clic **en Aplicar** y, a **continuación, en Aceptar.**
1. Seleccione **Start Streaming** in OBS (Iniciar streaming en OBS).
1. Cambie a YouTube y verá que ahora está en directo en YouTube.
1. Para ver la página de vídeo real de YouTube Live Stream, deberá seleccionar el icono COMPARTIR en la parte superior derecha.
1. Haga clic en el "Vínculo de vídeo" y verá y escuchará la transmisión en vivo de YouTube. 
1. Esta dirección URL es el vínculo de streaming en vivo y se puede compartir con todos los canales de redes sociales :)
1. Para detener la transmisión en vivo, seleccione END STREAM on YouTube **(END STREAM** en YouTube) y Stop Streaming on OBS **(Detener streaming** en OBS).

Para obtener puntos extra, comparta sus vídeos en redes sociales y asegúrese de etiquetarnos @AltspaceVR :)