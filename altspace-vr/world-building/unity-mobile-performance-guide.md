---
title: Guía de rendimiento de AltspaceVR Mobile
description: Aprenda a usar varias propiedades de Unity para que sus mundos se realicen en dispositivos móviles, como Oculus Quest.
ms.date: 04/20/2021
ms.topic: article
keywords: editor world, performance, oculus, vr, unity, textures, lightmaps, stats, profiler, draw calls, altspacevr, uploader
ms.openlocfilehash: 9d6afba6fff85adfaa2ba290916f25c84c5377cd
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "112961258"
---
# <a name="altspacevr-mobile-performance-guide"></a>Guía de rendimiento de AltspaceVR Mobile

## <a name="main-points"></a>**Puntos principales:**

* **72 FPS** en Oculus Quest 1 y 2, es el destino.
* **La reducción de las llamadas a draw** a través del procesamiento por lotes estático es esencial, con el objetivo de menos de **25 drawcalls**
* **Un material por objeto para** fomentar el procesamiento por lotes estático (dividir objetos de varios materiales en objetos independientes).
* **Los** objetos de un entorno deben establecerse en **"Static"** en la mayoría de los casos.
* **Un mapa de** luz por escena, un 2 000 o 4 k para toda la escena, ~25 elementos de textura por unidad, el escalado de mapa de luz debe ajustarse por objeto (gráfico de escalado a continuación)
* **Use** sombreadores de calidad móvil (es decir, "Móvil/Difuso", etc.), evite el sombreador estándar de Unity/PBR/Sondeos de reflexión/sondeos de luz, ya que son operaciones pesadas y, en el caso de los sondeos, agregarán llamadas a draw.
* **Menos de 100 000 triángulos** en pantalla
* **La** selección de oclusión puede ayudar a reducir los polígonos en pantalla, aunque hay un costo inicial por tener habilitada la selección de oclusión, así que mida el efecto en la velocidad de fotogramas en Altspace mediante el Panel de diagnósticos.
* Para todas **las texturas** de una escena, use "Invalidar para **Android"** y estaflícelas en formato de bloque **ASTC 6x6 comprimido RGB(A).**  Deje la compresión configuración de compilación de Android en el valor predeterminado (que se encuentra en: File/Build Settings/Android/Texture Compression: 'Don't override'), para que Lightmaps no obtenga compresión ASTC.  Al hacer lo anterior y compartir materiales entre objetos, intentamos mantener el paquete unity de nuestra escena en unos **10-20 MB para Android.**

El objetivo general es alcanzar una velocidad de fotogramas aceptable en todos los dispositivos: en Oculus Quest 1 y 2 idealmente, la escena se ejecutará a 72 FPS desde todos los puntos de escena cuando se rellene la escena, aunque un intervalo de 60-72 FPS suele ser un objetivo más realista.

La velocidad de fotogramas se puede medir en AltspaceVR en cualquier dispositivo que use (se encuentra en la aplicación AltspaceVR en **Configuración/Soporte técnico/Mostrar panel de diagnóstico/FPS).**

Un resumen de las herramientas estándar de Unity disponibles para ayudarle a optimizar mejor sus escenas:

## <a name="stats-panelframe-debuggerprofiler"></a>**Panel estadísticas/Depurador de fotogramas/Profiler**

* Estas herramientas serán sus mejores amigos para mejorar el rendimiento de la escena.  Solo se puede hacer referencia a ellos mientras la escena está reproduciendo en el **editor,** ya que sus valores serán diferentes de cuando la escena no se esté reproduciendo (es decir, el procesamiento por lotes estático automático no se realizará cuando la escena no se esté reproduciendo).

* **El Panel de** estadísticas (que se puede ver en la vista de juegos en "Estadísticas") mostrará la cantidad de lotes/lotes guardados, **llamadas SetPass y velocidad de fotogramas.**

    * Lotes: la cantidad de llamadas a draw actuales que son visibles desde la perspectiva de la cámara actual.  **Menos de 25 lotes** para un entorno es un buen objetivo.
    * Lotes guardados (solo visibles cuando la escena está reproduciendo): la cantidad de llamadas a draw que se han reducido a través del procesamiento por lotes estático o la creación de **instancias de GPU**
    * Llamadas SetPass: el número de materiales visibles diferentes en una escena
    * Velocidad de fotogramas: la cantidad de fotogramas por segundo en la vista Juego (le ofrece una idea aproximada de lo que sucede; las escenas siempre se deben probar en la aplicación, en el casco, mediante el panel Velocidad de fotogramas de Oculus, ya que la lectura de fps siempre será diferente de lo que está en el editor).

* **Depurador de fotogramas** (se encuentra en Ventana/Análisis/Depurador de fotogramas).  El Panel de estadísticas de la marca que, cuando está habilitado, le permitirá ver lo que la GPU dibuja para crear la imagen final, que muestra una lista de llamadas draw de primero a último.  Le dará motivos para que una llamada a draw no se procesara por lotes con una llamada a draw anterior (es decir, "Este objeto usa un material diferente" o "Este objeto usa un mapa de luz diferente"), y es una excelente manera de desarrollar un conocimiento de lo que sucede en la escena y de cómo y por qué determinadas opciones visuales pueden ser costosas computacionalmente.

* **Profiler** le mostrará qué partes del equipo se usan en cualquier momento mientras se ejecuta el juego. Resulta útil para determinar dónde se está cuellos de botella en el rendimiento.  Por ejemplo, si ve un uso intensivo de CPU en la escena, podría ser que hay demasiadas llamadas a draw o, si ve un uso intensivo de GPU, puede que se produzca un exceso de dibujo (es decir, el número de veces que se representa un solo píxel para generar la imagen final), lo que puede deberse a que hay varias superficies transparentes. , u objetos que no se están haciendo la selección cuando están fuera de la vista.

## <a name="draw-calls-shadersmaterialsobjects"></a>**Llamadas a Draw (sombreadores,materiales/objetos)**

* Cada vez que es necesario representar un sombreador, material u objeto, la CPU tiene que indicar a la GPU del modificador (también conocido como "llamadas a draw", de forma coloquial **"drawcalls").**  Es decir, si tiene 5 sombreadores, 10 materiales y 20 objetos, con lo que sea mayor. tendrá aproximadamente 20 drawcalls.  Otras cosas que pueden multiplicar las llamadas a draw incluyen tener objetos en mapas de luz diferentes o tener más de una luz en tiempo real en una escena (es decir, una luz de punto agregará otra llamada drawcall a cada objeto que esté dentro de su intervalo), por lo que generalmente se debe evitar cualquier cosa que no sea la luz direccional de una escena.  Los sondeos de reflexión y los sondeos claros también multiplicarán las llamadas a draw en los objetos que se toban, por lo que deben evitarse.

*  El procesamiento por lotes estático procesará por lotes los objetos que comparten materiales similares en un solo objeto cuando se envían a la GPU (con oclusión Culling descartando mallas que están fuera de la vista), por lo que al establecer todos los objetos del ejemplo anterior en "Static", reduciría la escena a aproximadamente 10 drawcalls, 1 para cada material. 

* **Los lotes de** materiales se producen cuando un objeto tiene los materiales exactos como otro objeto; sin embargo, si un objeto tiene varios materiales, no se procesará por lotes con un objeto que tenga menos materiales.  Por esta razón: los objetos SOLO DEBEN tener **1 material** y los objetos que usan varios materiales deben dividirse en objetos independientes por material.  **Los lotes de** material se pueden reducir a través de la atlasación de **texturas** (combinando las texturas de varios objetos únicos para compartir una sola hoja de textura para que todos usen el mismo material).  Intente mantener la cantidad de Atlases en una sola textura o material de 2 k o 4 k por escena, si es posible.

## <a name="scene-complexity"></a>**Complejidad de la escena**

* **Geometría:** intente mantener triángulos en pantalla para entornos por debajo de 100 000.  Use la pestaña "Estadísticas" en el panel Juego de Unity para ver los recuentos de triángulos que está alcanzando desde varios puntos de escena de la escena.  Las propiedades como tales deben estar en el intervalo de "cientos" de triángulos, con solo propiedades importantes "hero" en el intervalo de miles de triángulos. 

* Técnicamente, puede usar los LOD (nivel de **mallas** de detalle), aunque la solución lightmap predeterminada de Unity no comparte datos de mapa de luz entre los LOD, por lo que puede obtener artefactos de iluminación cuando los LOD cambien a esta resolución.  Como alternativa, puede usar el componente Grupo de LOD para la selección de distancia simple, incluso si el objeto no tiene mallas loD inferiores:

![Ventana Grupo de LOD en Unity](images/world-building-lod-Group.png)

* **La** selección de oclusión reduce el número de objetos que se representan solo a lo que se encuentra dentro de la frustum de la vista de la cámara y que están inmediatamente visibles (es decir, los objetos que se ocultan desde la vista se Culled).  La selección de oclusión casi siempre debe estar lista para la escena y los niveles deben diseñarse para admitirla (es decir, si tiene un nivel grande, se pueden usar paredes u objetos grandes para dividir la línea de visión del jugador, de modo que no siempre puedan ver hasta el extremo opuesto del nivel.  La configuración predeterminada de la "bake" debería funcionar, aunque es posible que tenga que reducir los valores "Occluder más pequeño" o "Más pequeño".  En el caso de objetos como barreras en las que es posible que pueda ver a través de fisuras en el objeto u objetos transparentes, debe desactivar el estado "Occluder" del objeto en el menú desplegable "Estático" para que los objetos subyacentes no se oscile erróneamente. 

## <a name="lightmaps"></a>**Mapas claros**

* Idealmente, **solo un mapa de luz por escena** (2 000 o 4 k para todo), si no es así; Menos mapas de luz de resoluciones más altas son mejores que muchos mapas de luz de resoluciones más bajas.
* Tener varios mapas claros también puede afectar al número de llamadas a draw, ya que los objetos que tienen o no tienen mapas claros estarán en lotes diferentes y otros mapas claros también estarán en lotes diferentes.
* Por lo general, una resolución de mapa de luz de aproximadamente **25 elementos de** textura por unidad debe ser suficiente (establezca la resolución en la configuración de iluminación/escena).  Si tiene espacio adicional en el mapa de luz, puede aumentar este valor.
* Cambie el **valor de Escala de Mapa** de luz por objeto para que la resolución se guarde para los objetos que lo necesiten. 

* **Gráfico de escalado de mapa de luz** (regla general) 
    * **Primer plano** (geoárrelo de nivel de recorrido): 1 
    * **Propiedades** (especialmente propiedades más pequeñas que un humano): **2-3** (para evitar artefactos de mapa de luz y juntas en los objetos) 
    * **Midground** (geometría que está justo fuera del área transitable o objetos grandes como edificios): **0,5**
    * **Fondo** (objetos vista/lejanos): **0,02** 
    * **Superficies transparentes** (como el cristal): **0** (con "Sombras de conversión/recepción" deshabilitado) 

Además, como línea de base, estas son algunas opciones de configuración que se usaron para el entorno de Efecto de la puerta de pantalla:

![Ventana de iluminación en Unity](images/world-building-lightmaps.png)

## <a name="texture-compressionfile-size"></a>**Compresión de textura/tamaño de archivo**

* Para nuestra compilación de Android, intentamos mantener el tamaño de la escena del paquete de Unity en torno a 10-20 MB en total.  Para ello, compartimos materiales genéricos entre muchos objetos, usamos el color de vértice para tint los objetos y también establecemos invalidaciones manuales para Android para que las texturas usen la compresión de bloques **ASTC 6x6,** que será menor que la compresión predeterminada.

* La razón por la que no establecemos la configuración de compilación de Android para usar ASTC es porque los mapas claros no se ven bien con esa compresión (muchos artefactos bloqueados) y tendríamos que establecer el mapa de luz para que use ETC después de cada bake, por lo que es más fácil configurar la invalidación para todas las texturas de escena una vez que actualizar la configuración de compresión del mapa de luz después de cada bake.

![Ventana Textura en Unity](images/world-building-texutres.png)

* Además, establecer Texturas para usar el modo de filtro trilineal con un nivel anisotropico de 2 puede ayudarles a mantenerse nítidos en los ángulos de visión.

Puede encontrar más sugerencias y trucos de rendimiento en la documentación de mejora [del rendimiento mundial](improving-performance.md).