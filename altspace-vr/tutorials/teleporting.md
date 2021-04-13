---
title: Uso del teletransportarr
description: Obtenga información sobre cómo viajar de un evento o un mundo a otro mediante un telepuerto en AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: teletransportador
ms.openlocfilehash: afc199e958824bb5f0a9ff6d74865cbcd3f16868
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213858"
---
# <a name="using-the-teleporter"></a>Uso del teletransportarr

Viajar de un evento o un mundo a otro es una excelente manera de que usted y la comunidad exploren todo lo que AltspaceVR tiene que ofrecer.

## <a name="the-short-version"></a>La versión abreviada

![Migrar los pasos del panel Editor a un destino de teleportabilidad](images/teleporter.png)

## <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

En primer lugar, asegúrese de que se encuentra en el Homespace, en un evento o mundo que haya creado o al que se le haya dado el rol Terraformer en. Si está en modo 2D y no ve el botón del editor mundial situado en la parte inferior derecha de la interfaz de usuario, haga clic con el botón secundario en el botón del mouse para activar o desactivar. Si sigue sin ver el botón del editor mundial, puede que esté en el espacio de otra persona. Si ese es el caso, pida al host que le proporcione el rol Terraformer.

También le ayudará a: 
1. Crear primero los eventos o mundos
2. Vaya a la ubicación en la que desea crear el teletransportador, de modo que los eventos/mundos se rellenen en el panel de destino de teleportabilidad y resulte más rápido y sencillo de conectarlos.

Otro truco para ayudarle a navegar por los teletransportadores en modo 2D es usar CTRL + barra espaciadora. Se abrirá el símbolo del sistema y podrá escribir: atrás, que le llevará al último espacio en el que se encontraba. 

Ahora, vaya a la ubicación en la que desea generar un teletransportador y seleccione en el editor internacional/panel Editor/conceptos básicos/teleusuario.

Se abrirá el panel destino de teleportabilidad. Verá tres categorías entre las que puede elegir:

* **Mis espacios** : lista de mundos que ha creado.
* **Reciente** : lista de eventos recientes que ha estado. Utilice esta opción si desea desplazarse a un evento, esta es la única opción que le llevará a un evento, mientras que los otros 2 solo le permiten viajar entre mundos. Nota: Consulte Opciones avanzadas si está conectando eventos de Front Row que han importado mundos, deberá generar y configurar los teletransportadores en el mundo importado y no en el evento real.
* Lista **destacada** de mundos destacados, puede establecer el telepuerto en el que va a viajar.

Seleccione el evento o el mundo que quiere usar, que generará el teletransportar y colocará una etiqueta de texto con el nombre del evento o del mundo ligeramente detrás. Por lo tanto, puede seleccionar el icono de engranaje en la sección objetos presentes para cambiar el nombre de la etiqueta.

Puede seleccionar en el teletransportador con el cursor (se le preguntará si está de viaje, en caso de que se tratase de un error) o trasladar el Avatar directamente al telepuerto y, presto, está viajando a su destino. Dígales que dicen Hola.

## <a name="advanced-features"></a>Características avanzadas

Si va a crear un evento de conferencia, cumbre o mayor con un mundo personalizado (por ejemplo, un mundo de la Fundación, una plantilla de espacio de cargador de Unity, Re-Import mundo), deberá configurar el telepuerto en el mundo de la Fundación y no en el evento real. Asegúrese de que está configurando el teletransportador para viajar al evento correcto (debe ser de la lista de recientes) en el mundo de la Fundación y, a continuación, Re-Import mundo en el evento para que los teletransportantes se muestren en todos los espacios de eventos de las filas.

## <a name="faqs"></a>Preguntas más frecuentes

**Error: "lo sentimos, nos gustaría, pero simplemente no podemos permitirle hacerlo"**

El evento podría tener un grupo adjunto, por lo que solo los nombres de usuario del grupo pueden llegar a ese telepuerto para llegar a ese evento de grupo privado.

**¿Cuántos teletransportadores puedo usar en un solo espacio?**

Los teletransportadores usan texturas transparentes con efectos de partículas animados, por lo que es mejor no tener demasiados en el mismo lugar o superposición, ya que esto podría afectar al rendimiento. Intente no tener más de 4 en la misma área o más de 10 si están repartidos en el espacio.