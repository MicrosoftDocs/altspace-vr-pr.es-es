---
title: Uso del Interactables
description: Aprenda a crear, usar y personalizar el generador de interactables para colocar elementos en los espacios de AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: generación, interacciones, personalizaciones
ms.openlocfilehash: 7f4b87591b2e11b2084af4d2bf83748ed51fd193
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213923"
---
# <a name="using-the-interactables-spawner"></a>Uso del Interactables

El Interactables generador permite colocar los elementos interactivos en el evento, el mundo o el espacio de inicio. Actualmente, esta característica forma parte de nuestro [programa de acceso temprano](../world-building/early-access.md) y no estará disponible a menos que haya participado en el menú principal.

> [!NOTE]
> Aunque seguimos realizando una prueba piloto de esta característica, tenga en cuenta que la generación de demasiadas interactables puede afectar al rendimiento de su entorno o evento. 

## <a name="creating-an-interactable"></a>Crear un interactuable

Para convertir el objeto en un objeto interactuable:

1. Coloque el objeto en el espacio.
2. A continuación, busque la entrada en la lista de objetos y seleccione el **icono de engranaje** situado junto a ella para abrir su configuración:

![Editor mundial abierto con la lista de objetos resaltada](images/interactables-spawner-img-01.png)

En la página Configuración encontrará una nueva casilla **"objeto de generación de objetos"**, que se usa para convertirla en un objeto interactuable.

1. Active la casilla y seleccione **confirmar**.
2. En el modo de edición, puede desplazarse por la ubicación de generación del objeto en el espacio.
3. **Salga del modo de edición** para habilitar la interacción del elemento.

![Ventana actualizar artefacto abierta en la aplicación AltspaceVR](images/interactables-spawner-img-02.png)

## <a name="other-customizations"></a>Otras personalizaciones

Después de habilitar **"objeto de generación de objetos"** cuando vuelva a las propiedades de ese objeto, habrá una configuración adicional que se puede aplicar a la forma en que se comporta el objeto generado.

> [!NOTE]
> Escala de objetos interactivos: Esto establece la escala del objeto cuando se selecciona, en comparación con "escala", que es la escala de cómo aparece el objeto en el mundo antes de seleccionarlo por primera vez.

Los responsables del kit pueden observar que los cambios en el kit mientras AltspaceVR se está ejecutando no surtirán efecto hasta que reinicie AltspaceVR.

Recientemente hemos agregado un botón en la pestaña **configuración moderada** denominada **recargar los kits de mundos**. Al hacer clic en este botón, se hace que (solo usted) vuelva a escribir el espacio y vuelva a cargar todos los kits, lo que descargará solo las nuevas versiones de los kits que se han actualizado mientras estaba en AltspaceVR.

![Panel de configuración moderada abierto en la aplicación AltspaceVR](images/interactables-spawner-img-03.png)