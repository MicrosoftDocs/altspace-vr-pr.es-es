---
title: Adición de puntos de generación personalizados
description: Aprenda a crear, agregar y solucionar problemas de los puntos de generación personalizados en AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: spawnpoint, solución de problemas
ms.openlocfilehash: 53ff2e60d929aed9be5650b132da6d1dab8e6f1c5a78425dc5f17c10f2c4dfdb
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127269"
---
# <a name="adding-custom-spawn-points"></a>Adición de puntos de generación personalizados

Las personas que  entran en su mundo se generan o aparecen en el origen, la posición (0,0,0), cuando entran en su mundo. Sin embargo, puede agregar uno o varios puntos de generación si quiere, por ejemplo, hacer que las personas comiencen en la entrada a su casa. Si especifica varios puntos de generación, se elegirá uno aleatoriamente cada vez que alguien entre y no se incluya el origen. Puede administrar puntos de generación en cualquier mundo o evento en el que esté habilitado el Editor del mundo. Puede controlar dónde se generan las personas (posición) y a qué dirección se enfrentarán (rotación). Los puntos de generación solo estarán visibles en el modo de edición. 

1. Vaya cerca del lugar donde desea que se desa generar la gente. Abra **World Editor > Basics (Conceptos básicos** de World Editor) y asegúrese de que la opción Rotación de **bloqueos** está activada. Seleccione **Punto de generación** para crear uno. Muévelo a la posición exacta que desee:

![Ventana Conceptos básicos del editor del mundo abierta](images/spawn-points-img-01.png)

2. Seleccione el icono de configuración del punto de generación y asegúrese de que **rotation > X** y Rotation > **Z** son **0.** Si son números pequeños como **8,537777745E-07,** también está bien. Es una quirk de cómo se controlan los números de punto flotante:

![Actualización de puntos de generación en la configuración del editor mundial](images/spawn-points-img-02.png)

3. Volver a escribir el mundo a través **del menú > Configuración > general > volver a escribir espacio > volver a entrar**
4. Debe generar en el nuevo punto de generación.
5. Si desea que las personas se aleen en otra dirección, seleccione la configuración del punto de generación y establezca **Rotación > solo Y.** Intente establecer Y en 180 y X y Z en 0 (advertencia: X y Z están avanzados puede hacer que las personas se vuelvan mal). A **continuación, seleccione** Confirmar y vuelva a escribir el mundo. Esto debería generar que se enfrentase a la dirección opuesta. 

## <a name="troubleshooting"></a>Solución de problemas

**¿Las personas siguen generando en el origen?**
    * Asegúrese de que los puntos de generación están ligeramente por encima del suelo o la superficie. Si el punto de generación se superpone a otros objetos, las personas se generan en la ubicación predeterminada, el origen. Esto puede ocurrir si el punto de generación dentro de un objeto y la altura de la persona varía. 
    * Pruebe a restablecer el mundo a través del **menú > Configuración > moderar > restablecer espacio**

**¿Tiene varios puntos de generación pero sigue generando en el mismo lugar?**
Es posible que no tenga suerte, es aleatorio después de todo. Pruebe a volver a escribir al menos cinco veces antes de suponer que hay un error. 

**Las personas no están cómodas o su cabeza inclinada** Es posible que haya olvidado comprobar **rotación de bloqueos** o establecer el valor X y Z para Rotación. Normalmente, se deben establecer en 0, a menos que esté creando un mundo insólo. 

**¿Las personas se caían cuando se generan?**
No establezca la posición del punto de generación demasiado alta sobre un objeto. Si están demasiado lejos, se volverán a abrir en el origen.