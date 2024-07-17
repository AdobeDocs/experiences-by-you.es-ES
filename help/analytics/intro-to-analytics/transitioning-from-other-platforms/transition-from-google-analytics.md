---
title: Guía completa para la transición a  [!DNL Adobe Analytics] desde Google [!DNL Analytics]
description: Obtenga información acerca de la ubicación de funcionalidades equivalentes y cómo utilizarlas de manera eficiente al pasar de Google [!DNL Analytics] a [!DNL Adobe Analytics]
solution: Analytics
feature: Third-party Integration
role: User
level: Beginner
kt: 9830
thumbnail: 34749.jpg
exl-id: 646bdc8f-c95e-40be-b2f7-8e4ba5653d91
source-git-commit: 02e3a6dfa59df45113242bd8e874e18e9e1efd58
workflow-type: tm+mt
source-wordcount: '3323'
ht-degree: 0%

---

# Guía completa para la transición a [!DNL Adobe Analytics] desde Google [!DNL Analytics]{#comprehensive-guide-for-transitioning-to-adobe-analytics}

## 1. Introducción

Uno de los mayores desafíos en la transición entre cualquier herramienta es aprender dónde encontrar una funcionalidad equivalente y utilizarla de manera eficiente. Esta discusión forma parte de una guía más amplia para ayudar a los usuarios a realizar la transición a [!DNL Adobe Analytics] (como nuevo usuario o como proveniente de Google [!DNL Analytics]) con mayor facilidad. Se proporciona una comparación detallada con GA, como herramienta con la que es más probable que la mayoría de los usuarios estén familiarizados, para ayudarlos a correlacionar los conocimientos existentes con el nuevo conjunto de herramientas. Cuando no haya sustituto en la práctica, esto le ayuda a empezar y a reducir las frustraciones que puedan afectarle.

Deberíamos hacer una comparación terminológica rápida:

| **Descripción** | **[!DNL Adobe Analytics]** | **Google[!DNL Analytics]** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Se ha visto una métrica de evento que representa una página (o pantalla de una aplicación) | Vista de página | Vista de página |
| Una métrica que representa un grupo de interacciones en su sitio web o aplicación que se producen en el mismo lapso de tiempo | Visita | Session |
| Una métrica que define un dispositivo identificado (según varios criterios, incluidas las cookies y otros patrones de comportamiento, para unir información del usuario) | Visitante único | Usuario |

## 2. Las interfaces

Cuando la gente compara [!DNL Adobe Analytics] y Google [!DNL Analytics], comentan que la interfaz de [!DNL Adobe] es desalentadora al principio. Esto es cierto, pero también lo es; créanlo o no; una fortaleza, no una debilidad. [!DNL Adobe] proporciona una amplia gama de herramientas y flexibilidades en la visualización de datos, lo que le permite tener mucha más libertad para construir lo que necesita.

Empecemos por ver los informes &quot;en el sitio&quot;.

### 2.1. Creación de informes en el sitio

#### 2.1.1. Pantalla de inicio

Tanto [!DNL Adobe Analytics] como Google [!DNL Analytics] ofrecen una forma de personalizar la primera vista que ve un usuario cuando inicia sesión.

##### 2.1.1.1. Pantalla de inicio de Workspace/conjunto personalizado ([!DNL Adobe Analytics])

[!DNL Adobe Analytics] no presume de crear un informe generado previamente para que todos los usuarios lo vean al iniciar sesión. La página de inicio predeterminada lleva al usuario a la pantalla de aterrizaje de Workspace, que muestra a cada usuario todos los informes de espacio de trabajo que han creado o que se han compartido con él. Además, cada uno puede establecer cualquiera de estos informes como su pantalla de inicio si así lo desea.

![workspace-create-project](assets/ga-to-aa_1.png)

Más adelante, en esta guía, hay más detalles sobre el espacio de trabajo. Consulte la sección 2.1.2.1

>[!TIP]
>
>Cree o comparta algunos informes estándar para su organización de modo que tengan un punto de partida para ver la información sin tener que sumergirse en la creación de sus propios informes de inmediato.



##### 2.1.1.2. Perspectivas de la pantalla de inicio (Google [!DNL Analytics])

* La pantalla de inicio de Google [!DNL Analytics] tiene algunas visualizaciones generadas previamente para usted. Estas cubren cosas como:
* Usuarios, Sesiones, Tasa de salida hacia otro sitio y Duración de la sesión en los últimos siete días
* Usuarios por hora del día en los últimos 30 días
* Usuarios actuales en este momento y Páginas activas principales
* Canal de tráfico, Source/Medium y Referencias en los últimos siete días
* Sesiones por país en los últimos siete días
* Páginas principales de los últimos siete días
* Tendencia de usuarios activos de los últimos 30 días
* y más

Los usuarios de GA4 tienen más opciones para personalizar y añadir sus propios informes a la pantalla de inicio.

![google-analytics-interfaces](assets/ga-to-aa_2.png)

Probablemente, esto es lo que más se echa de menos en [!DNL Adobe Analytics]. No hay una pantalla de inicio prediseñada para usted. Sin embargo, puede configurar fácilmente un Workspace personalizado para replicar lo que necesita de la lista anterior y establecerlo como su pantalla de aterrizaje. Hay más información más adelante (o consulte la sección 2.1.2.1 [!DNL Adobe] de Workspace).

#### 2.1.2. Report Builder in situ

Además de los informes simples que proporcionan las herramientas de análisis, cada una de ellas también ofrece herramientas más potentes para crear sus propios informes personalizados.

##### 2.1.2.1. [!DNL Adobe Analytics] Workspace

Este es el centro de [!DNL Adobe Analytics], ya que se introdujo en 2017 y se ha convertido en el lugar de referencia para el análisis de [!DNL Analytics], y la razón principal por la que la sección Informes pronto dejará de funcionar.

Esta herramienta le permite crear informes con una libertad casi completa.

El informe se puede desglosar en paneles y estos pueden contener cualquier cantidad de visualizaciones. Los paneles se pueden configurar como información común, como filtros de intervalo de fechas y de segmento comunes.

Se puede cambiar el tamaño de los paneles y las visualizaciones que los rodean, así como arrastrarlos para mostrar los elementos juntos o apilados. Por lo tanto, si desea comparar dos grupos diferentes de datos uno al lado del otro, puede crear paneles que se dividan al 50/50 en el medio para mostrar los dos sitios en paralelo y facilitar la comparación.

Los usuarios tienen a su disposición una gran variedad de visualizaciones:

* Tabla de forma libre
* Tabla de cohortes
* Abandonos
* Flujo
* Gráficos
   * Área (apilada y sin apilar)
   * Línea
   * Dispersión
   * Barra (apilada y sin apilar)
   * Viñeta
   * Anillo
   * Histograma
   * Barras horizontales (apiladas y sin apilar)
* Mapa
* Bloques de resumen
   * Cambio de resumen
   * Texto de resumen
   * Texto (campo de texto libre para introducir información adicional que proporcione contexto)
* Venn

Cada panel y visualización puede tener título y se le puede aplicar una descripción para ayudar a contextualizar lo que muestra la información.
En [!DNL Adobe], los segmentos (sobre todo los filtros de datos) se aplican de forma retroactiva, y se pueden extraer en columnas de tablas de forma libre para comparar los datos en paralelo. Por ejemplo, si un usuario quisiera comparar dos categorías en el sitio para el tráfico, podría crear un segmento para la categoría A y otro para la B.

![analytics-page-views-report](assets/ga-to-aa_3.png)

Las tablas de forma libre permiten tener varias columnas y utilizar la segmentación, según sea necesario, para visualizar los datos como desee.

Si no desea ver un desglose por fecha, simplemente arrastre y suelte allí otra dimensión o segmento para ver los datos de una manera diferente. Por ejemplo, use segmentos para Tipo de dispositivo y, a continuación, agregue un desglose por sistema operativo para los usuarios de móviles o tabletas:

![analytics-compare-page-views-report](assets/ga-to-aa_4.png)

Workspace le permite dejar volar su creatividad, no se limita a desgloses &quot;estándar&quot;. Puede crear las visualizaciones que necesita para profundizar en las comparaciones que necesita ejecutar.

>[!TIP]
>
>No tenga miedo de jugar y explorar. Hay muchas maneras de pensar fuera de lo común. Además, compruebe que lo que ha creado demuestra lo que piensa. La experiencia ayuda.

Puede crear métricas calculadas sobre la marcha o segmentos que solo existan dentro del informe para evitar que se sature el repositorio de segmentos y cálculos. Esto le permite crear elementos centrados que son necesarios para informes específicos sin confundir a su organización con cosas que no se pueden utilizar en otros contextos.

Esta discusión es solo una introducción a esta herramienta, hay otras guías completas para comenzar. Una vez que revise estas guías, realice informes completos como los siguientes:

![workspace-dashboard](assets/ga-to-aa_5.png)

Los espacios de trabajo no se guardan automáticamente, por lo que es más fácil hacer un único informe ad hoc sin saturar el repositorio de informes.

Otra funcionalidad potente de los espacios de trabajo es la capacidad de aplicar modificadores interactivos a los informes en forma de desplegables. Estos desplegables no funcionan en archivos CSV o de PDF exportados de los informes. Sin embargo, en el informe en directo, le permiten actualizar todas las visualizaciones de un panel para mostrar el mismo informe en condiciones diferentes. Se pueden utilizar varios desplegables y, siempre que las opciones no sean mutuamente excluyentes, los elementos seleccionados se apilarán para permitir presentar de forma limpia la información.

>[!IMPORTANT]
>
>Para obtener más información acerca del uso de desplegables y desgloses de forma libre, consulte <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google [!DNL Analytics]: paneles e informes personalizados y guardados

Google tiene algunas herramientas para crear informes dentro de la interfaz, pero siguen teniendo la misma visualización y las mismas limitaciones de la sección de informes.

Ahora, aquellos versados en Google [!DNL Analytics] que lean esto, podrían estar diciendo: &quot;Bueno, espere un segundo, ¿qué pasa con Google Data Studio? ¿No es un mejor equivalente al Workspace de [!DNL Adobe]?&quot; Sí, pero técnicamente Data Studio no forma parte de la herramienta [!DNL Analytics] y permite conexiones a diferentes fuentes de datos. Esta herramienta se trata más adelante, específicamente en la sección 2.2.3, Acceso ampliado a informes.

Los paneles y los informes personalizados de Google le permiten agrupar varias visualizaciones en un informe, pero, a diferencia de Workspace, aún están bloqueados en correlaciones sencillas y en qué datos se pueden colocar en qué columnas.

En los informes personalizados, uno de los mayores desafíos es, cuando crea un filtro, que se aplique a todas las pestañas del informe. No existe una forma de comparar dos filtros diferentes dentro del mismo informe.

Para las comparaciones superficiales, cumple su función. Todos son similares a los [!DNL Adobe] paneles, informes personalizados y marcadores heredados. Herramientas básicas proporcionadas para satisfacer sus necesidades y que residen en el grupo de informes.

#### 2.1.3. Informes

Tanto Google como [!DNL Adobe] tienen algunos informes navegables que son tablas creadas previamente y gráficos básicos de cronología basados en una dimensión.

##### 2.1.3.1. [!DNL Adobe Analytics] informes

[!DNL Adobe Analytics] también tiene una sección Informes, aunque se está eliminando gradualmente en favor de Analysis Workspace. De hecho, se ha anunciado el fin de la vida útil de esta interfaz, ya que Workspace es una herramienta más potente. La mayoría de estas tablas se pueden crear y modificar con mayor facilidad. Las secciones de [!DNL Adobe] están mucho más divididas, y esto puede ser desalentador:

![analytics-site-metrics](assets/ga-to-aa_6.png)

Como la mayoría de lo anterior es accesible a través de los espacios de trabajo, hago una breve descripción de estas secciones y cómo se relacionan con Google [!DNL Analytics], y resalto los informes que siguen siendo relevantes.

Las métricas del sitio son lo que cabría esperar: abarcan las métricas estándar (vistas de página, visitantes únicos, visitas y eventos personalizados que haya configurado). Esto es similar al informe de comportamiento de GA, pero también incluye algo de lo que encontraría en la audiencia (ya que [!DNL Adobe] no divide los tipos de métricas).

Aquí, encontrará los informes de &quot;bots&quot;. El tráfico de bots se excluye de todos los informes estándar. Sin embargo, hay dos que ofrecen una perspectiva de lo que está sucediendo y de los bots que llegan al sitio. Esto es especialmente bueno si configura reglas de bots personalizadas para excluir los bots de spam conocidos que visitan con frecuencia el sitio. Puede obtener información sobre lo que están haciendo esos bots sin que los informes principales se inunden de ese tráfico. Actualmente, los informes de bots no están disponibles a través de Workspace (pero las nuevas funciones de creación de informes que se lanzarán próximamente también permitirán a los usuarios obtener esta información).

Contenido del sitio es una agrupación de [!DNL Adobe] dimensiones estándar: Nombre de página, Secciones de sitio, Jerarquías, Servidores y más. Todas estas dimensiones están disponibles en Workspace.

Móvil es una agrupación de datos específicos de dispositivos móviles, incluidos dispositivos, tipos de dispositivos y mucho más. Están disponibles en Workspace.

Las rutas no están disponibles en Workspace. Workspace tiene un diagrama de flujo en el que puede ver los flujos de entrada y salida de una sola página o valor. Por el contrario, las rutas permiten ver las rutas más comunes utilizadas en el sitio web. De forma predeterminada, Páginas es el primer informe de ruta configurado para usted. Sin embargo, puede activarlo para props personalizados como un valor de Tipo de página. Puede observar las rutas dentro de los tipos de página. La otra cosa que personalmente me gusta de las Rutas es la forma sencilla en que se presenta la información... El diagrama de flujo en el espacio de trabajo (dependiendo de cuánto esté intentando ver) puede ser abrumador. Recomiendo probar ambos... cada uno tiene un uso y valor dependiendo de lo que esté tratando de lograr. Debe tenerse en cuenta que cualquier dimensión se puede utilizar en Flujos, mientras que las Rutas deben configurarse en una propiedad en el panel Administración.

Los informes Fuentes de tráfico, [!DNL Campaign] y Canales de marketing son todos similares al informe Adquisición del producto de Google. Fuentes de tráfico se centra en los remitentes del reenvío reales, [!DNL Campaign] en los códigos [!DNL Campaign] y los canales de marketing, también en los códigos [!DNL Campaign], pero además aplica una lógica adicional (según determine el usuario) sobre cómo procesar la información. [!DNL Adobe] proporciona más libertad sobre cómo configurar las reglas. Por el contrario, Google hace muchas cosas por usted, lo que supone un cambio en la forma de pensar. De manera predeterminada, la atribución de Google para [!DNL Campaign] códigos es de seis meses. La atribución de [!DNL Adobe] se establece en una semana de forma predeterminada. Esto se puede cambiar en la configuración de administración, pero en Workspace puede aplicar una atribución personalizada sobre cualquier dimensión, lo que le ofrece una mayor flexibilidad sobre la marcha.

Los informes Retención de visitantes y Perfil del visitante son similares a los informes Audiencia de Google [!DNL Analytics]. Retención de visitantes se centra más en la frecuencia de retorno, mientras que Perfil del visitante, en la geografía y la tecnología de los usuarios.

Los informes Conversión personalizada y Tráfico personalizado son informes de dimensión personalizados. Las conversiones son eVars. Puede establecer una caducidad personalizada en el valor, como visita individual, visita, mes y año. Este valor permanece en la persistencia de un usuario durante el lapso de tiempo configurado, a menos que se sobrescriba. Las variables de tráfico son props. También puede configurarlas para informes de rutas o como elementos de lista que separan varios valores según un delimitador de su elección.

Medios es para elementos como vídeos o archivos de audio en los que ha configurado un seguimiento de medios especial.

Informes personalizados es una sección en la que un usuario puede personalizar las columnas y desgloses que ha creado en la interfaz de informes y guardarlos como un informe personalizado. Sin embargo, como se ha mencionado anteriormente, dado que Workspace permite desgloses y correlaciones mucho más potentes, cualquier personalización debería realizarse allí. Esta era una buena solución antes de que existiera Workspace.

La sección Marcadores es similar a los Informes personalizados, donde los informes usados con frecuencia se pueden añadir como marcador en la interfaz de informes para que se puedan encontrar más fácilmente.

El tablero era un producto heredado que permitía a las personas combinar informes breves de datos en una sola visualización. Sin embargo, la funcionalidad de Workspace (sección 2.1.2.1) es mucho más fácil de usar, ya que solo existe como punto de acceso a los informes heredados que deben reconstruirse antes de que esta función se cierre.

Los objetivos permiten a las personas crear un informe basado en un objetivo dentro de un periodo de tiempo determinado. Los equipos supervisan las campañas para ver si están en el camino correcto para alcanzar sus objetivos de tráfico.

Todos los informes aquí permiten varias columnas de métricas y desgloses de dimensiones. Sin embargo, la simplicidad de las visualizaciones y parte de la lógica detrás de qué elementos podrían correlacionarse pueden ser frustrantes a veces.

##### 2.1.3.2. Informes [!DNL Analytics] de Google

Google [!DNL Analytics] divide estos informes en las siguientes secciones: Tiempo real, Audiencia, Adquisición, Comportamiento y Conversaciones (en GA3) y en Ciclo vital (con las subsecciones Adquisición, Participación, Monetización y Retención) y Usuario (con las subsecciones Demografía y Tecnología).

![google-analytics-interface-compare](assets/ga-to-aa_7.png)

Puede realizar algunos ajustes menores en estas visualizaciones, agregar un desglose de dimensión secundario, cambiar la visualización, crear un filtro en los datos y más. Puede guardar las personalizaciones como un informe guardado.

Proporcionan una visión rápida y sencilla de sus datos. Sin embargo, no puede comparar cosas como usuarios con vistas de página para una página de la misma tabla y no puede agregar más de una dimensión adicional para ver datos adicionales.

Son buenos para obtener datos analíticos rápidos, pero si realmente necesita profundizar, sufren de limitaciones.

### 2.2. Acceso ampliado a los informes

Además de la Creación de informes en el sitio, la mayoría de las herramientas ofrecen una funcionalidad ampliada que le permite sacar el análisis de las herramientas y crear algo un poco más personalizado.

#### 2.2.1. Report Builder [!DNL Adobe Analytics] (extensión de Microsoft® Excel)

Workspace es una buena herramienta, pero a veces es necesario poner los datos en una hoja de cálculo personalizada, posiblemente para poder unir varias fuentes de datos. Aquí es donde Report Builder entra en juego.

Report Builder es un complemento para Microsoft® Excel que le permite crear conexiones con los datos de [!DNL Adobe Analytics] para extraer datos de tablas que puede manipular en Excel. Por lo general, para utilizarlo de forma eficaz, extraiga los datos en algunas pestañas de datos sin procesar, luego utilice referencias de celdas de Excel para extraer datos de estas pestañas en un único informe consolidado y, a continuación, cree gráficos y visualizaciones.

>[!NOTE]
>
>El Report Builder tiene un permiso especial que debe aplicarse a los usuarios para acceder a este complemento. Debería concederse a los usuarios que hayan aprendido a utilizar bien la herramienta.

#### 2.2.2. Conexión de la API [!DNL Adobe Analytics]

Si necesita que los datos de [!DNL Adobe Analytics] se digieran con algo distinto a Excel y quiere los datos procesados, incluidas las exclusiones de reglas de bots, use la API de [!DNL Adobe] para extraer los datos directamente. A continuación, procese los datos mediante una secuencia de comandos o agréguelos a una base de datos para su uso con otro sistema.

Debe tenerse en cuenta que la API sigue extrayendo datos de correlación aplicando los desgloses y segmentos según se especifican en la solicitud de extracción.

El Workspace de [!DNL Adobe] (sección 2.1.2.1) utiliza la API para generar los informes y, si activa el modo de depuración en Workspace, le mostrará las llamadas de API exactas que se han usado. Esta es una forma rápida de crear sus llamadas a la API. Al utilizar Workspace para generar y validar los datos que desea extraer, utilizará esas llamadas de API para sacar los datos a su propio procesamiento.


#### 2.2.3. Google [!DNL Analytics] Data Studio

Si ha estado leyendo, ya sabe que he mencionado Data Studio como el equivalente al Workspace de [!DNL Adobe]. Data Studio le permite extraer datos de Google [!DNL Analytics], pero también de otras fuentes. Es interesante si desea consolidar los datos de análisis con otros datos recopilados. Sin embargo, con Google [!DNL Analytics], existen el mismo tipo de limitaciones de visualización. El modo en que se forman las filas y columnas sigue siendo limitado.

Sigue siendo una herramienta poderosa, y no disuadiría a la gente de usarla de ninguna manera. Mi experiencia personal es que el comportamiento rígido me parece bastante restrictivo.


#### 2.2.4. Extensión de hoja de cálculo de Google

Para mis propios usos, cuando necesito extraer datos de forma extendida de Google [!DNL Analytics], la herramienta de mi elección es la extensión de hoja de cálculo de Google. Aunque necesito hacer múltiples conexiones a mis tablas de GA, puedo hacer referencia a las celdas desde los datos sin procesar y elaborar los informes que necesito. A continuación, los visualizo utilizando las funciones gráficas de la hoja de cálculo de Google.


## 3. Exportaciones de datos sin procesar

Cuando realmente necesita datos sin procesar, tanto [!DNL Adobe] como Google ofrecen funcionalidades para extraer información de esta manera.

### 3.1. Fuente de datos [!DNL Adobe]

En la sección 2.2.2, mencioné que la API [!DNL Adobe Analytics] extraía &quot;datos procesados&quot;. La fuente de datos sin procesar extrae datos procesados por las &quot;reglas de procesamiento&quot; que se han configurado en el panel de administración, pero estos datos sin procesar incluyen todos los datos que se excluyen en cualquier otra parte.

Esto significa que todas las exclusiones de bots, los datos filtrados de IP internos, etc., se incluirán en las fuentes de datos sin procesar. Existen indicadores para identificar estos datos, de modo que si crea un lago de datos, el equipo de ingeniería puede crear lógicas para procesar estos datos en consecuencia.

Las fuentes de datos sin procesar se pueden personalizar para enviar todas las columnas de datos o solo columnas específicas si necesita una fuente más enfocada.

Las fuentes se pueden enviar directamente a FTP, SFTP o S3.


### 3.2. Google Big Query

Desafortunadamente, esta es una herramienta de Google con la que no he tenido ninguna experiencia. En teoría, debería ser similar a la Fuente de datos de [!DNL Adobe], lo que permite a su equipo de ingeniería acceder a los datos sin procesar de su cuenta de Google [!DNL Analytics].

Sin embargo, en lugar de proporcionar un volcado de datos sin procesar completo, permite a los ingenieros acceder a los datos a través de consultas SQL para extraer datos sin procesar concretos o todas las columnas.

## 4. Conclusión

Como cualquier sistema, se necesita práctica para sentirse cómodo con la herramienta. Esperamos que esta guía le ayude a empezar o le proporcione sugerencias para mejorar el uso de [!DNL Adobe Analytics].

Sin embargo, subrayaré que recomendaría utilizar tanto [!DNL Adobe Analytics] como Google [!DNL Analytics] en su estrategia de implementación (incluso si Google [!DNL Analytics] es solo la versión gratuita). Esto le permite tener un sistema de copia de seguridad para asegurarse de que tiene datos, ya que ningún sistema es infalible.

Hay muchos recursos disponibles más allá de esta guía que pueden ayudar a mejorar su estrategia:

* [[!DNL Adobe] Experience League](https://experienceleague.adobe.com/?lang=es#home): contiene tutoriales, vídeos, documentación y foros de la comunidad
* [[!DNL Adobe] Grupos de usuarios](https://analytics-augs.adobe.com/): un centro de eventos de la comunidad para ayudar a los usuarios a conectar entre sí y mejorar sus implementaciones.
* [[!DNL Adobe Analytics] Canal de YouTube de grupos de usuarios](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - ¿No pudo asistir a una sesión de grupo de usuarios de [!DNL Adobe Analytics]? Vuelva a ver las sesiones de grupos de usuarios anteriores en todo el mundo para obtener más información acerca de cómo utilizan la herramienta sus colegas.
* [Canal de Slack de chat de Measure](https://www.measure.chat/): conéctese con usuarios de [!DNL Adobe Analytics] de todo el mundo y comparta las lecciones aprendidas en la industria, haga preguntas de sus colegas y únase a grupos de interés centrados en la medición.
* ¡y más!

## Autor

Este documento fue escrito por:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, jefa de optimización [!DNL Analytics] en Torstar

[!DNL Adobe Analytics] campeón
