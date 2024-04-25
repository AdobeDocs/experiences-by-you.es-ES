---
title: Creación de una cultura de datos y una mejor referencia de diseño de soluciones
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
source-git-commit: 07b28edade263aa3c85348716bd45df4a053e239
workflow-type: tm+mt
source-wordcount: '1640'
ht-degree: 0%

---


# Creación de una cultura de datos y una mejor referencia de diseño de soluciones

**Revolucione su estrategia de datos y permita a su equipo crear un documento de referencia de diseño de soluciones (SDR) sólido. Elimine las brechas de medición y fomente una cultura de datos colaborativa a través de metodologías paso a paso.**

Por fin es el momento. Se crea una referencia de diseño de la solución (DRS) sólida. Esta es la guía que se usa para implementar métricas y dimensiones, como se llaman, cuando se activan y a los desarrolladores les encantó. Pasaste por todo el proceso de implementación, escribiste criterios de aceptación, pasaste por tus sprints, hiciste un control de calidad de todo, ¡y está hecho! Fue un montón de trabajo, y ahora está hecho. Su ejemplo de Adobe Analytics debe ser obtener marketing y productos que saltan hacia arriba y hacia abajo a medida que profundizan en los datos, obtienen nuevas revelaciones sobre sus clientes y encuentran todas las áreas de éxito y, bueno, las áreas de menos éxito. Pero no estás escuchando los elogios que esperabas.

Desde un campamento, se escuchan quejas.

&quot;¿Por qué no puedo averiguar la tasa de conversión en este canal?&quot;

&quot;¿Por qué no hay una métrica para esto?&quot;

&quot;¡Necesito más detalles sobre esto! Una métrica por sí sola no es suficiente. Hay al menos tres dimensiones diferentes que necesito para entender el rendimiento. ¿Por qué no los pusiste?&quot;

Pero es el otro campo el que es un motivo de preocupación aún mayor. De ellos, no se oye nada en absoluto. Pero mucho peor, se ven gráficos que fueron tomados muy claramente de su vieja solución de análisis, ya saben, la que ya no se mantiene, y cada día cae más en un pantano de decrepitud y datos sucios. Una sensación de temor te llena mientras piensas en las decisiones que se pueden tomar con ese desorden.

¿Qué ha fallado? ¿Por qué hay lagunas en la medición? ¿Por qué los miembros de su equipo no aceptan esto?

Empezaré por dejarte salir un poco de la trampa. Hay... *siempre* va a ser una revisión. Si su sitio o aplicación es lo suficientemente complejo como para necesitar una solución de análisis empresarial, básicamente se garantiza que se perderá algo. Pero no lo suficiente como para explicar los huecos de medición de los que estoy hablando. Lo que salió mal es mucho más difícil de poner en una hoja de cálculo. Se ha perdido la oportunidad de crear una cultura de datos colaborativa al mismo tiempo que creaba la SDR. Quiero guiarles por un método que mis colegas y yo hemos desarrollado tanto para crear un mejor SDR con menos lagunas como para conseguir que los usuarios finales se impliquen e incluso, ocasionalmente, se entusiasmen con su nueva instancia de Adobe Analytics. Vamos a repasar los programas y los por qué.

**El Cómo**

***La Conferencia de Medición:***

1. Reúne a las partes interesadas, ya sea en persona o virtualmente, con el objetivo de averiguar qué medir. Esto debería incluir a algunos ejecutivos.
1. Tenga ya algunos ejemplos obvios en el tablero en las notas adhesivas, cosas como ingresos, ventas o posibles clientes, se medirán los KPI muy importantes que conoce. Repita este proceso con dimensiones, cosas como estado de inicio de sesión, categorías de productos o términos de búsqueda.
1. Haga que todos agreguen sus propias notas adhesivas, agrupándolas según sea necesario
1. Haga que la gente vote las que crea que son importantes. Son votos ilimitados, ya que quizá todas estas métricas y dimensiones importen.
1. En el caso de los que tengan votos bajos, pida a las partes interesadas que les pidan que expliquen para qué los utilizarán. Si hay un buen caso de uso, manténgalo dentro. Si hay una mejor manera de obtener esos datos, no pueden explicar cómo es procesable, o hay otra buena razón para dejarlo fuera, golpearlo desde el tablero.
1. Añada estas métricas y dimensiones a la SDR para que las partes interesadas que estuvieron presentes las revisen por primera vez

***El mapa del canal***

1. Obtenga una visualización de todos los canales, paso a paso con cada estado incluido
1. Con los diseñadores y los gestores de producto, revise cada paso y hable de lo que consideran éxito en ese canal. ¿Es la tasa de conversión? ¿Está eligiendo una ruta en particular? ¿Está usando ciertas características?
1. Haga preguntas sobre qué métricas y dimensiones son necesarias para comprender el rendimiento del canal en cada paso del canal y en general.
1. Por encima de cada paso del canal, añada las métricas y dimensiones que se medirán en ese paso, incluidas las métricas calculadas.
1. Al principio de cada canal, escriba los informes que irán en el panel que el gestor de producto utilizará para rastrear el rendimiento, cosas como un informe de visitas en el orden previsto, tasas de conversión del mes actual y de tendencias y cualquier cosa más específica para ese canal.
1. Añada las nuevas métricas y dimensiones que haya descubierto a la SDR y envíelas a las partes interesadas para una segunda revisión.

***Los paneles de previsualización***

1. Con el mapa de canal como guía, cree paneles de prueba.
1. Debe haber una vista general, como un Tablero de resumen ejecutivo, y paneles para cada uno de los canales.
1. También habrá algunas más específicas para su sitio o aplicación, como el rendimiento del producto o el rendimiento del contenido.
1. Distribuya estos elementos a las partes interesadas relevantes y obtenga comentarios sobre el diseño.
1. Realice las actualizaciones solicitadas y, si se necesitan nuevas métricas o dimensiones, agréguelas a la SDR.
1. Envíe los paneles de vista previa actualizados y la SDR para una revisión final.

***Herramientas de democratización de datos***

1. Crear un diccionario de datos. La SDR es para sus desarrolladores. El diccionario de datos es para los usuarios finales. Hacerlo legible para los usuarios finales, de modo que puedan buscar fácilmente qué datos están disponibles y cómo utilizarlos. Los usuarios finales deben ser los aprobadores finales.
1. Anotaciones. En cada organización, hay ciertas fechas que importan cada año y otras que surgirán. Asegúrese de recopilar las más relevantes de las partes interesadas y agregarlas como anotaciones para aumentar la comprensión de los datos que ven.
1. Revisión. Si su SDR es grande, podría ser abrumador. La parálisis de elección no se aplica solo a sus clientes. Vea lo que importa a cada grupo de usuarios y depure los elementos que verán.

**El por qué**

***Para obtener requisitos***

Esto es obvio, pero hay otras formas eficaces de obtener los requisitos. Personalmente he utilizado una a una entrevistas, cuestionarios y revisiones de informes existentes. Funcionarán, aunque creo que no tan bien como los métodos que acabo de esbozar. Sinceramente, no creo que la brecha en la recopilación de requisitos sea tan grande. El método que he descrito te dará el 95% del camino, y estos otros métodos te darán el 90% del camino. Entonces, ¿cuál es el gran por qué?

***Para generar una referencia cultural de datos***

Con este proceso, puede:

- Una reflexión profunda sobre cómo medir el éxito
- Cree un sentido de pertenencia en las partes interesadas
- Facilitar a las partes interesadas la comprensión de sus datos

***Generando reflexión profunda sobre los datos***

Para muchas de las personas de su compañía, los datos son algo que consumen. Lo usan. Lo analizan. Ellos no piensan profundamente en ello. Algunos de ellos heredaron informes y procesos de sus predecesores, pero no se han alterado debido a la necesidad de continuidad. Nunca han necesitado pensar en el por qué de los datos.

Este proceso les da la oportunidad de *entender* datos. Haciendo las preguntas, ¿qué es el éxito? ¿Cómo sabrías si tuvieras éxito? ¿Cómo sabrías qué cambiar si no tuvieras éxito? Este es un ejercicio que debe realizarse al principio de la creación de cada sitio, aplicación y producto, pero muy a menudo no lo es. Al hacer estas preguntas, ayuda a profundizar su comprensión no solo de los datos, sino también de su propio producto.

***Creación de un sentido de propiedad sobre los datos***

Esto no es algo que fue transmitido desde lo alto. Esto no es algo que era una reunión de treinta minutos hace tres meses. Este no es el molesto cuestionario que fueron acosados durante una semana para responder y que lo hicieron con prisa porque tenían una demostración a la que llegar para poder hacer la fecha de lanzamiento del sprint. Este es el producto de su profunda reflexión y de su trabajo con usted y sus colegas, algo que han revisado varias veces, proporcionado comentarios continuos para, y que han aprobado después de que se incorporaran los comentarios. ¡Es de ellos! El hecho de que sea útil se debe a ellos. Es... *sus* y es el proceso lo que lo hizo suyo.

***Facilitar la comprensión de los datos***

También les ha mostrado cómo lo utilizarán y cómo se verá a través de los paneles de vista previa. Cualquier nueva solución es *difícil*. Hay mucho que aprender y, dada la tremenda capacidad de personalización de Adobe Analytics, la curva de aprendizaje puede ser bastante pronunciada. Pero has eliminado el 80% de eso. Incluso antes de que se haya escrito la primera línea de código, las partes interesadas saben cómo serán sus paneles. Ellos sabrán cómo leerlos y obtener significado de ellos. Sabrán cómo es literalmente el éxito porque les han dicho qué métricas y dimensiones definen el éxito, y usted les ha dicho cómo se visualizará para ellos. La entrega de los paneles reales es un repaso, no una nueva tarea de aprendizaje que da miedo.

Esta no es la forma más rápida de reunir un SDR. Es mucho trabajo y requiere de una gran coordinación de horarios, sobre todo porque es vital que tengas algunos ejecutivos en la mezcla. Sin embargo, al final, una solución de análisis empresarial es una enorme inversión de tiempo y dinero, y desea asegurarse de que la adopción y la satisfacción sean altas. Este método es muy útil para que esto suceda.

**Autor**

Este documento fue escrito por:

![disparo en la cabeza de gitai](assets/gitai-headshot-150.jpg)

Gitai Ben-Ammi, directora asociada de arquitectura empresarial en Accenture

Campeona de Adobe Analytics

