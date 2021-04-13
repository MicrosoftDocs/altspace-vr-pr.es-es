---
title: Mejorar el rendimiento del mundo
description: Obtenga información sobre cómo medir, solucionar problemas y mejorar el rendimiento de los mundos de AltspaceVR con las herramientas de diagnóstico.
ms.date: 03/11/2021
ms.topic: article
keywords: rendimiento, solución de problemas
ms.openlocfilehash: 558ce2e089aecc206445c6b7bf99423f2d5c45cc
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213651"
---
# <a name="improving-world-performance"></a>Mejorar el rendimiento del mundo

Queremos que los usuarios tengan una buena experiencia con el fin de obtener el mejor rendimiento, o de lo bien que su mundo se ejecute en auriculares VR, es importante en gran medida. Nuestro sistema de compilación mundial está diseñado para un rendimiento excelente en los casos de uso más comunes. Si quiere maximizar la presencia, esta guía es para usted. Altspace aspira para admitir todas las plataformas de hardware. Aunque recomendamos que los creadores del mundo inserten los límites, en el caso de los mundos públicos, le recomendamos que se dirija a Oculus Quest y a cualquier plataforma basada en PC como Windows Mixed Reality, Oculus Rift/Rift S o HTC Naopak. Para simplificar la ejecución, si su mundo se ejecuta correctamente en una solicitud, probablemente sea excelente para Altspace.

## <a name="tools-and-measurement"></a>Herramientas y medición

Diagnósticos de administrador es una herramienta sin conexión disponible en nuestro sitio web, altvr.com. Si navega a [mundos > mis mundos](https://account.altvr.com/users/sign_in), encuentra su mundo y selecciona "diagnósticos", verá algo parecido a esto:

![Ventana de diagnóstico de administrador](images/performance.png)

Estas son directrices más que los requisitos. El rendimiento depende de cuántos objetos tenga y cómo estén organizados. Por ejemplo, si tiene 500 objetos distribuidos en 2 kilómetros, es probable que el rendimiento sea correcto. Sin embargo, si coloca los mismos objetos 500 en un área empaquetada estrechamente, es probable que vea problemas. Esto se debe a que el rendimiento depende de lo que haya en el campo de vista de una persona. La mejor manera de probar es pasar a Altspace y teletranspórtate en todo el mundo. Si observa algún problema o se siente inconveniente, estos son los puntos problemáticos que desea investigar.

Al adjuntar estas recomendaciones, se configura para que se realice correctamente. Vamos a repasar este diagnóstico de ejemplo tomado de un mundo destacado real: 

* **Objetos** : número total de objetos del mundo. Todo es un objeto: artefactos, fotos, puntos de generación, etc. Se recomienda permanecer bajo cierto número pero es flexible. Si realiza la conmutación, indicamos nuestro problema con un signo de exclamación amarillo, como se muestra aquí. Sin embargo, en este caso, hay dos áreas independientes en este mundo, por lo que la densidad no es alta.
* **Kits** : número total de kits de creación mundial únicos usados. Esto afecta al tiempo de descarga inicial al cargar el mundo. Los kits contienen artefactos, el menú de los objetos que se pueden generar en el mundo. 

> [!NOTE] 
> Si se usa un solo artefacto de un kit, es necesario descargar los recursos de ese kit. Por tanto, es muy caro usar solo algunos artefactos de un único kit. 

* **Kits: móvil** : tamaño total de todos los recursos del kit que una persona de una solicitud tiene que descargar antes de entrar en el mundo. Intente no hacer que las personas esperen 5 minutos para descargar todo lo que necesitan para su mundo.
* **Fotos** : número total de fotografías usadas, que suelen tener un mayor impacto en el rendimiento que los artefactos. Úselo con moderación.
Plantilla--móvil: Si usa el cargador de Unity, mantenga el tamaño de la descarga bajo.
* **SKYBOX--Mobile** : Si usa skyboxes personalizado, mantenga el tamaño de archivo pequeño para que los usuarios no obtengan "pantalla en negro" (quedarse sin memoria de vídeo).
* **Kits/artefactos que faltan o no son válidos** : referencias a artefactos o kits problemáticos... ¿Tiene una idea para una métrica? ¡Díganoslo!
De nuevo, estos no son requisitos, por lo que se muestran los iconos de estado verde, amarillo y rojo. Incluso un mundo con una gran cantidad de indicadores rojos todavía puede aparecer. Probaremos en Altspace, por lo que también debe hacerlo. [Si necesita ayuda, puede ponerse en contacto con nosotros](getting-help.md). 

## <a name="load-time"></a>Tiempo de carga

Cuando una persona comienza a viajar a su mundo (intenta entrar), primero cargará la plantilla. Descargarán los recursos de la plantilla (archivos) para su plataforma y verán el "entorno de carga". A continuación, se descargarán los recursos de SKYBOX y kit. Por último, cargarán todos los objetos mientras ven "cargando objetos". La descarga de todos los recursos puede tardar unos minutos, en función de su ancho de banda de Internet, la carga de objetos es bastante rápida. Aunque los recursos se descargan de servidores rápidos en todo el mundo, Altspace usa técnicas de almacenamiento en caché para evitar la redescarga de los mismos archivos repetidamente. Técnicamente, el tiempo de carga inicial no afecta al rendimiento de una persona una vez que entran en el mundo, sino que es parte de la experiencia global, por lo que se intenta no hacer que la gente espere demasiado tiempo al viajar a su mundo. Se recomienda pensar detenidamente en qué kits usar y imaginativas con menos.

## <a name="troubleshooting-and-tips"></a>Solución de problemas y sugerencias

Los **usuarios ven una "pantalla negra"** Normalmente, esto se debe a que el dispositivo se quedó sin memoria de vídeo. Intente reducir el número de objetos en el área de problemas del mundo y reduzca el tamaño de las cosas como el skybox o la plantilla o el número de fotografías. Esos tipos tienden a tener el mayor impacto en el uso de memoria de vídeo.

**Los usuarios se bloquean**
    * A veces, un artefacto o un kit rotos pueden causar esto.
    * Los sombreadores o las animaciones locos pueden causar esto también.
    * Vea las cosas en plantillas y kits personalizados.
    * Realice una copia de seguridad de su mundo a menudo, especialmente durante el desarrollo temprano. Use esas copias de seguridad para ajustarse a lo que ha agregado recientemente y que hace que las personas se bloqueen.

**Dejar "espacio"**
    * Recuerde que puede tener 20-30 personas en el mundo al mismo tiempo. ¿Qué ocurre si todas esas personas se huddled en torno a un Campfire. ¿Desea colocar 200 Pebbles por el fuego? Probablemente no sea una buena idea. Deje espacio para los avatares y Interactables (por ejemplo, los baloncesto).
    * Menos es más.

**Planeación previa** Piense en lo que desea crear y espaciar las cosas. Es fácil ponerse en marcha en Altspace.

**Usar la herramienta de diagnóstico en el principio y con frecuencia** Colóquelo y actualícela una vez. Finalmente, habrá herramientas similares en la VR que serán más accesibles.

**Cree amigos con usuarios de Oculus Quest** Invitarles a participar en su mundo para ayudarle a probar. Pruebe minuciosamente y con frecuencia. Pruebe todos los mundos de los demás. Nada supera las pruebas de lo real.

**Agregue amigos como "Admins" para su mundo** Edite su mundo y agregue sus amigos a la lista de administradores. Esto le permitirá ver la herramienta de diagnóstico de su mundo. No obstante, tenga cuidado porque también puede editar otros aspectos de su mundo. 

La **optimización del rendimiento es difícil, por lo que nuestra comunidad está ansioso por ayudarle** Únase al [AltspaceVR oficial](https://discordapp.com/invite/altspacevr) de compilaciones * visite el canal de creación de #world para obtener ayuda general con mundos.
    * Visite los canales del SDK de MRE para obtener ayuda específica con ayuda relacionada con el cargador de Unity más técnico y de Unity (plantillas y kits personalizados)