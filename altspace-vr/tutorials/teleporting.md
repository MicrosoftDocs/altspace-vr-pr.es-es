---
title: Uso del teleportador
description: Aprenda a viajar de un evento o un mundo a otro mediante un teleportador en AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Teletransportador
ms.openlocfilehash: 79c5b09e1643a70939ba1e967a948ac6c80c2b615bce9eef598d0e07b7722ea3
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126195"
---
# <a name="using-the-teleporter"></a>Uso del teleportador

Viajar de un evento o de un mundo a otro es una excelente manera para que usted y la comunidad exploren todo lo que AltspaceVR tiene para ofrecer.

## <a name="the-short-version"></a>La versión corta

![Pasos de teleportación desde el panel del editor para establecer un destino de teleportación](images/teleporter.png)

## <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

En primer lugar, asegúrese de que está en su espacio principal, en un evento o un mundo que haya creado o en el que se le haya dado el rol terraformer. Si está en modo 2D y no ve el botón Editor del mundo situado en la parte inferior derecha de la interfaz de usuario, haga clic con el botón derecho en el botón del mouse para activar o desactivarlo. Si todavía no ve el botón Editor del mundo, es posible que esté en el espacio de otra persona. Si ese es el caso, pida al host que le dé el rol terraformer.

También le ayudará a: 
1. Creación de eventos o mundos en primer lugar
2. Vaya a donde quiera generar el teleportador, para que los eventos o mundos se rellenen en el panel Destino del teleportador y que sea más rápido y fácil conectarlos.

Otro truco para ayudarle a navegar con teleportadores en modo 2D es usar Ctrl + Barra espaciadora. Se mostrará el símbolo del sistema y puede escribir: back -That will take you back to the last space you were in. 

Ahora, muévese a la ubicación en la que desea generar un teleportador y seleccione en Editor del mundo/ Panel del editor / Aspectos básicos / Teleporter.

Se mostrará el panel Teleporter Destination (Destino del teleportador). Verá tres categorías entre las que elegir:

* **MY SPACES:** lista de mundos que ha creado.
* **RECIENTE:** lista de eventos recientes a los que ha estado. Use esta opción si desea viajar a un evento, esta es la única opción que le llevará a un evento; las otras 2 solo le permiten viajar entre mundos. NOTA: Consulte Opciones avanzadas a continuación si va a conectar eventos de front-row que tienen mundos importados, deberá generar y configurar los teleportadores en el mundo importado y no en el evento real.
* **DESTACADO:** lista de mundos destacados al que puede establecer el teleportador al que va a viajar.

Seleccione el evento o el mundo que desea usar, lo que genera el teleportador y coloca una etiqueta de texto con el nombre del evento o del mundo ligeramente detrás. Por lo tanto, puede seleccionar el icono de engranaje en la sección Present Objects (Presentar objetos) para cambiar el nombre de la etiqueta.

Puede seleccionar en teleportador con el cursor (se le preguntará si está bien ir allí, en caso de que se haya hecho clic en un error de clic) o mover el avatar directamente al teleportador y, prescindió, se desplaza a su destino. ¡Cuénteles que diga hola!

## <a name="advanced-features"></a>Características avanzadas

Si va a crear una conferencia, una conferencia o un evento más grande mediante Front Row con un mundo personalizado (por ejemplo, un mundo base, una plantilla de espacio de carga de Unity, Re-Import World), deberá configurar el teleportador en foundation world y NO en el evento real. Asegúrese de configurar el teleportador para que viaje al evento correcto (debe estar en la lista Recientes) en foundation world y, a continuación, Re-Import World en el evento para que los teleportadores se muestren en todos los espacios de eventos de front-row.

## <a name="faqs"></a>Preguntas más frecuentes

**Error: "Lo sentimos, nos gustaría, pero no podemos permitir que entre ahí".**

El evento podría tener un grupo asociado, por lo que solo los nombres de usuario del grupo pueden acceder a ese teleportador para llegar a ese evento de grupo privado.

**¿Cuántos teleportadores puedo usar en un solo espacio?**

Los teleportadores usan texturas transparentes con efectos de partícula animados, por lo que es mejor no tener demasiados en el mismo punto o superposición, ya que esto podría afectar al rendimiento. Intente no tener más de 4 en la misma área o más de 10 si todos están distribuidos en su espacio.