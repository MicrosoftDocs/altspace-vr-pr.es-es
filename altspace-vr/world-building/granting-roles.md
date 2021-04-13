---
title: Conceder roles mundiales
description: Obtenga información sobre el sistema de roles y capacidades y obtenga instrucciones paso a paso para conceder a los usuarios roles en sus AltspaceVR mundos.
ms.date: 03/11/2021
ms.topic: article
keywords: roles
ms.openlocfilehash: f8cd55fbd8ede6cedd199724a3e6b2413c5bc3e6
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213690"
---
# <a name="granting-world-roles"></a>Conceder roles mundiales

Altspace tiene un sistema de roles y capacidades. Cada persona puede tener varios roles y sus roles pueden ser diferentes en función de dónde se encuentren. Cada rol, a su vez, proporciona una o más capacidades. Por ejemplo, si se encuentra en su propio evento, recibirá **automáticamente los roles de** Moderador y **moderador** . Con esos dos roles, puede poner en marcha usuarios impropios, estar en fase y puede liberar el confeti. 

1. Edite su mundo y desplácese hacia abajo hasta la sección **en VR** ([Cómo administrar mundos](managing-worlds.md))

![Cambiar roles en la sección de en la VR](images/granting-roles.png)

2. Edite el campo **roles** si desea conceder roles específicos a usuarios específicos solo para este mundo. Por ejemplo, si desea que el moderador del **presentador** le proporcione el moderador de  +   un dedo, debe agregar lo siguiente y seleccionar **Guardar**.  El formato es **{role}, {username o email}** en cada línea. Username no distingue mayúsculas de minúsculas. 

```
presenter,jimmy
moderator,jimmy
moderator,calen
```

3. Si vuelve a seleccionar **Editar** , debería ver lo siguiente sobre el campo roles. Así es como sabe actualizar en la base de datos.

```
Presenters: jimmy
Moderators: jimmy,calen
```

* Para que el cambio surta efecto en Altspace, debe restablecer el mundo, de forma que todos los usuarios puedan volver a unirse. A continuación encontrará una lista completa de los roles.

4. Edite el campo **roles contextuales** si desea conceder un rol a cada uno de ellos que se una a su mundo. Por ejemplo, si desea permitir que las personas vuelen y usen el megaphone para que puedan escucharse entre sí mientras están en parte, agregue lo siguiente:

```
pilot,megaphone_only
```

Después de seleccionar **Actualizar**, restablezca el mundo. Esto solo afectará a este mundo. Si desea conceder roles a un universo completo, edite los mismos campos en el universo. 

## <a name="roles"></a>Roles 

* **Presentador** : capacidades como poder estar en fase
* **Moderador** : capacidades como **Kick** to maintain Decorum
* **Terraformer** : capacidad de usar el editor mundial
* **Piloto** : capacidad para alternar el modo de vuelo y generar la herramienta 6DOF Flight
* **Megaphone_only** : capacidad de hablar con los oídos de los usuarios dondequiera que se encuentren en el mundo.
* **Showcase_new_sdk** : capacidad de generar aplicaciones de SDK de MRE

## <a name="troubleshooting"></a>Solución de problemas

**¿Puedo eliminar roles?**
No desde el formulario ahora mismo para que el archivo a Support Request en help.altvr.com y nos encargaremos de ello.

**¿Se copian roles cuando un mundo importa desde otro?**
No, los roles no se copian