---
title: Creación de un evento
description: Obtenga información sobre los eventos AltspaceVR, cómo crearlos y agregar objetos 3D y personal de marca con el Editor del mundo.
ms.date: 03/11/2021
ms.topic: article
keywords: events, terminology, console, multimedia, world editor, live stream
ms.openlocfilehash: 0c6e59604339ad354dc0241ca81335f92d65b0845529f6d1fe5eb2eb0d18627f
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127460"
---
# <a name="creating-an-event"></a>Creación de un evento

Esta es una guía paso a paso para crear eventos en AltspaceVR. Se recomienda encarecidamente que asista a varios eventos en AltspaceVR para obtener una sensación de cómo funcionan. Compruebe el [Calendario de eventos AltspaceVR](https://account.altvr.com/events) para obtener una lista de todos nuestros eventos.

En este artículo, aprenderá lo siguiente:

* Terminología del evento AltspaceVR
* Creación de un evento y un espacio de eventos o un mundo
* Uso de la consola multimedia para una presentación de diapositivas
* Personal de marca del evento con imágenes
* Agregar objetos 3D mediante world editor/kits
* Cómo grabar o Live Stream Mi evento

## <a name="altspacevr-event-terminology"></a>Terminología del evento AltspaceVR

Estos son los términos con los que debe estar familiarizado para crear el espacio de eventos y eventos:

</br>

| Término | Definición |
|---|---|
| World Building | AltspaceVR ofrece la capacidad de crear y personalizar mundos virtuales. Los hosts de AltspaceVR admiten documentación, canales de discordia y eventos en el mundo para ayudarle a obtener más información sobre cómo obtener ayuda y [empezar a crear mundos.](../world-building/world-building-faq.md) |
| World | Un mundo es un espacio virtual en AltspaceVR. Puede ser una oficina o una gran cadena de montaña. Es un entorno muy personalizable. Se encuentra dentro de un universo y puede haber varios mundos dentro de ese universo. Si desea tener varios espacios de eventos para eventos especiales, centros de entrenamiento y diferentes espacios de reunión para crear cosas, agregue los mundos del mismo universo para mantenerlos juntos como un grupo. |
| Universo | Un universo en AltspaceVR world building vernacular representa la categorización de los mundos. Cada universo puede contener varios mundos. Los mundos heredan la configuración del universo, lo que facilita la adición de personas a la lista de permitidos para varios mundos y otras características de control. Consulte [Managing Your Worlds (Administración de los mundos)](../world-building/managing-worlds.md) para obtener más información. |
| Plantilla | Una plantilla (o plantilla de espacio) es un entorno o mundo creado previamente que se puede usar en lugar de crear una con las características de World Building. AltspaceVR ofrece una amplia gama de plantillas para diferentes experiencias y eventos. |
| Espacio de eventos | Un espacio de eventos es un sinónimo de world en AltspaceVR. En general, hace referencia a un mundo que se usa para hospedar eventos. |
| Sitio web | Las referencias al "sitio web" son al [sitio web de AltspaceVR.](https://altvr.com/) A menudo es más fácil crear y editar eventos a través de la página [web](https://account.altvr.com/events/my) Eventos en un equipo o tableta en lugar de a través del dispositivo VR. También tendrá que acceder al sitio web para [la creación](../world-building/managing-worlds.md) mundial. |
| Roles contextuales | [Los roles contextuales](../getting-started/roles.md) los asigna el creador de eventos o el creador del mundo. Estos roles dan a los usuarios características y funcionalidades adicionales en un espacio de eventos o mundo. Actualmente, se componen de Host, Moderator, Pilot (flight), Terraformer (world building) y Megaphone Only. Se pueden asignar individual o globalmente, lo que permite a todos tener los mismos roles en el espacio de eventos o en el mundo. |
| Interfaz de usuario (UI)/Menu | Cuando se encuentra en AltspaceVR en el mundo, dentro del entorno envolvente, hay menús a la izquierda y a la derecha de la pantalla. El círculo o el menú principal con el logotipo altspaceVR abre la interfaz de usuario (UI) principal o el menú para acceder a distintas pantallas para explorar AltspaceVR y personalizar su experiencia. Los elementos opcionales de la interfaz de usuario se encuentran en el tamaño correcto de la pantalla y suelen incluir World Editor y Host Tools. Estos se abren e interactúan haciendo clic en ellos con el cursor. |
| SDK/MRE | Estos son los términos de creación del mundo asociados al Kit de desarrollo de software y Mixed Reality [Extensions](../world-building/using-mixed-reality-extensions.md) que se usan para agregar características y funcionalidades a la experiencia de creación mundial. Normalmente son para usuarios más avanzados. |

## <a name="understanding-events"></a>Descripción de eventos

AltspaceVR facilita la creación de un mundo en el que puede usar un espacio de plantilla precalcial para usar o personalizar para sus necesidades específicas, o crear un mundo desde cero. En este artículo se trata el uso de una plantilla predefinida para crear el evento. Las secciones siguientes sobre [personalización de](#branding-your-event-with-images) marca de un evento con imágenes y Adición de objetos [3D](#adding-3d-objects-using-world-editor-and-kits) mediante el editor y los kits del mundo incluyen sugerencias para una mayor personalización. Para obtener información sobre cómo crear un mundo personalizado desde cero, asista a los encuentros de World Building Tour en AltspaceVR y consulte la documentación de soporte técnico de [World Building](../world-building/world-editor-getting-started.md).

AltspaceVR ofrece dos maneras de crear un espacio para el evento.

* **Uso único:** Cree un evento y seleccione un mundo de plantillas.
* **Uso repetido:** Cree un espacio del mundo e impórtelo en el evento.

El proceso de creación de un evento es el [](../world-building/managing-worlds.md) mismo para ambos, con una excepción: la creación de un mundo y su importación como un espacio de eventos de uso repetido. También debe saber lo siguiente:

</br>

| Término | Definición |
|---|---|
| World copied (Mundo copiado) | El uso de un espacio mundial para un evento repetido permite una personalización persistente. Los signos, las imágenes, los puntos de generación y otras personalizaciones se mantienen de evento a evento en lugar de personalizar el espacio del evento cada vez. |
| Personalización del mundo de los eventos | Cuando se crea un evento, la plantilla o el mundo importado se copia y se bloquea en ese evento. Puede realizar cambios en el mundo de los eventos y no afectar al mundo original y al contrario. Considere la posibilidad de agregar decoración de vacaciones, imágenes u otros elementos del editor del mundo de uso único para que el espacio del evento sea más divertido y adecuado para el evento. |

Las modificaciones realizadas en el mundo original no estarán en el mundo del evento a menos que se actualice el espacio de eventos:
1. Use el **botón RE-IMPORT WORLD** en la página web del evento.
2. Espere entre 2 y 3 minutos para que se complete la sincronización. 
3. Si el espacio de eventos no ha cambiado, vaya a Configuración > Restablecer > **restablecer** espacio para restablecer el espacio de eventos. Restablecerá mucho el espacio como creador del mundo.

Si tiene problemas técnicos, como que los elementos no se cargan correctamente, vaya al menú AltspaceVR y seleccione Configuración > **Moderar > Restablecer** espacio para restablecer el espacio de eventos y ver los nuevos cambios. Windows Los usuarios de PC en 2D pueden usar el método abreviado de teclado **CTRL + ALT + R** en AltspaceVR para restablecer rápidamente el espacio.

## <a name="creating-your-event-and-event-space-or-world"></a>Creación de un evento y un espacio de eventos o un mundo

A continuación se indican instrucciones paso a paso para crear un evento para un evento único o repetido. Seleccionando la plantilla o importando un mundo para el evento. 

> [!NOTE]
> La página web de eventos AltspaceVR ofrece instrucciones sobre todos los aspectos del formulario mediante el uso de botones de signo de interrogación verdes. Coloque el cursor sobre ellos para obtener instrucciones específicas.

En la [página web Eventos > Mis](https://account.altvr.com/events/my) eventos en el  sitio web de AltspaceVR, seleccione Programar un evento o vaya directamente a la página web Crear evento en [AltspaceVR](https://account.altvr.com/events/new).

1. **Título del evento:** Escriba el nombre del evento. Mantén la información específica y concisa para su visualización en las distintas vistas de calendario en el sitio web de AltspaceVR y en la interfaz del mundo. Intente mantener el título por debajo de 23 caracteres, incluidos los espacios entre palabras.
2. **Descripción:** Escriba la descripción del evento.
    * Debe tener al menos 10 caracteres en la descripción o no se creará el evento.
    * Agregue un espacio vacío entre párrafos.
    * Para agregar un vínculo a facebook, discordia, sitio web u otros recursos del evento, use el formato siguiente (este markdown solo funciona en la página de promoción del evento en el sitio web, esto no se representará correctamente en los menús AltspaceVR): `[Event Name](http://example.com/)`

3. **Fecha de inicio/fecha de finalización:** Establezca la hora de inicio y asegúrese de que la hora de finalización es posterior a la hora de inicio.
4. **Categoría:** Elija la categoría que mejor describa el tipo de evento. 
5. Establezca el evento en **Privado** o **Público.**
    * Visibilidad: los eventos públicos están visibles en la pestaña Todos del calendario de eventos del sitio web de AltspaceVR [y](https://account.altvr.com/events/all) están abiertos al público.
    * Los eventos privados no están visibles en los calendarios de eventos AltspaceVR y requieren que la dirección URL del evento escriba el espacio del evento.
    * Si desea "Agregar como evento principal", el evento debe establecerse en público.
6. **Seleccione una plantilla:** En el lado derecho de la página web hay una lista de imágenes en miniatura de las plantillas disponibles en AltspaceVR. Hay salas de juegos, oficinas, espacios de reuniones, espacios de presentación y espacios de encuentro divertidos. Seleccione uno que parezca interesante. Si no le gusta, vaya y cree un nuevo evento con una nueva plantilla. Si desea crear su propio mundo de eventos personalizados, seleccione **El cielo** escoboso como plantilla predeterminada y siga las instrucciones siguientes para importar su mundo.
7. Seleccione **OPCIONES AVANZADAS.**

### <a name="advanced-options"></a>Opciones avanzadas

1. **Promover:** Cada evento requiere dos imágenes de personal de marca (estas imágenes aparecen en el sitio web altspaceVR y no aparecen en el evento dentro de AltspaceVR):
    * **Icono:** La imagen de mosaico debe ser de 1920 x 1080 píxeles. Esta imagen se escalará a varios tamaños de miniatura y se mostrará en el calendario de eventos AltspaceVR con otros eventos. Asegúrese de que la imagen está clara y no tiene mucho texto. No use imágenes o logotipos con derechos de autor que no posee.
    * **Banner:** Las imágenes de banner deben ser de 1920 x 576. Este cambio de tamaño se ajustará automáticamente según sea necesario y visible en la información del evento o la página web. Una superposición semitransparente cubre el 25 % inferior de la imagen. Evite colocar texto en esa área.
    * Otra opción (más rápida) es copiar la imagen de mosaico en la imagen de banner de **fondo,** que también usará la imagen de icono como imagen de banner. Pruébalo :). Si no tiene buen aspecto, puede crear una nueva imagen de Banner.
2. **En VR:** En esta sección se incluyen características que se aplican a la experiencia virtual durante el evento dentro de la aplicación AltspaceVR:
    * **Roles contextuales predeterminados:** El signo de interrogación verde muestra los roles específicos disponibles para *todos los miembros de la audiencia del evento*. El más común es *megaphone_only*. Agregue esto para dar la opción "Ampliar mi voz" bajo el botón Herramientas de host a todos los miembros de la audiencia para que se puedan escuchar en el evento si es un espacio grande. Si el evento requiere vuelo, agregue *el piloto*. Para agregar ambos, el formato es: *megaphone_only, piloto*. Cada usuario debe habilitar el modo Fly en la aplicación AltspaceVR Configuración/Input/Fly.
    * **Instrucciones:** Las [instrucciones](../world-building/adding-welcome-messages.md) son para el texto que genera una imagen de bienvenida al llegar al espacio. Los usuarios deben seleccionar "Aceptar" para quitarlo de su vista. Esto suele usarse para proporcionar instrucciones para el público como "Please stay muted until invited to speak" (Permanezca silenciado hasta que se le invite a hablar) o "Welcome to XYZ event where we'll be covering ABC". Esto no es necesario, por lo que debe usar de forma judiciosa. También puede usar Markdown para agregar color y tamaño de fuente, más detalles: [http://digitalnativestudios.com/textmeshpro/docs/rich-text](http://digitalnativestudios.com/textmeshpro/docs/rich-text)
3. **Avanzado:** A continuación se muestra una explicación rápida de las características avanzadas de los eventos (algunas de estas características no se mostrarán hasta después de crear el evento y edite el evento):
    * **Administradores:** Los administradores son usuarios de AltspaceVR en los que confía para ayudarle a administrar el evento. Pueden ser los cohosts o los hosts de copia de seguridad. Al agregar su nombre de usuario a la lista De administradores, pueden:
        * Cambie el título, la descripción y otras características del evento.
        * Agregue y quite roles contextuales para moderadores, hosts y otros roles.
        * Elimine el evento.
    * **Grupo:** Elija entre los grupos [privados mediante](group-features.md) el menú desplegable. Solo se mostrará si la cuenta se ha creado o se ha agregado a un grupo.
    * **Etiqueta:** Esta frase concisa se mostrará en la página web del evento bajo el título .
    * **Importar desde el mundo:** Para usar un espacio de eventos del mundo creado para un uso repetido, esta es la sección del formulario que se va a usar para importar el diseño y la personalización de ese mundo en el evento. Tenga presente las siguientes consideraciones:

    **Importar su propio mundo:** Para importar un mundo, ha creado y posee:
    * Seleccione la flecha desplegable para ver una lista de mundos que ha creado.
    * Seleccione el mundo.
    * Después de completar el resto del formulario de evento, espere al menos 2 minutos antes de visitar el espacio de eventos en AltspaceVR para asegurarse de que la información de la base de datos se actualiza y se genera el mundo.
    
    **Usar el mundo de otra persona:**
    * Póngase en contacto con el propietario del mundo para solicitar que use la característica **Compartir** con amigos en un mundo individual para compartirlo con usted.

3. **Identificador de vídeo de YouTube:** Visible en la página web del evento, agrega finalizadores o vídeos de eventos de YouTube a la página web del evento, no en el mundo. Solo necesitará la parte del identificador de vídeo de la dirección URL: dQw4w9WgXcQ.
4. **Identificador de Twitter:** Esto agrega la secuencia de Twitter a la página web del evento. Si la cuenta de Twitter es personal y no está relacionada con el evento o la asociación, es posible que esté compartiendo en exceso. Solo necesitará el identificador: @elonmusk
5. **Roles contextuales:** Aquí es donde se controlan los superpoderes o [roles contextuales](../world-building/granting-roles.md) de los hosts de eventos, moderadores y otros roles dentro del evento. Para agregarlos, escriba su nombre de usuario altspaceVR y asígneles un rol en el menú desplegable. Para quitarlos, active la casilla Quitar y guarde la página web del evento. NOTA: Si desea conceder una funcionalidad de moderación de host, debe agregarla como host y moderador. Los siguientes roles contextuales están disponibles actualmente:
    * **Host:** Agrega las [características de Front Row](../faqs/front-row-events.md) a la interfaz del usuario en AltspaceVR para agregar esas características.
    * **Moderator:** Agrega características de moderación a la interfaz del usuario, incluida la capacidad de enviar mensajes de texto a cada asistente, silenciarlos globalmente para el evento o quitarlos del evento. Vuelva a agregar el host y asízcále roles de moderación si desea que tengan privilegios de moderación.
    * **Solo megáphone:** Agrega el botón Amplify My Voice (Ampliar mi voz) a su interfaz mediante el botón Host Tools (Herramientas de host).
    * **Terraformer:** Agrega el botón Editor del mundo a su interfaz.
    * **Piloto:** Agrega funcionalidades de vuelo para ese individuo. NOTA: Deben habilitar esto en Configuración/Entrada/Fly
    * **Intérprete de música:** Agrega funcionalidades y características asociadas a eventos de música y de música.
6. **Bloquear usuarios enumerados:** Si desea bloquear el acceso de un usuario o un moderador o un host ha quitado previamente un usuario del evento y el evento está duplicado, se mostrará el nombre del usuario de la lista de bloques. Los hosts de eventos o administradores pueden agregar o quitar un usuario de la lista de bloques en cualquier momento.

Una vez completado el formulario y activado el triple, seleccione **CREATE EVENT**.

> [!IMPORTANT]
> Si el evento no se crea correctamente, asegúrese de que tiene al menos 10 caracteres en la descripción o que ha seleccionado una plantilla, el nombre de la plantilla pasará de blanco a azul si está seleccionado.

## <a name="event-page-actions"></a>Acciones de página de eventos

En la página web Evento, tiene las siguientes acciones y opciones:

1. Seleccione **EDITAR para** realizar cambios en la configuración del evento.
2. Seleccione **END EVENT (FINALIZAR** EVENTO) para finalizar el evento (por ejemplo, si el evento ha terminado pronto).
3. Seleccione **SET TO DRAFT (ESTABLECER EN BORRADOR)** para establecer el evento en Draft en lugar de Active (Activo).
4. Si ha realizado una actualización en el mundo importado, deberá seleccionar **RE-IMPORT WORLD** para que esos cambios aparezcan en el evento, no olvide restablecer el espacio en el evento :)
5. Seleccione **DUPLICATE EVENT (EVENTO DUPLICADO)** para duplicar el evento para eventos futuros. Este duplicado aparecerá en Mis eventos/Mis eventos de borrador; deberá actualizar el nuevo día y hora y activarlo desde allí.
6. Seleccione **AGREGAR COMO EVENTO PRINCIPAL para** establecer el evento en la lista de calendarios.
7. Seleccione **DELETE EVENT (ELIMINAR** EVENTO) si desea eliminar completamente el evento (no se puede recuperar).

Cuando esté listo, vaya al menú **Eventos > Mis** eventos en la interfaz del mundo AltspaceVR y escriba el espacio de eventos en Restablecer espacio, inspeccione los cambios o continúe con la personalización. 

> [!IMPORTANT]
> Se trata de una copia y las personalizaciones del espacio de eventos son solo para este evento. Si dedica mucho tiempo a personalizar el espacio del evento, podría ser mejor crear un mundo para el evento **de uso repetido**.

Para obtener más información sobre cómo personalizar el espacio de eventos o crear un mundo de espacio de eventos original para importar:

* [Cómo conceder roles a otras personas de mis mundos?](../world-building/granting-roles.md)
* [Cómo permitir que las personas vuelen (o tengan otras capacidades) en mi mundo?](../world-building/adding-user-abilities.md)
* [¿Dónde puedo obtener ayuda con la creación mundial?](../world-building/getting-help.md)
* [Cómo administrar mis mundos?](../world-building/managing-worlds.md)
* [Preguntas más frecuentes sobre world-building](../world-building/world-building-faq.md)
* [Cómo agregar puntos de generación personalizados a mis mundos?](../world-building/adding-custom-spawn-points.md)
* [Cómo cargar mis propios kits?](../world-building/uploading-custom-kits.md)
* [Cómo introducción a World Building Toolkit (Unity Uploader)?](../world-building/world-building-toolkit-getting-started.md)

## <a name="using-the-multimedia-console-for-a-slide-presentation"></a>Uso de la consola multimedia para una presentación de diapositivas

La consola multimedia es una excelente manera de organizar el contenido de una presentación, incluidas imágenes, audio o vídeo. Siga las [instrucciones de la consola multimedia](multimedia-console.md) para obtener esa configuración para el evento.

## <a name="branding-your-event-with-images"></a>Personal de marca del evento con imágenes

Agregar imágenes al espacio de eventos o al logotipo y personal de marca de su empresa, o incluso fotografías de usted mismo, su equipo u otro contenido visual es fácil en AltspaceVR.

Los requisitos de imagen son:
* Se aceptan archivos JPG o PNG
* Tamaño máximo de la imagen: 1920 x 1080
* Resolución: 72 PPP
* Tamaño de archivo: menos de 250 KB por archivo

El proceso implica cargar la imagen en [altspaceVR Fotos](https://account.altvr.com/photos)y, a continuación, usar el Fotos en el editor del mundo para importarla y colocarla en el espacio del mundo del evento.

1. Vaya a [Fotos](https://account.altvr.com/photos) en el sitio web de AltspaceVR.
2. Haga clic en **Cargar**.
3. Seleccione **Examinar** para abrir un cuadro de diálogo en el equipo y busque y seleccione la imagen optimizada.
4. seleccione **Open**(Abrir).
5. Seleccione CREATE PHOTO ( **CREAR FOTO).**
6. Repita este paso para todas las imágenes.

En AltspaceVR y en el mundo del evento, colócate cerca de donde quieras colocar la imagen. (Si va a crear esto para un evento **de** uso repetido, asegúrese de que está en su mundo y no en el espacio evento).

1. En la interfaz de usuario, en la esquina inferior derecha, seleccione **Editor del mundo/Panel del editor.**
2. Haga clic en **la** pestaña Minería en la parte inferior.
3. Seleccione **Fotos**.
4. Fotos se almacenan en el orden cronológico de carga, por lo que la imagen más reciente cargada debe ser la primera imagen de la lista. Selecciónelo para agregarlo al mundo.
5. Con el cursor del dispositivo, tome la imagen y colócala donde quiera que esté.
    * Puede cambiar su tamaño con los controladores (normalmente, deslizar el dedo horizontalmente por el panel táctil en VR o usar el mouse en modo 2D).
    * Para ajustar la posición y la rotación de la imagen, seleccione el símbolo **GEAR** en la imagen en el Editor y establezca los valores de Rotación y Posición correctamente.
    * También puede cambiar el tamaño de la imagen con la característica Escala.

> [!NOTE]
> Cuando el modo de edición está en (texto naranja), tendrá automáticamente la capacidad de realizar la marcha, lo que permite un movimiento más sencillo para colocar imágenes más arriba en el mundo del evento.

6. Repita esta opción para cada ubicación de imagen.
7. Cuando las imágenes estén establecidas en su lugar, seleccione Bloquear todo si no las bloqueó individualmente, desactive El modo de edición y cierre el editor. 
8. Use un máximo de cinco Fotos por evento.

## <a name="adding-3d-objects-using-world-editor-and-kits"></a>Adición de objetos 3D mediante el editor y los kits del mundo

AltspaceVR permite importar objetos 3D a mundos con el Editor del mundo. Hay muchos kits de editores del mundo disponibles actualmente para su uso y mucho más en el camino. Hay spaceships, rockets, animated trees, trees, plants y muchos objetos diferentes. O bien, puede agregar sus propios kits a la colección pública o para su propio uso personal, o considerar la posibilidad de usar una de las [aplicaciones altspaceVR MRE](../world-building/using-mixed-reality-extensions.md), que aportan objetos interactuables a su mundo, como cascos, accesorios, alerones, ropa, cascos u otros objetos interactables. Espere que la lista de objetos se expanda pronto.

Las instrucciones aquí se centran en el uso de elementos que ya están en los kits. Para obtener más información sobre cómo agregar e importar objetos 3D en AltspaceVR, consulte "Cómo importar modelos [glTF a mis mundos?".](../world-building/importing-models.md) y ["Cómo cargar mis propios kits?".](../world-building/uploading-custom-kits.md)

Para agregar un objeto 3D existente de World Building Kits a su mundo de eventos, con el Editor del mundo o el Panel del editor abierto y el modo de edición habilitado:

1. Explore los kits del objeto que desea importar y selecciónelo.
2. Seleccione en el objeto de kit con el cursor y posiciónelo. Use el icono GEAR del objeto en el Editor del mundo para usar las opciones Posición, Rotación y Escala para la entrada de número manual.
3. Cuando el objeto se coloque en la posición correcta, haga clic en el icono Bloquear para bloquearlo.
4. Agregue otro objeto si lo desea. Sea judioso a la hora de agregar objetos 3D, manteniendo sus selecciones en no más de elementos de cinco kits individuales diferentes, para mejorar la compatibilidad del usuario con Oculus Quest. No use más de 200 objetos en un mundo.
5. Cuando haya terminado, bloquee todos los elementos, desactive el modo de edición y cierre el Editor del mundo. Pasear. Invite a algunos evaluadores a visitarlo y echarle un vistazo, y prepárese para su excelente evento.

Para obtener más información sobre los kits del editor del mundo y agregar objetos 3D a AltspaceVR:

* [¿Qué es el Programa de acceso anticipado?](../world-building/early-access.md)
* [¿Cómo importar modelos glTF en mis mundos?](../world-building/importing-models.md)
* [Cómo usar un MRE en mi mundo?](../world-building/using-mixed-reality-extensions.md)

## <a name="how-to-record-or-live-stream-my-event"></a>Cómo grabar o Live Stream Mi evento

Consulte el siguiente documento de soporte técnico para obtener instrucciones sobre cómo grabar o transmitir en vivo el evento:

* [Cómo grabar o Live Stream Mi evento](recording-and-live-streaming.md)