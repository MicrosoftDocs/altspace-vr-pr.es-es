---
title: Concesión de roles de mundo
description: Obtenga información sobre el sistema de roles y capacidades y obtenga instrucciones paso a paso para dar a los usuarios roles en sus mundos altspaceVR.
ms.date: 04/14/2021
ms.topic: article
keywords: roles
ms.openlocfilehash: f299f637d77c989be5504532279fb42451367b4ac53095d00627f67402dd8552
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127130"
---
# <a name="granting-world-roles"></a>Concesión de roles de mundo

Altspace tiene un sistema roles y capacidades. Cada persona puede tener varios roles y sus roles pueden ser diferentes en función de dónde estén. Cada rol, a su vez, le proporciona una o varias capacidades. Por ejemplo, cuando se encuentra en su propio evento, recibe automáticamente los **roles host** **y moderador.** Con esos dos roles puede poner en marcha a los usuarios desenfasados, estar en el escenario y, quizás, liberar el confconfeso.

1. Edite su mundo y busque en la columna derecha **roles contextuales** [(Cómo administrar mundos)](managing-worlds.md)

![Cambio de roles en la sección Roles contextuales de los mundos](images/granting-roles.png)

2. Haga **clic en Agregar** usuario en el campo Roles **contextuales** si desea conceder roles específicos a usuarios específicos solo para este mundo. Por ejemplo, si quiere proporcionarme **el moderador de host**, agregaría lo anterior y  +  seleccionaría **Guardar**. El formato es username **,** username no tiene en cuenta mayúsculas de minúsculas, elija el rol en el menú desplegable **Terraformer,** haga clic en Agregar usuario varias veces para seguir agregando más usuarios y, a continuación, haga clic en **Actualizar.**

* Para que el cambio suba efecto en Altspace, debe restablecer el espacio en el mundo, lo que obliga a todos a volver a unirse o hacer que cada usuario con un nuevo rol se vuelva a unirse al mundo.

3. Edite **el campo Roles contextuales** predeterminados, en la sección En **REALIDAD** virtual, si desea conceder un rol a todos los usuarios que se unan a su mundo. Por ejemplo, si quiere permitir que los usuarios vuelen y usen el megáphone para que puedan escucharse mientras están lejos, agregue lo siguiente:

```
pilot,megaphone_only
```

Después de seleccionar **Actualizar**, Restablecer espacio en el mundo. Esto solo afectará a este mundo. Si desea conceder roles a un universo completo, edite los mismos campos en el universo. Lo mismo ocurre con los eventos, si quiere que todos los miembros del evento tengan estos roles, deberá agregarlo a los **roles contexuales** predeterminados del propio evento.

## <a name="roles"></a>Roles

* **Megaphone_only:** capacidad de hablar en los oídos de los usuarios dondequiera que estén en el mundo
* **Moderator:** capacidades como **kick** para mantener el decoro
* **Piloto:** capacidad para alternar el modo de vuelo y generar la herramienta de vuelo 6DOF
* **Host:** capacidades como poder estar en el escenario, tener megáphone
* **Terraformer:** capacidad de usar el Editor del mundo Más información sobre ([Roles en eventos, mundos, grupos y en AltspaceVR)](../getting-started/roles.md)

## <a name="troubleshooting"></a>Solución de problemas

**¿Puedo eliminar roles?**
Sí, edite su mundo, haga clic en **Quitar** debajo del rol que desea eliminar y haga clic en **Actualizar.**

**¿Se copian los roles cuando un mundo importa desde otro?**
No, los roles no se copian