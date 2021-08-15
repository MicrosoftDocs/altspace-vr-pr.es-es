---
title: Mejora del rendimiento mundial
description: Obtenga información sobre cómo medir, solucionar problemas y mejorar el rendimiento de los mundos altspaceVR mediante herramientas de diagnóstico.
ms.date: 03/11/2021
ms.topic: article
keywords: rendimiento, solución de problemas
ms.openlocfilehash: 79d2bc43858c99652439aafa159c23f48eb3aa299c2b183936e40b1794fe444e
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126933"
---
# <a name="improving-world-performance"></a>Mejora del rendimiento mundial

Queremos que los usuarios tengan una buena experiencia, por lo que el rendimiento o el funcionamiento de su mundo en cascos de realidad virtual son enormemente importantes. Nuestro sistema World Building está diseñado para ofrecer un rendimiento excelente para los casos de uso más comunes. Si desea maximizar la presencia, esta guía es para usted. Altspace se utiliza para admitir todas las plataformas de hardware. Aunque animamos a World Builders a que presione los límites, en el caso de los mundos públicos, se recomienda dirigirse a Oculus Quest y a cualquier plataforma basada en PC como Windows Mixed Reality, Oculus Alsao s, o BIEN aLENT Vive. Para que sea sencillo, si el mundo se ejecuta bien en una misión, probablemente sea excelente para Altspace.

## <a name="tools-and-measurement"></a>Herramientas y medida

Diagnósticos de administrador es una herramienta sin conexión disponible en nuestro sitio web, altvr.com. Si navega a [Worlds > My Worlds](https://account.altvr.com/users/sign_in)(Mis mundos), busque su mundo y seleccione "Diagnostics", verá algo parecido a esto:

![Ventana de diagnóstico del administrador](images/performance.png)

Se trata de más directrices que requisitos. El rendimiento depende del número de objetos que tenga y de cómo se organizan. Por ejemplo, si tiene 500 objetos distribuidos en 2 kilómetros, el rendimiento probablemente será bueno. Sin embargo, si coloca los mismos 500 objetos en un área muy empaquetada, es probable que vea problemas. Esto se debe a que el rendimiento depende de lo que hay dentro del campo de vista de una persona. La mejor manera de probar es saltar a Altspace y teleportar por todo el mundo. Si observa algún problema o siente algún problema, esos son los puntos de problemas que querrá investigar.

Al apegarse a estas recomendaciones, se configura para el éxito. Vamos a retrasemos este diagnóstico de ejemplo tomado de un mundo destacado real: 

* **Objetos:** número total de objetos del mundo. Todo es un objeto: Artifacts, Fotos, puntos de generación, y así sucesivamente. Se recomienda mantener un número determinado, pero esto es flexible. Si se pasa por encima, se indica nuestra preocupación con un signo de exclamación amarillo, como se muestra aquí. Sin embargo, en este caso, hay dos áreas independientes en este mundo, por lo que la densidad no es alta.
* **Kits:** número total de kits únicos de creación mundial usados. Esto afecta al tiempo de descarga inicial al cargar el mundo. Los kits Artifacts, el menú de Objetos que puede generar en el mundo. 

> [!NOTE] 
> Si se usa un único artefacto de un kit, es necesario descargar los recursos del kit. Por lo tanto, es costoso usar solo algunas Artifacts de un solo kit. 

* **Kits: móvil:** tamaño total de todos los recursos del kit que una persona de una misión tiene que descargar antes de entrar en el mundo. Intente no hacer que los usuarios esperen 5 minutos para descargar todo lo que necesitan para su mundo.
* **Fotos:** número total de fotos usadas, que tienden a tener un mayor impacto en el rendimiento que Artifacts. Use con moderación.
Plantilla: móvil: si usa el uploader de Unity, mantenga el tamaño de descarga bajo.
* **Skybox-Mobile:** si usa Skyboxes personalizados, mantenga el tamaño de archivo pequeño para que los usuarios no obtengan "pantalla negra" (se quedas sin memoria de vídeo).
* **Missing/Invalid Kits/Artifacts:** referencias a kits problemáticos o Artifacts ... ¿Tiene una idea de una métrica? Háganoslo saber.
Una vez más, estos no son requisitos, por lo que se muestran iconos de estado verdes, amarillos y rojos. Incluso un mundo con una serie de indicadores rojos todavía puede ser destacado. Se prueba en Altspace, por lo que también debe hacerlo. [Si necesita ayuda, puede](getting-help.md)comunicarse con nosotros. 

## <a name="load-time"></a>Tiempo de carga

Cuando una persona comienza a viajar a su mundo (intenta entrar), primero cargará la plantilla. Descargarán los recursos de plantilla (archivos) para su plataforma y verán "Entorno de carga". A continuación, descargarán los recursos de Skybox y Kit. Por último, cargarán todos los objetos mientras ven "Cargando objetos". La descarga de todos los recursos puede tardar unos minutos en función de su ancho de banda de Internet: la carga de objetos es bastante rápida. Aunque los recursos se descargan desde servidores rápidos de todo el mundo, Altspace usa técnicas de almacenamiento en caché para evitar volver a descargar los mismos archivos repetidamente. Técnicamente, el tiempo de carga inicial no afecta al rendimiento de una persona después de entrar en el mundo, pero forma parte de la experiencia general, así que intente no hacer que las personas esperen demasiado tiempo al viajar a su mundo. Se recomienda pensar detenidamente en qué kits usar y ser imaginario haciendo más con menos.

## <a name="troubleshooting-and-tips"></a>Solución de problemas y sugerencias

**La gente ve una "pantalla negra"** Normalmente, esto se debe a que el dispositivo se quedó sin memoria de vídeo. Intente reducir el número de objetos en el área problemática del mundo y reducir el tamaño de cosas como skybox o plantilla o el número de Fotos. Esos tipos tienden a tener el mayor impacto en el uso de memoria de vídeo.

**Las personas se bloquean**
    * A veces, un kit o artefacto roto puede provocar esto.
    * Las animaciones o sombreadores de sombras también pueden provocar esto.
    * Esté atento a las cosas en plantillas y kits personalizados.
    * Haga una copia de seguridad de su mundo con frecuencia, especialmente durante el desarrollo temprano. Use esas copias de seguridad para tendrán en cuenta lo que ha agregado recientemente y que está causando que las personas se bloquean.

**Dejar "headroom"**
    * Recuerde que puede tener entre 20 y 30 personas en el mundo al mismo tiempo. ¿Qué ocurre si todas esas personas estuvieran amontonadas en torno a una fogueo? ¿Seguiría deseando colocar 200 hondos junto al incendio? Probablemente no sea una buena idea. Deje algo de espacio para avatares e interactuables (como los partidos de equipo).
    * Menos es más.

**Planear con antelación** Piense en lo que quiere crear y espacio en el espacio. Es fácil moverse por Altspace.

**Uso anticipado y** frecuente de la herramienta de diagnóstico A bookmark it and refresh it once in a while. (Marcarlo y actualizarlo de vez en cuando). Finalmente, habrá herramientas similares en vr que serán más accesibles.

**Hacer amigos con los usuarios de Oculus Quest** Invítelos a que entren en su mundo para ayudarle a probar. Pruebe exhaustivamente y a menudo. ¡Pruebe los mundos de los demás! Nada supera las pruebas en lo real.

**Agregar amigos como "administradores" para su mundo** Edite su mundo y agregue a sus amigos a la lista de administradores. Esto les permitirá ver la herramienta Diagnósticos para su mundo. Sin embargo, tenga cuidado, ya que también pueden editar otros aspectos de su mundo. 

**La optimización del rendimiento es difícil, por lo que nuestra comunidad está ansiosa por ayudar.** Únase a [la discordia oficial de AltspaceVR](https://discordapp.com/invite/altspacevr) *Visite el #world de creación de aplicaciones para obtener ayuda general con los mundos.
    * Visite los canales del SDK de MRE para obtener ayuda específica con ayuda más técnica y relacionada con el uploader de Unity (plantillas y kits personalizados).