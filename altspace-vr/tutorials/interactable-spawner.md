---
title: Uso del spawner Interactables
description: Obtenga información sobre cómo crear, usar y personalizar el elemento de generación interactuable para colocar elementos en los espacios AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: spawner, interacciones, personalizaciones
ms.openlocfilehash: abeddec5c2b50e0612db5efb6bc2e3c5bd9de4a8b67c50b19afee18b17c5e746
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127407"
---
# <a name="using-the-interactables-spawner"></a>Uso del spawner Interactables

Interactables Spawner permite colocar elementos interactuables en el evento, el mundo o el espacio de inicio. Esta característica forma parte actualmente de [nuestro](../world-building/early-access.md) Programa de acceso anticipado y no estará disponible a menos que haya participado en el menú principal.

> [!NOTE]
> Aunque seguimos piloto de esta característica, tenga en cuenta que la generación de demasiados interactuables puede afectar al rendimiento de su entorno o evento. 

## <a name="creating-an-interactable"></a>Creación de un elemento interactuable

Para convertir el objeto en un objeto interactable:

1. Coloque el objeto en el espacio.
2. A continuación, busque la entrada en la lista de objetos y seleccione el icono **de engranaje** junto a ella para abrir su configuración:

![Editor del mundo abierto con la lista de objetos resaltada](images/interactables-spawner-img-01.png)

En la página de configuración encontrará una nueva casilla **"Object spawner"**(Generador de objetos), que se usa para convertirla en un objeto interactuable.

1. Active la casilla y seleccione **Confirmar**.
2. Mientras está en modo de edición, puede desplazarse por la ubicación de generación del objeto en el espacio.
3. **Salga del modo de edición** para habilitar la interacción de elementos.

![Ventana actualizar artefacto abierta en la aplicación AltspaceVR](images/interactables-spawner-img-02.png)

## <a name="other-customizations"></a>Otras personalizaciones

Después de **habilitar "Object spawner"** (Generador de objetos) al volver a las propiedades de ese objeto, habrá una configuración adicional que puede aplicar a cómo se comporta el objeto generado.

> [!NOTE]
> Escala de objetos interactuable: establece la escala del objeto cuando se recoge, en comparación con "Escala", que es la escala de cómo aparece el objeto en el mundo antes de seleccionarlo por primera vez.

Es posible que los creadores del kit observen que los cambios en el kit mientras se ejecuta AltspaceVR no se realizarán hasta que reinicie AltspaceVR.

Recientemente hemos agregado un botón en la pestaña **Moderador Configuración** llamada **Reload Worlds Kits (Volver** a cargar kits de mundos). Al hacer clic en este botón, (solo usted) volverá a entrar en el espacio y volverá a cargar todos los kits, lo que descargará solo las nuevas versiones de los kits que se han actualizado mientras estaba en AltspaceVR.

![Panel de configuración moderado abierto en la aplicación AltspaceVR](images/interactables-spawner-img-03.png)