---
title: Crear un evento
description: Obtenga información sobre los eventos de AltspaceVR, cómo crearlos y cómo agregar personalización de marca y objetos 3D con el editor mundial.
ms.date: 03/11/2021
ms.topic: article
keywords: eventos, terminología, consola, multimedia, editor mundial, streaming en vivo
ms.openlocfilehash: 9b9f7ac8ef5d036b739873fc19c879250a1e264e
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213720"
---
# <a name="creating-an-event"></a>Crear un evento

Esta es una guía paso a paso para crear eventos en AltspaceVR. Se recomienda encarecidamente que asista a varios eventos en AltspaceVR para familiarizarse con su funcionamiento. Busque en el [calendario de eventos AltspaceVR](https://account.altvr.com/events) una lista de todos los eventos.

En este artículo, aprenderá lo siguiente:

* Terminología de eventos de AltspaceVR
* Crear el espacio de eventos y eventos o el mundo
* Usar la consola multimedia para una presentación de diapositivas
* Personalización de marca del evento con imágenes
* Agregar objetos 3D mediante el editor mundial
* Cómo grabar o Live Stream My Event

## <a name="altspacevr-event-terminology"></a>Terminología de eventos de AltspaceVR

A continuación se indican los términos que debe conocer para crear el evento y el espacio de eventos:

</br>

| Término | Definición |
|---|---|
| Edificio mundial | AltspaceVR ofrece la posibilidad de crear y personalizar mundos virtuales. AltspaceVR hospeda documentación de soporte técnico, canales de descables y eventos en el mundo para ayudarle a obtener [más información sobre cómo obtener ayuda y comenzar a crear mundos](../world-building/world-building-faq.md). |
| World | Un mundo es un espacio virtual en AltspaceVR. Puede tratarse de una oficina o de una amplia gama de Mountain. Se trata de un entorno muy personalizable. Se encuentra dentro de un universo y puede haber varios mundos dentro de ese universo. Si desea tener varios espacios de eventos para eventos especiales, centros de entrenamiento y diferentes espacios de reuniones para enriquecer las cosas, agregue los mundos en el mismo universo para mantenerlos juntos como un grupo. |
| Universo | Un universo en AltspaceVR World Building vernáculo representa la categorización de los mundos. Cada universo puede tener varios mundos. Los mundos heredan la configuración del universo, lo que facilita agregar personas a la lista de permitidos para varios mundos y otras características de control. Consulte [Administración de los mundos](../world-building/managing-worlds.md) para obtener más información. |
| Plantilla | Una plantilla (o plantilla de espacio) es un entorno o un mundo prediseñado que se puede usar en lugar de crear una mediante las características de creación del mundo. AltspaceVR ofrece una amplia variedad de plantillas para diferentes experiencias y eventos. |
| Espacio de eventos | Un espacio de eventos es un sinónimo del mundo en AltspaceVR. En general, hace referencia a un mundo que se usa para hospedar eventos. |
| Sitio web | Las referencias al "sitio web" son el [sitio web de AltspaceVR](https://altvr.com/). A menudo es más fácil crear y editar eventos a través de la [Página Web de eventos](https://account.altvr.com/events/my) en un equipo o tableta en lugar de hacerlo a través del dispositivo VR. También necesitará tener acceso al sitio web para la [creación del mundo](../world-building/managing-worlds.md) . |
| Roles contextuales | Los [roles contextuales](../getting-started/roles.md) se asignan mediante el creador del evento o el consorcio mundial. Estos roles proporcionan a los usuarios una funcionalidad y características adicionales del espacio de eventos o del mundo. Actualmente, se componen de host, presentador, moderador, piloto (vuelo), Terraformer (edificio mundial) y megaphone. Estos se pueden asignar individualmente o globalmente, lo que permite a todos los usuarios tener los mismos roles en el espacio de eventos o en el mundo. |
| Interfaz de usuario (UI)/menu | Cuando se encuentra en AltspaceVR en el mundo, dentro del entorno inmersivo hay menús a la izquierda y a la derecha de la pantalla. El círculo o el menú principal con el logotipo de AltspaceVR abre la interfaz de usuario (UI) o el menú principal para tener acceso a diferentes pantallas para explorar AltspaceVR y personalizar su experiencia. Los elementos de interfaz de usuario opcionales se encuentran en el tamaño correcto de la pantalla y, por lo general, incluyen el editor mundial y las herramientas de host. Para abrirlos y interactuar con ellos, haga clic en ellos con el cursor. |
| SDK/MRE | Se trata de términos de creación mundiales asociados al kit de desarrollo de software y [extensiones de realidad mixta](../world-building/using-mixed-reality-extensions.md) que se usan para agregar características y funcionalidad a la experiencia de creación del mundo. Suelen ser para usuarios más avanzados. |

## <a name="understanding-events"></a>Descripción de los eventos

AltspaceVR facilita la creación de un mundo en el que puede usar un espacio de plantilla predefinido para usar o personalizar según sus necesidades específicas, o bien crear un mundo desde cero. En este artículo se tratará el uso de una plantilla predefinida para crear el evento. Las secciones siguientes sobre [la personalización de marca del evento con imágenes](#branding-your-event-with-images) y la [adición de objetos 3D mediante el editor mundial y los kits](#adding-3d-objects-using-world-editor-and-kits) incluyen sugerencias para una personalización adicional. Para obtener información sobre cómo crear un mundo personalizado desde cero, asista a la guía de creación del mundo encuentros en AltspaceVR y [consulte la documentación de soporte técnico para la creación del mundo](../world-building/world-editor-getting-started.md).

AltspaceVR ofrece dos maneras de crear un espacio para el evento.

* **Uso único:** Cree un evento y seleccione el mundo de una plantilla.
* **Uso repetido:** Cree un espacio mundial e impórtelo en el evento.

El proceso de creación de un evento es el mismo para ambos, con una excepción: la [creación de un mundo e importarlo](../world-building/managing-worlds.md) como un espacio de eventos de repetición de uso. También debe saber:

</br>

| Término | Definición |
|---|---|
| Mundo copiado | El uso de un espacio mundial para un evento repetido permite la personalización persistente. Los signos, las imágenes, los puntos de generación y otras personalizaciones se mantienen de evento a evento en lugar de personalizar el espacio de eventos cada vez. |
| Personalizar el mundo del evento | Cuando se crea un evento, la plantilla o el mundo importado se copia y se bloquea en ese evento. Puede realizar cambios en el mundo del evento y no afectar al mundo original, y al revés. Considere la posibilidad de agregar adornos de festividades, imágenes u otros elementos del editor mundial de uso único y decorativo para que el espacio de eventos sea más agradable y adecuado para el evento. |

Las modificaciones realizadas en el mundo original no estarán en el ámbito del evento a menos que se actualice el espacio de eventos:
1. Use el botón **volver a importar el mundo** de la Página Web de eventos.
2. Permita 2-3 minutos para que se complete la sincronización. 
3. Si el espacio de eventos no ha cambiado, vaya a **configuración > moderar > restablecer espacio** para restablecer el espacio de eventos. Se restablecerá el espacio como un generador mundial.

Si tiene problemas técnicos, como los elementos que no se cargan correctamente, vaya al menú AltspaceVR y seleccione **configuración > moderada > restablecer espacio** para restablecer el espacio de eventos y ver los nuevos cambios. Los usuarios de PC de Windows en 2D pueden usar el método abreviado de teclado: **Ctrl + Alt + R** en AltspaceVR para restablecer rápidamente el espacio.

## <a name="creating-your-event-and-event-space-or-world"></a>Crear el espacio de eventos y eventos o el mundo

A continuación se muestran instrucciones paso a paso para crear un evento para un evento de una sola vez o repetido. Seleccionando la plantilla o importando un mundo para el evento. 

> [!NOTE]
> La Página Web de eventos AltspaceVR ofrece instrucciones sobre todos los aspectos del formulario mediante el uso de botones de signo de interrogación verdes. Revierta el cursor sobre ellas para obtener instrucciones específicas.

En la Página Web [eventos > mis eventos](https://account.altvr.com/events/my) del sitio web de AltspaceVR, seleccione **programar un evento** o vaya directamente a la [Página Web crear evento en AltspaceVR](https://account.altvr.com/events/new).

1. **Título del evento:** Escriba el nombre del evento. Manténgalo específico y conciso para verlo en las diversas vistas de calendario en el sitio web de AltspaceVR y en la interfaz en el mundo. Intente mantener el título en menos de 23 caracteres, incluidos los espacios entre las palabras.
2. **Descripción:** Escriba la descripción del evento.
    * Debe tener al menos 10 caracteres en la descripción o no se creará el evento.
    * Agregue un espacio vacío entre los párrafos.
    * Para agregar un vínculo a la Facebook, el descodificador, el sitio web u otros recursos del evento, use el formato siguiente (este Markdown solo funciona en la página de promoción del evento en el sitio web, lo que no se representará correctamente en los menús de AltspaceVR): `[Event Name](http://example.com/)`

3. Fecha de **Inicio y finalización:** Establezca la hora de inicio y asegúrese de que la hora de finalización es posterior a la hora de inicio.
4. **Categoría:** Elija la categoría que mejor describe el tipo de evento. 
5. Establezca el evento en **privado** o **público**.
    * Visibilidad: los eventos públicos están visibles en la [pestaña todos](https://account.altvr.com/events/all) del calendario de eventos del sitio web de AltspaceVR y están abiertos al público.
    * Los eventos privados no están visibles en los calendarios de eventos de AltspaceVR y requieren la dirección URL del evento para especificar el espacio de eventos.
    * Si desea "agregar como evento principal", el evento debe establecerse en público.
6. **Seleccione una plantilla:** A lo largo del lado derecho de la página web hay una lista de imágenes en miniatura de las plantillas disponibles en AltspaceVR. Hay salones de juego, oficinas, espacios de reuniones, espacios de presentación y divertidos espacios de Meetup. Seleccione una que parezca interesante. Si no le gusta, continúe y simplemente cree un nuevo evento con una plantilla nueva. Si desea crear su propio mundo de eventos personalizados, seleccione el **cielo fantástico** como plantilla predeterminada y siga las instrucciones que se indican a continuación para importar su mundo.
7. Seleccionar **Opciones avanzadas**

### <a name="advanced-options"></a>Opciones avanzadas

1. **Promover:** Cada evento requiere dos imágenes de personalización de marca (estas imágenes aparecen en el sitio web de AltspaceVR y no aparecen en el evento dentro de AltspaceVR):
    * **Icono:** La imagen del icono debe ser de 1920 x 1080 píxeles. Esta imagen se escalará a varios tamaños de miniatura y se mostrará en el calendario de eventos AltspaceVR con otros eventos. Asegúrese de que la imagen está clara y no tiene mucho texto. No utilice imágenes/logotipos con derechos de autor que no posea.
    * **Banner:** Las imágenes de banner deben ser 1920x576. Se cambiará automáticamente de tamaño según sea necesario y visible en la página web o la información de eventos. Una superposición semitransparente cubre el 25% inferior de la imagen. Evite colocar texto en esa área.
    * Otra opción (más rápida) consiste en **Copiar la imagen de icono en la imagen de pancarta de fondo**, lo que hará que también se use la imagen de icono como imagen de banner. Asígnele un intento:). Si no tiene buen aspecto, puede crear una nueva imagen de banner.
2. **En VR:** En esta sección se incluyen las características que se aplican a la experiencia virtual durante el evento dentro de la aplicación AltspaceVR:
    * **Roles contextuales predeterminados:** El signo de interrogación verde muestra los roles específicos que están disponibles para *todos los miembros de audiencia en el evento*. Lo más común es *megaphone_only*. Agregue esto para dar la opción "ampliar mi voz" bajo el botón herramientas del host a todos los miembros de la audiencia para que puedan ser oídas en el evento si se trata de un gran espacio. Si el evento requiere vuelo, agregue *Pilot*. Para agregarlos ambos, el formato es: *megaphone_only, piloto*. Cada usuario debe habilitar el modo de marcha en la aplicación AltspaceVR. para ello, vaya a configuración/entrada/marcha.
    * **Instrucciones:** Las [instrucciones](../world-building/adding-welcome-messages.md) son para el texto que genera una imagen de bienvenida al llegar en el espacio. Los usuarios deben seleccionar "Aceptar" para quitarlo de la vista. Esto se suele usar para proporcionar instrucciones a la audiencia, como "Manténgase silenciado hasta que se le invite a hablar" o "Bienvenido al evento XYZ donde vamos a cubrir ABC". Esto no es necesario, por lo que debe usarse con prudencia. También puede usar Markdown para agregar colores y tamaños de fuente, más detalles: [http://digitalnativestudios.com/textmeshpro/docs/rich-text](http://digitalnativestudios.com/textmeshpro/docs/rich-text)
3. **Opciones avanzadas:** A continuación se muestra una explicación rápida de las características avanzadas de los eventos (algunas de estas características no se mostrarán hasta que se cree el evento y se EDITe el evento):
    * **Administradores:** Los administradores son usuarios de AltspaceVR de confianza que le ayudarán a administrar el evento. Pueden ser sus hosts de copia de seguridad o cohosts. Al agregar su nombre de usuario a la lista de administradores, pueden:
        * Cambiar el título, la descripción y otras características del evento.
        * Agregue y quite roles contextuales para moderadores, moderadores y otros roles.
        * Elimine el evento.
    * **Grupo:** Elija entre los [grupos](group-features.md) privados mediante el menú desplegable. Solo mostrará si su cuenta se ha creado o se ha agregado a un grupo.
    * **Subtítulo:** Esta oración concisa se mostrará en la Página Web de eventos bajo el título.
    * **Importar desde el mundo:** Para usar un espacio de eventos del mundo creado para su uso repetido, esta es la sección del formulario que se va a usar para importar el diseño y la personalización del mundo en el evento. Tenga presente las siguientes consideraciones:

    **Importe su propio mundo:** Para importar un mundo, ha creado y posee:
    * Seleccione la flecha desplegable para ver una lista de los mundos que creó.
    * Seleccione el mundo.
    * Después de completar el resto del formulario de eventos, espere al menos 2 minutos antes de visitar el espacio de eventos en AltspaceVR para asegurarse de que se actualiza la información de la base de datos y se genera el mundo.
    
    **Usar el mundo de la otra persona:**
    * Póngase en contacto con el propietario del mundo para solicitarle que use la característica **compartir con amigos** en un mundo individual para compartirla con usted.

3. **Identificador de vídeo de YouTube:** Visible en la página web del evento, agrega finalizadores de eventos de YouTube o vídeos a la Página Web de eventos, no en el mundo. Solo necesitará la parte del identificador de vídeo de la dirección URL: dQw4w9WgXcQ
4. **Identificador de Twitter:** Esto agrega la secuencia de Twitter a la página web del evento. Si la cuenta de Twitter es personal y no está relacionada con el evento o la asociación, puede que esté sobrecargado. Solo necesitará el identificador: @elonmusk
5. **Roles contextuales:** Aquí es donde se controlan las superpotencias o los [roles contextuales](../world-building/granting-roles.md) de los hosts de eventos, presentadores, moderadores y otros roles dentro del evento. Para agregarlas, escriba en su nombre de usuario de AltspaceVR y asígneles un rol en el menú desplegable. Para quitarlos, active la casilla para quitar y guardar la Página Web de eventos. Nota: Si quiere conceder una capacidad de moderación del moderador, debe agregarla como presentador y moderador. Los siguientes roles contextuales están disponibles actualmente:
    * **Presentador:** Agrega las [características](../faqs/front-row-events.md) de la fila de Front a la interfaz de la persona en AltspaceVR para agregar esas características.
    * **Moderador:** Agrega características de moderación a la interfaz de usuario, incluida la capacidad de texto de cada asistente, las silencias de forma global para el evento o las quita del evento. Agregue el presentador de nuevo y asígneles roles de moderación si desea que tengan privilegios de moderación.
    * **Solo megaphone:** Agrega el botón amplificar mi voz a su interfaz a través del botón herramientas del host.
    * **Terraformer:** Agrega el botón del editor mundial a su interfaz.
    * **Piloto:** Agrega capacidades de vuelo para ese individuo. Nota: deben habilitar esto en configuración/entrada/marcha
    * **Rendimiento musical:** Agrega funcionalidades y características asociadas con eventos musicales y concierto.
6. **Bloquear usuarios de la lista:** Si desea impedir el acceso de un usuario, o un usuario ha quitado previamente el evento de un moderador o presentador y el evento está duplicado, se mostrará el nombre del usuario del bloque de la lista. Los hosts o administradores de eventos pueden agregar o quitar un usuario de la lista de bloqueados en cualquier momento.

Una vez que se haya completado el formulario y se haya comprobado triple, seleccione **crear evento**.

> [!IMPORTANT]
> Si el evento no se crea correctamente, asegúrese de que tiene al menos 10 caracteres en la descripción y/o que ha seleccionado una plantilla, el nombre de la plantilla pasará de blanco a azul si está seleccionada.

## <a name="event-page-actions"></a>Acciones de la página de eventos

En la Página Web de eventos, tiene las siguientes acciones y opciones:

1. Seleccione **Editar** para realizar cambios en la configuración de eventos.
2. Seleccione **Finalizar evento** para finalizar el evento (si el evento se encuentra por encima del comienzo, por ejemplo).
3. Seleccione **establecer en borrador** para establecer el evento en borrador en lugar de activo.
4. Si realizó una actualización a su mundo importado, deberá seleccionar volver a importar el **mundo** para que los cambios aparezcan en el evento, no olvide restablecer el espacio en el evento:)
5. Seleccione **duplicar evento** para duplicar el evento para eventos futuros. Este duplicado aparecerá en mis eventos/My draft Events; deberá actualizar el nuevo día/hora y activarlo desde allí.
6. Seleccione **Agregar como evento principal** para establecer el evento en la lista de calendarios.
7. Seleccione **eliminar evento** si desea eliminar completamente el evento (no puede recuperarlo).

Cuando esté listo, vaya al menú **eventos > mis eventos** en la interfaz del mundo de AltspaceVR y escriba el espacio de eventos para restablecer el espacio, inspeccione los cambios o siga personalizando. 

> [!IMPORTANT]
> Esta es una copia y las personalizaciones del espacio de eventos solo son para este evento. Si va a gastar mucho tiempo en personalizar el espacio del evento, es posible que sea mejor crear un mundo para el **evento de uso repetido**.

Para obtener más información sobre cómo personalizar el espacio de eventos o crear un espacio de eventos original para importar:

* [Cómo conceder roles a otras personas en mis mundos?](../world-building/granting-roles.md)
* [Cómo permitir que los usuarios vuelen (o tengan otras capacidades) en mi mundo?](../world-building/adding-user-abilities.md)
* [¿Dónde puedo obtener ayuda con la creación mundial?](../world-building/getting-help.md)
* [¿Cómo administrar mis mundos?](../world-building/managing-worlds.md)
* [Preguntas más frecuentes sobre la creación mundial](../world-building/world-building-faq.md)
* [¿Cómo agregar puntos de generación personalizados a mis mundos?](../world-building/adding-custom-spawn-points.md)
* [¿Cómo cargar mis propios kits?](../world-building/uploading-custom-kits.md)
* [Cómo Introducción al kit de herramientas de creación mundial (cargador de Unity)](../world-building/world-building-toolkit-getting-started.md)

## <a name="using-the-multimedia-console-for-a-slide-presentation"></a>Usar la consola multimedia para una presentación de diapositivas

La consola multimedia es una excelente manera de organizar el contenido de una presentación, como imágenes, audio o vídeo. Siga las [instrucciones de la consola multimedia](multimedia-console.md) para obtener esa configuración para el evento.

## <a name="branding-your-event-with-images"></a>Personalización de marca del evento con imágenes

La adición de imágenes al espacio de eventos o el logotipo y la marca de la empresa, o incluso fotografías de usted, su equipo u otro contenido visual es fácil en AltspaceVR.

Los requisitos de la imagen son los siguientes:
* Se aceptan archivos JPG o PNG
* Tamaño máximo de la imagen: 1920 x 1080
* Solución: 72 ppp
* Tamaño de archivo: menos de 250 KB por archivo

El proceso implica la carga de la imagen en las [fotos de AltspaceVR](https://account.altvr.com/photos)y el uso de las fotos del editor mundial en todo el mundo para importarlas y colocarlas en el espacio de eventos del mundo.

1. Vaya a [fotos](https://account.altvr.com/photos) en el sitio web de AltspaceVR.
2. Seleccione **Cargar**.
3. Seleccione **examinar** para abrir un cuadro de diálogo en el equipo y busque y seleccione la imagen optimizada.
4. Seleccione **Open** (Abrir).
5. Seleccione **crear foto**.
6. Repita este paso para todas las imágenes.

En AltspaceVR y en el mundo del evento, colóquelo cerca de donde desea colocar la imagen. (Si va a crear esto para un **evento de uso repetido**, asegúrese de que se encuentra en su mundo y no en el espacio de eventos).

1. En la interfaz de usuario, en la esquina inferior derecha, seleccione **Editor mundial/panel Editor**
2. Haga clic en la pestaña **mío** en la parte inferior.
3. Seleccione **fotos**.
4. Las fotos se almacenan en orden cronológico de carga, por lo que la imagen más reciente cargada debe ser la primera imagen de la lista. Selecciónelo para agregarlo al mundo.
5. Con el cursor del dispositivo, grabe la imagen y colóquela donde quiera que esté.
    * Puede cambiar su tamaño mediante los controladores (normalmente deslizando el pulgar horizontalmente en el panel táctil en VR o usando el mouse en modo 2D).
    * Para ajustar la posición y la rotación de la imagen, seleccione el símbolo de **engranaje** en la imagen en el editor y establezca la rotación y la posición adecuadamente.
    * También puede cambiar el tamaño de la imagen con la característica de escalado.

> [!NOTE]
> Cuando el modo de edición está activado (texto naranja), tendrá la capacidad de volar de forma automática, lo que facilita el movimiento para colocar imágenes más arriba en el mundo del evento.

6. Repita este paso para cada ubicación de la imagen.
7. Cuando se hayan establecido las imágenes en su lugar, seleccione **bloquear todo** si no las ha bloqueado individualmente y desactive el modo de edición y cierre el editor.
8. Use solo cinco fotos por evento como máximo.

## <a name="adding-3d-objects-using-world-editor-and-kits"></a>Agregar objetos 3D mediante el editor mundial y los kits

AltspaceVR permite importar objetos 3D en mundos con el editor mundial. Hay muchos kits de editores mundiales disponibles actualmente para su uso y mucho más. Hay Spaceships, cohetes, animales animados, Sculptures, árboles, plantas y muchos objetos diferentes. También puede agregar sus propios kits a la colección pública o para su propio uso personal, o bien considerar el uso de una de las [aplicaciones de ALTSPACEVR MRE](../world-building/using-mixed-reality-extensions.md), que aportan objetos interactivos en su mundo como cascos, espadas, alas, ropa, sombreros u otros objetos interactivos. Espere que la lista de objetos se expanda pronto.

Estas instrucciones se centran en el uso de elementos que ya están en los kits. Para obtener más información sobre cómo agregar e importar objetos 3D en AltspaceVR, vea ["cómo importar modelos glTF en mis mundos?"](../world-building/importing-models.md) . y ["Cómo cargar mis propios kits?"](../world-building/uploading-custom-kits.md).

Para agregar un objeto 3D existente desde los kits de construcción del mundo al mundo del evento, con el panel Editor de mundo/editor del editor y el modo de edición habilitados:

1. Explore los kits del objeto que desea importar y selecciónelo.
2. Seleccione en el objeto del kit el cursor y colóquelo. Use el icono de engranaje del objeto en el editor mundial para usar las opciones de posición, rotación y escala para la entrada de número manual.
3. Cuando el objeto se coloque en la posición derecha, haga clic en el icono de candado para bloquearlo.
4. Agregue otro objeto si lo desea. Tenga cuidado al agregar objetos 3D, manteniendo sus selecciones en un máximo de elementos de cinco kits individuales diferentes, para ofrecer un mejor soporte de usuario de Oculus Quest. No use más de 200 objetos en un mundo.
5. Cuando haya terminado, bloquee todos los elementos, desactive el modo de edición y cierre el editor mundial. Moverse. Invite a algunos evaluadores a visitar y desprotegerlos, y prepárese para su fantástico evento.

Para obtener más información sobre los kits del editor del mundo y cómo agregar objetos 3D a AltspaceVR:

* [¿Cuál es el programa de acceso temprano?](../world-building/early-access.md)
* [¿Cómo se importan los modelos glTF en mis mundos?](../world-building/importing-models.md)
* [¿Cómo usar una MRE en mi mundo?](../world-building/using-mixed-reality-extensions.md)

## <a name="how-to-record-or-live-stream-my-event"></a>Cómo grabar o Live Stream My Event

Consulte el siguiente documento de soporte técnico para obtener instrucciones sobre cómo grabar o hacer streaming en vivo de su evento:

* [Cómo grabar o Live Stream My Event](recording-and-live-streaming.md)