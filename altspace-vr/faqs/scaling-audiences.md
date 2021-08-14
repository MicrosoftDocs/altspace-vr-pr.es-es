---
title: Escalado de audiencias con la característica FrontRow
description: Aprenda a habilitar, solucionar problemas y escalar las audiencias de AltspaceVR con la característica FrontRow.
ms.date: 03/11/2021
ms.topic: article
keywords: escalado, front-row
ms.openlocfilehash: 3b6a518a463fc373439f411d4ae75352a0343304b1fb73c8848d3bfd5fa19973
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128075"
---
# <a name="scaling-your-audiences-with-frontrow-feature"></a>Escalado de audiencias con la característica FrontRow

## <a name="what-is-frontrow"></a>¿Qué es FrontRow?

FrontRow es una tecnología AltspaceVR que permite que todo el evento se "refleja" en varias instancias. FrontRow permite escalar la audiencia más allá de los límites de habitación individuales y se puede usar para dar cabida a públicos grandes en un solo evento. Sin FrontRow, el tamaño de la audiencia se limitará al límite de habitación del entorno principal.

## <a name="how-does-it-work"></a>¿Cómo funciona?

FrontRow agrega características y capacidades adicionales a la experiencia de host, lo que le proporciona el máximo control sobre el evento y la audiencia. 

* La **herramienta En el aire** se agrega al panel host.
    * Con **On-Air,** puede elegir quién desea "reflejar" (por ejemplo, presentadores, intérpretes, panelistas, miembros del público, entre otros) FrontRow también "refleja" contenido en todas las salas. Por lo tanto, si tiene un panel de oradores y una presentación de diapositivas, puede "reflejar" los oradores y la presentación en todas las salas de FrontRow.
* Se **abre** una pestaña Salas en el Panel de invitados.
    * En este panel se proporciona información general de un vistazo sobre cuántas salas tiene, cuántos invitados hay en cada habitación y quiénes son esos invitados. Desde aquí, también puede  elegir  Agregar sala o Eliminar sala para que pueda administrar el tamaño de la configuración que mejor se adapte a su evento.
    * Puede teleportar de una habitación a otra y distribuir fácilmente los moderadores entre los espacios.
* Distribución de audiencia reactiva
    * A medida que los invitados comienzan a entrar en el espacio, FrontRow los distribuirá intuitivamente. Se puede configurar para rellenar una sala a la vez o para rellenar simultáneamente varias salas para una distribución de audiencia más uniforme.

## <a name="when-to-enable-frontrow"></a>Cuándo habilitar FrontRow

Convierta a FrontRow cuando necesite escalar más allá de la capacidad de la sala del entorno.

* Los entornos oficiales de plantilla altspaceVR permiten un máximo de 50 avatares por espacio. Si espera un público mayor que 50, use FrontRow para crear varias salas de 50 avatares.
* Custom Words (Unity Uploader/Custom Space Templates), también permite un máximo de 50 avatares por espacio si se usa como entorno de eventos. Si espera una audiencia superior a 50, use FrontRow para crear varias salas de 30 avatares.

## <a name="how-to-enable-frontrow"></a>Habilitación de FrontRow

1. [Cree el evento](https://account.altvr.com/events/new).
2. Escriba el evento.
3. Una vez dentro del evento, abra **Herramientas de host** en la esquina inferior derecha.
4. Seleccione en el **botón Panel de** participación.
5. Vaya a la **pestaña Salas** y, desde aquí, puede **agregar habitación.**
    * Tenga en cuenta que puede tardar hasta 30 segundos en generar otra habitación. 
6. Una vez abierta la nueva sala, verá que aparece en la **pestaña** Salas. 

## <a name="how-to-use-frontrow"></a>Uso de FrontRow

Al convertir el evento en un evento de FrontRow, se agregan algunas herramientas y capacidades adicionales al panel host. En concreto, aparecerá **una pestaña** Salas. En esta pestaña, puede hacer lo siguiente:

* **Agregar sala:** agregue una sala adicional al evento. 
* **Eliminar sala:** quite una sala completa del evento.
* **Restablecer espacio:** restablezca la sala que ha seleccionado. Esto hace que los invitados vuelvan a entrar en el mismo espacio.
* **Redistribuir:** redistribuya todos los invitados que se encuentran actualmente en una habitación a otras salas. (Buena para la aglomeración).
* **Teleport:** vaya a otra habitación.

En un evento FrontRow, los hosts también verán otras herramientas y características como **On-Air.** Este botón, situado junto a **Herramientas** de host, permite a un host o moderador reflejar a los miembros de la audiencia y a otros participantes para que puedan estar visibles en todos los espacios. (Como host, es probable  que también quiera estar en el aire. (Pro sugerencia: [Use zonas host](https://altvr.com/holiday2020/) para habilitar automáticamente El aire para cualquier persona dentro de la zona).

Consulte el artículo Información general de las herramientas de host para eventos de [FrontRow](../tutorials/host-tools-for-events.md) para obtener una visión completa y detallada de cada una de las características y funciones disponibles para los hosts en los eventos de FrontRow.

![Introducción a las herramientas del panel host](images/scaling-audiences.png)

Si necesita ayuda a lo largo del proceso, envíe una entrada a nuestro equipo de soporte técnico en [altvr.com/eventsupport](https://help.altvr.com/hc/en-us/requests/new?ticket_form_id=360001833313)

* Incluya la dirección URL del identificador de evento (por ejemplo: [https://account.altvr.com/events/1461193283454632537](https://account.altvr.com/events/1461193283454632537) )
    * Para obtener esto, puede iniciar sesión en nuestro sitio web www.altvr.com, ir a Eventos/Mis *eventos/* Su evento y copiar la dirección URL en la barra de direcciones del explorador o hacer clic en el botón COMPARTIR para obtener la dirección URL.
    * La respuesta del vale puede tardar entre 3 y 5 días laborables, por lo que debe enviar la solicitud con la mayor antelación posible.
 
## <a name="how-will-i-know-when-frontrow-is-on"></a>¿Cómo puedo saber cuándo está en servicio FrontRow?

Sabrá que el evento se ha convertido una vez que empiece a ver otras salas agregadas a la **pestaña** Salas. Si quieres 
 
## <a name="can-i-turn-off-frontrow"></a>¿Puedo desactivar FrontRow?

Seguro que sí. Puede eliminar **sala tan** fácilmente como puede agregar **habitación.** El **botón Eliminar** sala se encuentra junto a cada una de las salas de la **pestaña** Salas. Al eliminar una sala con personas en ella, FrontRow le notificará la eliminación y las redistribuirá a otras salas activas. Al escalar el evento hasta llegar a una sola sala, se desactiva FrontRow de forma eficaz. 
 
## <a name="any-pro-tips-or-helpful-hints-to-be-aware-of"></a>¿Hay sugerencias profesionales o sugerencias útiles que tener en cuenta?

La configuración de un evento depende de diferentes factores. Aunque no hay una fórmula exacta para el éxito, estas son algunas sugerencias profesionales y sugerencias útiles al hospedar eventos (FrontRow o no) en AltspaceVR:
* Piense en la experiencia de su audiencia y haga lo que puede optimizar para todos. Por ejemplo, si el entorno no es compatible con dispositivos móviles, puede perder la experiencia de alguien con un casco móvil. Para aumentar la audiencia, quiere dar una primera impresión excelente.
* La práctica hace al maestro. Antes de hospedar un evento en directo, realice tantos run-throughs como sea posible. Asegúrese de que se siente cómodo con todas las herramientas a su alcance para que pueda estar seguro cuando esté en el primer plano. Si el evento incluye actores (hablantes o intérpretes) también los incluye en los run-throughs.
* Evite los cambios de último minuto. Puede parecer tentador quitar una suma o reorganizar la configuración del evento minutos antes de la hora de inicio. pero puede estar a un clic de distancia de un cambio importante en el evento. 
* No olvide la moderación. Revise las herramientas de moderación (Kick, Report, Block, Mute), asigne moderadores para ayudar a mantenerse al tanto y compartir las reglas del evento con sus invitados. Recuerde que es posible que las personas que no están nunca en la realidad virtual no siempre sepan cuáles son las normas sociales de las reuniones virtuales.