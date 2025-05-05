---
title: Creación de una cultura de datos y una mejor referencia de diseño de la solución
description: Revolucione su estrategia de datos y permita a su equipo crear un documento sólido de referencia de diseño de la solución (DRS). Elimine las brechas de medición y fomente una cultura de datos colaborativa a través de metodologías paso a paso.
feature: Implementation Basics
topic: Administration
role: User
level: Experienced
doc-type: Article
duration: 72000
last-substantial-update: 2024-04-25T00:00:00Z
jira: KT-15338
thumbnail: KT-15338.jpeg
exl-id: 99fcf68f-5698-4270-9055-ab224e6323a1
source-git-commit: b2e05ff39e065691dda530ed17762a55cf2e6778
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# Creación de una cultura de datos y una mejor referencia de diseño de soluciones

_Revolucione su estrategia de datos y capacite a su equipo para crear un documento sólido de referencia de diseño de soluciones (SDR). Elimine las brechas de medición y fomente una cultura de datos de colaboración mediante metodologías paso a paso._

Por fin es el momento. Usted armó un SDR sólido. Un SDR es la guía que se utiliza para implementar las métricas y dimensiones. Has definido cómo se llaman, cuándo se activan, y a tus desarrolladores les encanta. Pasaste por todo el proceso de implementación, escribiste criterios de aceptación, pasaste por tus sprints, lo probaste, ¡y está hecho! Su instancia de [!DNL Adobe Analytics] debería estar recibiendo a los equipos de mercadotecnia y productos celebrando mientras se adentran en los datos, obtienen nuevas revelaciones acerca de sus clientes y encuentran todas las áreas de éxito y, bueno, las de menor éxito. Pero no estás escuchando los elogios que esperabas.

Desde un equipo, se escuchan quejas como:

&quot;¿Por qué no puedo averiguar la tasa de conversión en este canal?&quot;

&quot;¿Por qué no hay una métrica para esto?&quot;

&quot;¡Necesito más detalles! Una métrica por sí sola no es suficiente. Hay al menos tres dimensiones diferentes que necesito para entender el rendimiento. ¿Por qué no los pusiste?&quot;

Pero es el otro equipo el que es un motivo de preocupación aún mayor. De ellos, no se oye nada en absoluto. Peor aún, se ven gráficos que claramente fueron tomados de su antigua solución de análisis (la que ya no se mantiene, y cada día está cayendo más en un pantano de decrepitud y datos sucios). Una sensación de temor te llena mientras consideras las decisiones que se podrían tomar con ese desorden original.

_¿Qué ha fallado?_

_¿Por qué hay huecos en la medición?_

_¿Por qué los integrantes del equipo no aceptan esto?_

Empezaré por dejarte salir un poco del anzuelo. _siempre_ va a haber alguna revisión. Si su sitio o aplicación es lo suficientemente complejo como para necesitar una solución de análisis empresarial, se garantiza que se perderá algo. Pero en este caso, no se perdió lo suficiente como para explicar los huecos de medición que estoy describiendo.

Lo que salió mal es mucho más difícil de poner en una hoja de cálculo. Básicamente, se perdió su primera oportunidad de crear una cultura de datos colaborativa mientras creaba su SDR.

Quiero guiarle a través de un método que mis colegas y yo desarrollamos tanto para construir un mejor SDR con menos brechas, como para hacer que los usuarios finales inviertan (e incluso, ocasionalmente, se entusiasmen) con su nueva instancia de [!DNL Adobe Analytics]. Veamos cómo y por qué debe considerar este método.

## El cómo

_Obtenga información acerca de la conferencia de medición. Utilice un mapa de embudo para visualizar cada paso del plan. Cree paneles ficticios para revisarlos como grupo. Crear un diccionario de datos para los usuarios._

### La conferencia de medición

1. Reúne a las partes interesadas, ya sea en persona o virtualmente, con el objetivo de averiguar qué medir. Esta reunión debería incluir a algunos ejecutivos.
1. Tenga ejemplos obvios ya en el tablero en las notas adhesivas, como ingresos, ventas o posibles clientes, se medirán los indicadores clave de producto (KPI) principales que sepa. Repita este proceso con dimensiones como el estado de inicio de sesión, las categorías de productos o los términos de búsqueda.
1. Haga que todos agreguen sus propias notas adhesivas, agrupándolas según sea necesario.
1. Pídele a la gente que vote por aquellos que ellos piensan que son importantes. Son votos ilimitados porque todas estas métricas y dimensiones probablemente importen.
1. Para cualquier métrica y dimensión que tenga votos bajos, pida a las partes interesadas que lo solicitaron que expliquen por qué se utilizarían estos componentes. Si hay un buen caso de uso, conserve estos componentes. Si hay una mejor manera de obtener esos datos, o nadie puede explicar cómo se pueden llevar a cabo acciones con esos datos, o si hay otra buena razón para eliminar las métricas y dimensiones, hágalo.
1. Añada estas métricas y dimensiones a la SDR para una revisión inicial por parte de las partes interesadas presentes.

### El mapa del canal

1. Obtenga una visualización de todos los canales, paso a paso con cada estado incluido.
1. Con los diseñadores y los gestores de producto, revise cada paso y hable de lo que todo el mundo considera éxito en ese canal. ¿Es la tasa de conversión? ¿Está eligiendo una ruta en particular? ¿Está usando ciertas características?
1. Haga preguntas sobre qué métricas y dimensiones son necesarias para comprender el rendimiento del canal en cada paso del canal y en general.
1. Por encima de cada paso del canal, añada las métricas y dimensiones que se miden en ese paso, incluidas las métricas calculadas.
1. Al principio de cada canal, escriba los informes que van en el panel que el gestor de producto puede utilizar para rastrear el rendimiento. Estos informes incluyen [informe de visitas en el orden previsto](https://experienceleague.adobe.com/es/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow), [mes actual](https://experienceleague.adobe.com/es/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges), [tasas de conversión de tendencias](https://experienceleague.adobe.com/es/docs/analytics/analyze/analysis-workspace/visualizations/line) y cualquier dato más específico de ese canal.
1. Añada las nuevas métricas y dimensiones que haya descubierto a la SDR y envíelas a las partes interesadas para una segunda revisión.

### Los paneles de previsualización

1. Con el mapa del canal como guía, cree paneles de prueba.
1. Debe haber una vista general, como [Tablero de resumen ejecutivo](driving-success-with-executive-summary-dashboards.md), y tableros para cada uno de los embudos.
1. También habrá algunas más específicas para su sitio o aplicación, como el rendimiento del producto o el rendimiento del contenido.
1. Distribuya estos elementos a las partes interesadas relevantes y obtenga comentarios sobre el diseño.
1. Realice las actualizaciones solicitadas y, si se necesitan nuevas métricas o dimensiones, agréguelas a la SDR.
1. Envíe los paneles de vista previa actualizados y la SDR para una revisión final.

### Herramientas de democratización de datos

1. Cree un diccionario de datos. La SDR es para los desarrolladores, pero el diccionario de datos es para los usuarios finales. Hágalo legible para que todos puedan buscar fácilmente qué datos están disponibles y saber cómo utilizarlos. Los usuarios finales deben ser los aprobadores finales.
1. Anotar. En cada organización, hay ciertas fechas que importan cada año y otras que surgirán. Asegúrese de recopilar las fechas relevantes de las partes interesadas y agregarlas como anotaciones para aumentar la comprensión de los datos que ven.
1. Depurar. Si su SDR es grande, podría ser abrumador. La parálisis de elección no se aplica solo a sus clientes. Vea lo que importa a cada grupo de usuarios y depure los elementos que verán.

## El por qué

_Obtenga información acerca de los requisitos de recopilación, la creación de una cultura de datos, la creación de una reflexión profunda sobre los datos, la creación de un sentido de propiedad sobre los datos y la simplificación de los datos._

### Recopilar requisitos

Reunir requisitos es obvio, pero hay varias formas efectivas de hacerlo. He utilizado entrevistas individuales, cuestionarios y revisiones de informes existentes. Esas estrategias funcionan, pero no tan bien como los métodos que acabo de describir. sin embargo, no creo que la diferencia entre los métodos para la recopilación de requisitos sea significativa. El método que he descrito te lleva al 95% de la manera, y estos otros métodos te llevan al 90% de la manera.

Entonces, ¿cuál es _por qué_?

### Generar referencia cultural de datos

Con este proceso, puede:

* Una reflexión profunda sobre cómo medir el éxito
* Cree un sentido de pertenencia en las partes interesadas
* Facilitar a las partes interesadas la comprensión de sus datos

### Una reflexión profunda sobre los datos

Para muchas de las personas de su compañía, los datos son algo que consumen. Lo usan. Lo analizan. Ellos no piensan profundamente en ello. Algunas personas heredaron informes y procesos de sus predecesores, pero no los han alterado por motivos de continuidad. Tal vez estas personas nunca tuvieron que pensar en _por qué_ de los datos.

Este proceso les da la oportunidad de _entender_ los datos. Hacer preguntas como: ¿Qué es el éxito? ¿Cómo sabrías si tuvieras éxito? ¿Cómo sabrías qué cambiar si no tuvieras éxito? Estas preguntas deben responderse al principio de la creación de cada sitio, aplicación y producto, pero muy a menudo no lo son. Al hacer estas preguntas, usted ayuda a profundizar la comprensión de una persona no solo de los datos, sino también de su producto.

### Crear un sentido de propiedad de los datos

Un sentido de propiedad no es algo que una persona adquiera fácilmente. No se encuentra en esa reunión de treinta minutos a la que asistió hace tres meses. No es creado por que un cuestionario molesto que respondieron demasiado rápido debido a otros problemas de trabajo urgentes como demostraciones y fechas de lanzamiento de sprint.

La propiedad es el producto del pensamiento profundo de alguien y de su trabajo con usted y sus colegas. Es lo que han revisado varias veces, proporcionado comentarios continuos para y lo que han aprobado después de incorporar dichos comentarios. ¡Es de ellos! El hecho de que sea útil se debe a ellos. Son _sus_ datos y es ese proceso el que los hizo suyos.

### Simplificación de los datos

También les has mostrado cómo usarán el proceso y cómo se verá a través de los [paneles de vista previa](#the-preview-dashboards). Cualquier nueva solución es _hard_. Hay mucho que aprender, y dada la tremenda capacidad de personalización de [!DNL Adobe Analytics], la curva de aprendizaje puede ser pronunciada. Pero has eliminado el 80% de eso. Incluso antes de que se haya escrito la primera línea de código, las partes interesadas saben cómo serán sus paneles. Ellos sabrán cómo leerlos y obtener significado de ellos. Sabrán cómo es el éxito literalmente porque le han dicho qué métricas y dimensiones definen el éxito. Y les has dicho cómo se visualizará ese éxito para ellos. La entrega de los paneles reales es un repaso, no una nueva tarea de aprendizaje que da miedo.

Esta no es necesariamente la forma más rápida de reunir un SDR. Es mucho trabajo y requiere una gran coordinación de horarios, especialmente porque es vital que tengas algunos ejecutivos en la mezcla. Sin embargo, al final, una solución de análisis empresarial es una enorme inversión de tiempo y dinero, y desea asegurarse de que la adopción y la satisfacción sean altas. Este método es muy útil para que esto suceda.

**Autor**

Este documento fue escrito por:

![gitai-headshot](assets/gitai-headshot-150.jpg)

Gitai Ben-Ammi, directora asociada de arquitectura empresarial en Accenture

[!DNL Adobe Analytics] campeón
