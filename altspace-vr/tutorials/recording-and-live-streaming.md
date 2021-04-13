---
title: Grabación y streaming en vivo
description: Obtenga información sobre cómo grabar y transmitir en vivo los eventos de AltspaceVR desde su equipo para promocionarlos y compartirlos con los usuarios.
ms.date: 02/10/2021
ms.topic: article
keywords: streaming, grabación
ms.openlocfilehash: 80d54407915af1a0d4b7783858446f54205e6a2a
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213899"
---
# <a name="recording-and-live-streaming"></a>Grabación y streaming en vivo

La grabación y el streaming en vivo de su experiencia de AltspaceVR para mostrar otras personas de todo el mundo es una excelente manera de promocionar el evento, AltspaceVR y VR en general. Eche un vistazo a continuación para ver cómo empezar:

En este artículo, aprenderá a:

* [Cómo grabar AltspaceVR en modo 2D en PC](#recording-altspacevr-in-2d-mode-on-pc)
* [Cómo hacer streaming en vivo en YouTube en AltspaceVR en modo 2D en PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## <a name="recording-altspacevr-in-2d-mode-on-pc"></a>Grabar AltspaceVR en modo 2D en PC

### <a name="the-short-version"></a>La versión abreviada

Tenga instalado AltspaceVR y OBS. Inicie AltspaceVR en modo 2D, inicie OBS, establezca OBS hasta record AltspaceVR y record Away.

### <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

1. Visite [https://obsproject.com/](https://obsproject.com/).
2. Seleccione **Windows** para descargar OBS. Esta publicación está usando **OBS v 22.0.2**
3. Instalación de OBS

### <a name="have-altspacevr-running-in-2d-mode-before-you-run-obs"></a>Tenga AltspaceVR ejecutándose en modo 2D antes de ejecutar OBS

1. Descargue e instale AltspaceVR desde nuestro sitio web: [altvr.com/get](https://altvr.com/getaltspacevr)
2. Asegúrese de iniciar AltspaceVR en modo 2D desenchufando el cable USB del HMD de su PC o bien, si tiene un Rift: Ctrl + Alt + Supr, servicios, Oculus servicio en tiempo de ejecución, haga clic con el botón derecho en detener. 
    * Esto deshabilitará Oculus e iniciará AltspaceVR en modo 2D, repetirá estos pasos y usará Start para volver a obtener el modo VR.

Ahora, Alt-Tab a OBS:

1. En orígenes, seleccione **+ > captura de juegos > crear nuevo** .
2. Edite el texto en ' AltspaceVR Capture ', marque la marca del **código fuente** y haga clic en Aceptar.
3. Haga doble clic en **AltspaceVR Capture** en sources
4. Cambiar el **modo** para **capturar una ventana específica**
5. Ventana: [AltspaceVR.exe]: AltspaceVR
6. Prioridad de coincidencia de ventana: título de coincidencia; de lo contrario, buscar ventana del mismo archivo ejecutable
7. Desplazarse hacia abajo hasta el cursor de captura: desmarcar correcto

Esto debería hacer que AltspaceVR aparezca en OBS. Ahora, para establecer las propiedades siguientes en OBS, vaya a **archivo > configuración**:

| Pestaña | Configuración |
|---|---|
| General | Deje el valor predeterminado. |
| Stream | Deje el valor predeterminado. |
| Modo de salida: cambiar a avanzado | Pestaña transmisión por secuencias <br> Pista de audio 1 <br> Codificador: x264 <br> Aplicar la configuración del codificador del servicio de streaming: tick <br> Cambiar el tamaño de la salida: sin marca <br> Control de velocidad: CBR <br> Velocidad de bits: 6000 (6000 para 30 fps o 9000 para 60 fps) <br> Intervalo de fotogramas clave = 2 <br> Valor preestablecido de uso de CPU = veryfast |
| Grabando | Tipo: estándar <br> Ruta de grabación: D:/video (Desplácese hasta el lugar en el que desea guardar el archivo de vídeo) <br> Formato de grabación: MP4 (si se produce algún bloqueo mientras se graba, pruebe con FLV aquí en lugar de MP4, si se bloquea el vídeo se seguirá pudiendo usar con FLV). <br> Pista de audio 1 <br> Codificador: usar el codificador de secuencias |
| Audio | Velocidad de bits de audio: 160 (para todas las pistas) |
| Búfer de reproducción | Deje el valor predeterminado. |
| Audio | Frecuencia de muestreo: 48 kHz <br> Canales: estéreo <br> Dispositivo de audio de escritorio: predeterminado <br> Dispositivo de audio de escritorio 2: deshabilitar <br> Dispositivo de audio MIC/AUX: predeterminado |
| Vídeo | Resolución base (canvas): 1920 x 1080 <br> Resolución de salida (escalada): 1920 x 1080 <br> Filtro downscale: bicúbico (escala enfocada, 16 ejemplos) <br> Valores de FPS comunes: 30 |
| Teclas de acceso rápido | Deje el valor predeterminado. |
| Avanzado | Prioridad del proceso: normal |

Bien, ahora Asegúrese de seleccionar **aplicar** y, luego, haga clic en **Aceptar** para guardar todos los valores de configuración de OBS. 

1. Alt-Tabr a AltspaceVR, entrar en el espacio, el mundo o el evento correctos y alinear la cámara (es decir, su avatar) estamos a punto de grabar un vídeo.
2. Alt-Tab a OBS y, cuando esté listo, haga clic en **iniciar grabación**.

Verá en la parte inferior derecha de OBS que REC: empezará a contar, lo que significa que está grabando.

Realice una grabación de prueba de: 
1. En AltspaceVR abrir, cerrar o sustituir los menús para crear sonidos de la interfaz de usuario
2. Por ejemplo, "sibilance, sibilance" y póngase en marcha a otro usuario para hablar con usted en un volumen normal o ver un vídeo en la pantalla 2D.
3. Consulte los niveles de audio y MIC/AUX de escritorio como lo hace para ver si funciona.

Normalmente silenciamos el MIC/AUX al grabar. Continúe y seleccione el icono de altavoz para MIC/AUX y se volverá rojo con una X.

* Es muy difícil hacer coincidir el audio y el audio del otro usuario para que el micrófono sea mejor silenciado.
* Otro problema con el audio es la forma en que se configura OBS. Captura todo el audio del equipo, por lo que, si está viendo YouTube, registrará ese audio, el margen de demora o los sonidos de notificación.
* Para grabar solo el audio de AltspaceVR, vaya a mezclador de volumen (haga clic con el botón derecho en el icono de altavoz situado en la parte inferior derecha de Windows) y silenciar sonidos del sistema, exploradores, etc., pero no silenciar OBS ni AltspaceVR.

> [!IMPORTANT]
> No olvide volver a activar esta configuración de mezclador de volumen después de la grabación.

Ahora, vuelva a OBS y seleccione **Detener grabación** desde **archivo>Mostrar grabaciones**. Se abrirá la carpeta con los archivos de vídeo de OBS, haga doble clic en el vídeo de prueba.

A veces, la grabación es bastante alta, por lo que se reduce el control deslizante para el audio de escritorio y se realiza otra grabación para probar.

<!-- Missing image -->

## <a name="live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc"></a>Streaming en vivo a YouTube en modo AltspaceVR 2D en PC

### <a name="the-short-version"></a>La versión abreviada

Tenga instalado AltspaceVR y OBS. Inicie AltspaceVR en modo 2D, inicie OBS, ya sea streaming en vivo o cree un "nuevo evento en directo" en YouTube, configure OBS con la clave de Stream de YouTube, empiece a streaming en OBS, empiece a streaming en YouTube y esté fuera de las carreras.

### <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

1. Visite [https://obsproject.com/](https://obsproject.com/).
2. Haga clic en **Windows** para descargar OBS (esta publicación está usando OBS v 22.0.2)
3. Instalación de OBS

Tenga AltspaceVR ejecutándose en modo 2D antes de ejecutar OBS
1. Descargue AltspaceVR desde nuestro sitio web: [https://account.altvr.com/downloads](https://account.altvr.com/downloads)
2. Para asegurarse de que se inicia AltspaceVR en modo 2D, desconecte el cable USB de su HMD del equipo o si tiene un Rift: Ctrl + Alt + Supr, servicios, Oculus servicio en tiempo de ejecución, haga clic con el botón derecho en detener. Esto deshabilitará Oculus Home e iniciará AltspaceVR en modo 2D, repetirá estos pasos y comenzará a obtener el modo VR de nuevo.

Alt-Tab a OBS

1. En orígenes, seleccione **+** , seleccione captura de juego, crear nuevo, editar texto en ' captura de AltspaceVR ', marcar marca de código fuente, aceptar
2. Haga doble clic en AltspaceVR Capture
3. Modo: capturar ventana específica
4. Ventana: [AltspaceVR.exe]: AltspaceVR
5. Prioridad de coincidencia de ventana: título de coincidencia; de lo contrario, buscar ventana del mismo archivo ejecutable
6. Desplazarse hacia abajo hasta el cursor de captura: desmarcar correcto

Esto debería hacer que AltspaceVR aparezca en OBS. ¡Perfecto!

Ahora, en OBS, va a la configuración de>de archivos

| Pestaña | Configuración |
|---|---|
| General | Marcar automáticamente al transmitir por secuencias (registra un archivo de vídeo en el equipo además de streaming en vivo) |
| Stream | Tipo de secuencia: servicios de streaming <br> Servicio: juegos de YouTube/YouTube (también se puede transmitir a Twitch, Mixer, Facebook Live, etc.)<br>Servidor: servidor principal de introducción de YouTube <br>Clave de secuencia: pegue la clave de flujo de YouTube * * _ (consulte Configuración de Live <br>Streaming en YouTube ' más abajo] |
| Salida | Modo de salida: cambiar a avanzado |
| Streaming | Pista de audio 1 <br>Codificador: x264 <br>Aplicar la configuración del codificador de servicio de streaming <br>Cambiar el tamaño de la salida: sin marca <br>Control de velocidad: CBR <br>Velocidad de bits: 6000 (6000 para 30 fps o 9000 para 60 fps) <br>Intervalo de fotogramas clave = 2 <br>Valor preestablecido de uso de CPU = veryfast |
| Grabando | Tipo: estándar <br>Ruta de grabación: D:/video (Desplácese hasta el lugar en el que desea guardar el archivo de vídeo si seleccionó "grabar automáticamente al streaming" anteriormente) <br>Formato de grabación: MP4 (si se produce algún bloqueo mientras se graba, pruebe con FLV aquí en lugar de MP4, si se bloquea el vídeo se seguirá pudiendo usar con FLV). <br>Pista de audio 1 <br>Codificador: usar el codificador de secuencias |
| Audio | Velocidad de bits de audio: 160 (para todas las pistas) frecuencia de muestreo: 48 kHz <br>Canales: estéreo <br>Dispositivo de audio de escritorio: predeterminado <br>Dispositivo de audio de escritorio 2: deshabilitar <br>Dispositivo de audio MIC/AUX: predeterminado |
| Búfer de reproducción | Deje el valor predeterminado. |
| Vídeo | Resolución base (canvas): 1920 x 1080 <br>Resolución de salida (escalada): 1920 x 1080 <br>Filtro downscale: bicúbico (escala enfocada, 16 ejemplos) <br>Valores de FPS comunes: 30 |
| Teclas de acceso rápido | Deje el valor predeterminado. |
| Avanzado | Prioridad del proceso: normal |

Bien, ahora Asegúrese de hacer clic en aplicar, luego en aceptar y, luego, en cerrar y volver a abrir OBS. Esto guardará todos los valores de configuración de OBS. Buscar buenos:)

Consulte la sección "Cómo grabar AltspaceVR en modo 2D en PC" anterior para obtener instrucciones sobre cómo probar la grabación con una grabación local en lugar de la secuencia en directo y también cómo obtener la configuración de la cámara antes de la grabación.

Otro problema con el audio es la forma en que se configura OBS. Captura todo el audio del equipo, por lo que, si está viendo YouTube, registrará esos mensajes de audio, equipos o sonidos de notificación.

Para grabar solo el audio de AltspaceVR, vaya a mezclador de volumen (haga clic con el botón derecho en el icono de altavoz situado en la parte inferior derecha de Windows) y silenciar sonidos del sistema, exploradores, etc., pero no silenciar OBS ni AltspaceVR.

No se olvide de volver a activarlas después de la grabación;)

### <a name="setting-up-live-streaming-on-youtube"></a>Configuración de streaming en vivo en YouTube

Puede obtener rápidamente una transmisión en vivo en directo (STREAMing en vivo) o configurar un evento de streaming en directo futuro (nuevo evento en directo). Es posible que le resulte más fácil configurarlo.

1. Abra el explorador e inicie sesión en [https://www.youtube.com/](https://www.youtube.com/)
2. Seleccione en el icono de la cuenta, en la parte superior derecha, seleccione Creator Studio en la lista desplegable.
3. STREAMing en vivo en el lado izquierdo de la página.

El método ' Stream Now ' cambia la vista en miniatura si tiene que cambiar el programa de instalación del CODIFICAdor de información básica mantenga la dirección URL del servidor como el nombre o la clave de la secuencia predeterminada _ * *, haga clic en ' Mostrar ' y copie esta clave Open OBS configuración de streaming en YouTube.
Para ver la página de vídeo real de YouTube live stream, debe desplazarse hacia abajo y mirar hacia la parte inferior derecha del vínculo de uso compartido.
Cópielo y péguelo en una nueva pestaña del explorador y, a continuación, haga clic en vídeos. en la lista verá el vídeo, se mostrará en este momento, haga clic en él y verá la página de YouTube live stream.
Esta dirección URL es el vínculo de la secuencia en directo y puede compartirse en todos los canales sociales:) Para detener la secuencia en directo, haga clic en detener streaming en OBS; esta finalizará la secuencia en directo en YouTube.

Método ' Events ': https://www.youtube.com/my_live_events haga clic en ' nuevo evento en directo ' agregar título, fecha, hora de inicio, Descripción y etiquetas; no olvide etiquetar AltspaceVR:) Elija público en el menú desplegable Tipo: haga clic en "crear evento" personalizado. Si desea agregar una miniatura personalizada, haga clic en examinar y cargue la imagen. (1280x720 funciona mejor) Select: clave de secuencia de un solo uso Seleccione su codificador: otros codificadores copiar nombre de flujo (clave de secuencia)

Ahora haga clic con el botón derecho en la vista "ver en la página de inspección" y "Abrir vínculo en una nueva pestaña"

Este es el vínculo de eventos de YouTube live stream, que puede compartirse con la misma dirección social por encima de su evento real.

Ahora, abra el archivo OBS>flujo de configuración, pegue la clave de secuencia que acaba de copiar en el campo de clave de secuencia, haga clic en "Live Control Room" y en "Abrir vínculo en una nueva pestaña" ahora vuelva a OBS para hacer clic en "iniciar streaming" de nuevo en YouTube. verá que el botón "vista previa" ahora es azul; se abrirá el cuadro de diálogo botón de vista previa, donde se le preguntará si desea obtener una vista previa del evento en directo, aceptar espere un momento y, a continuación, verá el botón "iniciar streaming" y se abrirá el cuadro de diálogo "iniciar streaming".

Ya está en directo.

Vaya a la pestaña del explorador con el vínculo "ver en la página de inspección" abierto para asegurarse de que el vídeo tenga un aspecto correcto. Recuerde que no oirá el audio porque ha desactivado el audio de los exploradores cuando los silencia en el mezclador de volumen de Windows. Compruebe el audio en el teléfono o pida a un amigo que consulte el audio.

¿Está mirando bien!

Alt-Tab volver a AltspaceVR para mover la cámara (es decir, su avatar) en torno al evento.

Cuando haya terminado con la secuencia en directo, vuelva a la página de la sala de control en directo de YouTube.

Haga clic en "detener transmisión por secuencias"

Se abre el cuadro de diálogo, en el que se le pregunta si desea detener el streaming del evento en directo, aceptar

Vaya a OBS y haga clic en detener streaming también.

Enhorabuena ahora es un streaming de AltspaceVR.


Recording_AltspaceVR_.png


En el caso de los puntos de bonificación, comparta sus vídeos con el mundo de los medios sociales y asegúrese de etiquetarnos @AltspaceVR :)