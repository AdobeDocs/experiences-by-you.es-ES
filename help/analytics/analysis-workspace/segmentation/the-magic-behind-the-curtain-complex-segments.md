---
title: 'La magia detrás de la cortina: segmentos complejos; exclusiones, contenedores y atribución'
description: _Descubra las complejidades de la segmentación de datos compleja, explorando exclusiones, contenedores y modelos de atribución. Como el truco de un mago, dominar estas técnicas permite a los analistas realizar magia de datos, transformando perspectivas con precisión y delicadeza.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
duration: 36000
last-substantial-update: 2024-03-25T00:00:00Z
jira: KT-15200
thumbnail: KT-15200.jpeg
exl-id: 1da85e88-64b3-49e5-9bf6-76126ac9f6ad
source-git-commit: 69fa16c1bf38604e4dabc553baee71598be83db3
workflow-type: tm+mt
source-wordcount: '4102'
ht-degree: 1%

---

# La magia detrás de la cortina: Segmentos complejos: exclusiones, contenedores y atribución

_Descubra las complejidades de la segmentación de datos compleja y explore las exclusiones, los contenedores y los modelos de atribución. Al igual que el juego de manos de un mago, el dominio de estas técnicas permite a los analistas realizar magia de datos, transformando las perspectivas con precisión y delicadeza._

Las cortinas están abiertas, el escenario está listo... esto puede no ser un acto de magia de Las Vegas, pero podemos realizar algunos trucos bastante sorprendentes al construir nuestros segmentos.

![Manos_Mágicas](assets/magician-hands.jpeg)

Dentro de este módulo cubriremos:

- Excluir lógica
- Uso de contenedores
- Modelo de atribución

## Incluir frente a excluir

De manera predeterminada, todos los contenedores comienzan como tipo **include**, lo que básicamente significa que devuelven los datos que coinciden con los criterios. Sin embargo, también puede cambiar el segmento o los contenedores dentro de los segmentos para que sean del tipo **exclude**, lo que le permitirá rechazar determinados criterios.

Si bien un mago puede encontrar tu carta en la baraja, es increíble cuando ese mago puede hacer que el resto de la baraja no exista. Del mismo modo, en los segmentos de exclusión, queremos que los datos no deseados simplemente desaparezcan de nuestro conjunto de datos.

![tarjetas en blanco](assets/blankcards.png)

Podrían estar sentados pensando, &quot;Ok, pero ya tengo las opciones &#39;No es igual&#39; y &#39;No contiene&#39;, ¿no debería cubrirme?&quot; Desafortunadamente, la respuesta a eso es no... y no se trata solo de poder excluir grupos de lógica, sobre un solo elemento. Incluso cuando se trata de un solo componente, a menudo necesitará usar *excluye* para lograr su objetivo.

- **No contiene / No es igual a** - Es exactamente como suena, coincide en elementos que no contienen una cadena específica
- **Excluir: el valor contiene / es igual a** - Esto *excluirá* elementos que coincidan con la cadena

A primera vista, ambos suenan igual... y en los contenedores/segmentos de nivel **hit**, usted estaría en lo correcto, ya que realizarán la misma acción. Sin embargo, al usar el ámbito **visita** o **visitante**, obtendrá resultados muy diferentes.

**Figura 1: No contiene / no es igual a - Ámbito de la visita**

![Figura1-DnceVsExclude-Hit](assets/figure1-dnce-vs-exclude-hit.png)

*Observe que cada visita devuelve un valor verdadero o falso y que esos valores se invierten entre no y excluir.*

- No contiene &quot;Value&quot; (Sí), por lo tanto devuelve true e incluye esa visita; del mismo modo, no contiene &quot;Example&quot; (no, lo contiene), por lo tanto devuelve false y no incluye esa visita. Básicamente, devuelva cualquier dato que devuelva un resultado verdadero.
- Si &quot;Value&quot; contiene &quot;Example&quot; (no) y, por lo tanto, devuelve false y no excluye esa visita; del mismo modo, si &quot;Example&quot; contiene &quot;Example&quot; (sí) y, por lo tanto, devuelve true y excluye esa visita. Básicamente, devuelve datos que **no** tienen un resultado verdadero o devuelve datos que son falsos según tus criterios.
- Puede ver que en el nivel de **visita individual**, ambos conjuntos de lógica devolverán el mismo conjunto de datos.

**Figura 2: No contiene / no es igual a - Ámbito de la visita**

![Figura2-DnceVsExclude-Visit](assets/figure2-dnce-vs-exclude-visit.png)

*Como en el caso anterior, cada visita individual dentro de la **visita**se evaluará con el mismo valor verdadero/falso. Sin embargo, el conjunto de datos devuelto es el de toda la visita.*

- En cada visita individual, &quot;Value&quot; no contiene &quot;Example&quot; (sí), por lo que devuelve el valor &quot;True&quot;; del mismo modo, no contiene &quot;Example&quot; (no, lo contiene), por lo que devuelve el valor &quot;False&quot;.
   - Si la visita de **any** en la visita devuelve **true**, entonces se devuelve **toda la visita**.*
   - Si la visita estaba compuesta totalmente por visitas que contenían &quot;Ejemplo&quot;, entonces ninguna visita devolverá un valor verdadero y, por lo tanto, esa visita **no se devolverá** en su conjunto de datos.
- De nuevo, en cada visita individual el &quot;Ejemplo&quot; contiene &quot;Ejemplo&quot; (sí), por lo que devuelve el valor &quot;True&quot;
   - Si **cualquier visita** devuelve **true**, toda la visita se **excluirá**
   - Si **todas las visitas** de la visita devuelven **falso**, se devolverá esa visita en el conjunto de datos
- Ahora pueden ver dónde esta lógica empieza a divergir. En el ejemplo anterior hay tres visitas distintas:
   - Si se usa &quot;No contiene/es igual que&quot; **se devolverán dos de las tres** visitas.
   - Al usar &quot;Excluir contiene / es igual que&quot; **solo se devolverá una** de esas visitas

**Figura 3: No contiene / no es igual a - Ámbito de la visita**

![Figura3-DnceVsExclude-Visitor](assets/figure3-dnce-vs-exclude-visitor.png)

*Al igual que arriba, cada visita realizada por el **visitante**se evaluará con la misma lógica verdadero/falso. Pero ahora estamos viendo todas las visitas que este visitante ha realizado, en todas las visitas (dentro del intervalo de fechas seleccionado).*

- En cada visita individual, &quot;Value&quot; no contiene &quot;Example&quot; (sí), por lo que devuelve el valor &quot;True&quot;; del mismo modo, no contiene &quot;Example&quot; (no, lo contiene), por lo que devuelve el valor &quot;False&quot;.
   - Si **cualquier** visita realizada por el visitante devuelve **verdadero**, entonces se devuelve **toda la visita**.
   - Si el visitante nunca realizó ninguna visita que contuviera &quot;Ejemplo&quot;, entonces ninguna visita devolvería el valor &quot;True&quot; y, por lo tanto, ese visitante **no sería devuelto** en su conjunto de datos.
- De nuevo, en cada visita individual el &quot;Ejemplo&quot; contiene &quot;Ejemplo&quot; (sí), por lo que devuelve el valor &quot;True&quot;.
   - Si **cualquier visita** devuelve **true**, se **excluirá a todo el visitante (y posteriormente a todas sus visitas).**
   - Si **todas las visitas** de la visita devuelven **falso**, se devolverá ese visitante en el conjunto de datos y, por lo tanto, se devolverá con éxito a los visitantes que no hicieron &quot;X&quot;.
- Esta es una extensión de la lógica de visita, donde hay incluso más consideraciones. En el ejemplo anterior hay dos visitantes diferentes, con 3 visitas cada uno:
   - Si se usa &quot;No contiene/es igual que&quot;, se devolverán **ambos** visitantes, al igual que las **tres** visitas (que representan 2 visitantes y 6 visitas totales en los informes)
   - Al usar &quot;Excluir contiene / es igual a&quot; **solo se devolverá uno** de esos visitantes, y solo se incluirán las tres visitas asociadas a ese visitante (que representan 1 visitante y 3 visitas totales en sus informes)

>[!TIP]
>
>Esta lógica puede ser compleja, especialmente cuando comienza a anidar contenedores... siempre es buena idea realizar pruebas con datos de muestra controlados para asegurarse de que el segmento devuelva los datos que cree que debería.

### Ejemplo de segmento 1: Excluir las visitas que realizan una compra

En este ejemplo, quiero segmentar usuarios que llegaron a un sitio y que *no* realizaron una compra durante su visita (básicamente, quiero excluir las visitas que realizaron una transacción; por lo tanto, me quedaré con las visitas que no completaron una transacción)

![Segmento1A-VisitLevelExclude](assets/segment-example-1/segment1a-visit-level-exclude.png)

Para comparar, veamos un segmento que se ha creado con &quot;No existe&quot;:

![Segmento1B-VisitaNoExiste](assets/segment-example-1/sement1b-visit-does-not-exist.png)

Observe cómo la vista previa muestra un resultado muy diferente. De hecho, este segmento devolverá el 100 % de mis visitas, ya que cada visita tiene al menos una visita que no incluye la métrica &quot;Pedido&quot;.

Para ilustrar esto más adelante, vamos a comparar los dos segmentos en paralelo:

![Segment1C-ComparisonTable](assets/segment-example-1/sement1c-comparison-table.png)

Primero, puede ver que a pesar del ámbito de nivel del segmento de *visita*, podemos emparejar el segmento con otras métricas (como vistas de página o visitantes únicos). El primer conjunto de columnas está sin segmentar, para mostrar de un vistazo que un segmento (no existe) devuelve casi el 100 % de los datos, solo el segmento de exclusión hace lo que necesitamos que haga.

La columna más destacable son los pedidos, que deberían ser inmediatamente obvios de que el contenedor &quot;No existe&quot; es incorrecto, ya que la mayoría de los pedidos aún se están devolviendo.

### Ejemplo de segmento 2: Excluir visitantes que han realizado una compra dentro del periodo del informe

En este ejemplo, quiero utilizar las ideas de la muestra anterior (que miraba específicamente en el nivel de visita) y expandirla para encontrar los visitantes que no han realizado una compra en el lapso de tiempo de mi informe.

Este segmento será muy similar al ejemplo anterior, casi idéntico, pero el ámbito del segmento va a marcar una gran diferencia.

![Segmento2A-VisitorLevelExclude](assets/segment-example-2/segment2a-visitor-level-exclude.png)

Ahora, si comparamos el segmento con alcance de visitante con el segmento con alcance de visita anterior, verá que se excluyen muchos más datos y muchas más visitas, ya que *los visitantes que realizaron compras* también tuvieron visitas en las que no se realizaron compras, y por lo tanto, esas visitas también se excluyen ya que forman parte del ciclo de vida del visitante.

>[!IMPORTANT]
>
>Cuando se buscan datos con ámbito de visitante, cuanto más largo sea el lapso de tiempo del informe, mayor será la exclusión, ya que muchos visitantes serán visitantes fieles que regresan al sitio (por supuesto, algunos modelos comerciales verán un impacto mayor que otros)

![Tabla de comparación de Segmento2B](assets/segment-example-2/sement2b-comparison-table.png)


>[!IMPORTANT]
>
>Aunque las diferencias entre la visita y el visitante pueden ser *sutiles* (especialmente en estos datos de ejemplo), son una lógica única que se debe tener en cuenta. Los datos pueden ser sorprendentemente diferentes según el sitio y los comportamientos de los usuarios.


Es importante saber exactamente qué datos o qué *historia* intenta contar con su informe. Para realizar el análisis adecuado, es fundamental asegurarse de que las tablas y visualizaciones indiquen claramente a la audiencia ***qué*** se está mostrando, y utilizar el modelo de segmentos adecuado. Las decisiones informadas solo se pueden tomar correctamente si todos entienden lo que están viendo.

## Uso de contenedores

Los contenedores nos proporcionan la capacidad de crear &quot;sublógica&quot; dentro de la lógica principal del segmento y una idea errónea común es que el ámbito debe ser el mismo entre el segmento y el contenedor... pero no es así. Esto nos da más libertad para crear escenarios específicos en el mayor esquema de las cosas, para construir lógicas complejas.

La mejor manera de pensar en los contenedores es imaginar que cada contenedor es una caja, y que podemos apilar cajas (de lógica) dentro de otra caja, dentro de otra caja... pero a diferencia de las cajas físicas donde cada caja debe ser más pequeña que la caja exterior, podemos poner algo más grande dentro si eso nos impulsa a recuperar los datos correctos. Piensen en ello como en un sombrero de mago, donde lo imposible cabe dentro y nosotros somos los magos de los datos...

![Conejo_en_sombrero](assets/rabbit-in-hat.jpeg)

### Ámbito de los contenedores

Primero hagamos un desglose rápido del ámbito *contenedor*. Al igual que *segmento s* cope, tiene las opciones de ámbito de **visita**, **visita** y **visitante** básicas, pero a veces también verá algo llamado **grupo lógico** en lugar de visitante (esto solo ocurrirá en segmentos secuenciales, y los explicaremos en el siguiente artículo).

Se puede agregar contenedores dentro del segmento (o dentro de otros contenedores) si se accede al menú **options*** (cuando anide varios elementos, tenga cuidado de agregarlos al bloque correcto, aunque afortunadamente puede arrastrar y soltar contenedores dentro de la interfaz si no los agrega a la ubicación incorrecta)

**Figura 1: Agregando un contenedor**

![Figura1-AgregandoContenedor](assets/figure1-adding-container.png)

El ámbito de un contenedor es independiente del principal, como mencioné anteriormente, estos *no* tienen que coincidir, y dependiendo de lo que quieras devolver, es posible que tengas que dibujar el plan para visualizar completamente lo que necesitas, al menos hasta que te sientas cómodo visualizándolo en tu cabeza.

**Figura 2: Ámbito del segmento vs. ámbito del contenedor**

![Figura2-SegmentScopeVsContainerScope](assets/figure2-segment-scope-vs-container-scope.png)

>[!NOTE]
>
>El Adobe tiene lógica para comprender los segmentos válidos y no válidos, no le proporcionarían opciones que *nunca* funcionarían... por lo que si ve la opción de usar un contenedor con ámbito de visitante dentro de un segmento con ámbito de visita, significa que es una opción válida.

Al igual que para los segmentos básicos, cuando empieza a generar un segmento complejo con contenedores anidados, necesita tener una idea clara sobre ***qué tipo de datos*** desea que se devuelvan. ***Cómo*** planea usar esos datos? ***¿Qué*** métricas planea emparejar con el segmento?

Estas preguntas ayudarán a determinar cuál será el ámbito del segmento en su conjunto, este es el punto de partida para cualquier segmento.

El hecho de que planee emparejar un segmento con su métrica de visitantes únicos no significa que el propio segmento deba ser de nivel de visitante... muy diferente. Un segmento de nivel de visitante devolverá todos los datos de un visitante... esto significa todas sus visitas, todas sus vistas de página, etc. Una vez que un visitante coincida con los criterios del segmento, el segmento podría empezar a devolver datos del *pasado* para este visitante (siempre y cuando esté dentro del intervalo de fechas de su área de trabajo).

>[!IMPORTANT]
>
>Incluso cuando planea emparejar un segmento con la métrica de visitantes únicos, este *no significa* que el segmento deba ser automáticamente ámbito de visitante... Esta idea errónea *podría* crear resultados inflados e incorrectos.

Por lo tanto, he hablado mucho sobre los conceptos de cómo seleccionar el ámbito adecuado, pero no he proporcionado ejemplos o detalles específicos que realmente le ayudarán... así que vamos a profundizar en eso ahora con algunos ejemplos de casos de uso reales. Dicen que un mago nunca revela sus secretos, pero eso no es del todo cierto. Dentro del mundo mágico, las técnicas y los trabajos &quot;detrás de la cortina&quot; a menudo se comparten con compañeros, permitiéndoles construir y mejorar la ilusión, y eso es lo que intento hacer... para abrir la puerta a las posibilidades que les esperan.

### Ejemplo de segmento 3: Vistas de páginas específicas de visitantes que han realizado un pedido reciente (dentro del período de informe)

En este caso, solo deseo devolver un conjunto de páginas específicas que han sido visitadas por compradores recientes (tenga en cuenta que aún puedo emparejar esto con visitas o visitantes únicos, aunque el segmento en sí mismo se encuentre en el ámbito de VISITA INDIVIDUAL).

Este tipo de escenario es bueno para ver si tengo compradores que buscan páginas específicas en un sitio o páginas que pueden no estar conectadas explícitamente a un evento específico.

Mi ejemplo es ir a las páginas de &quot;Ofertas destacadas&quot; y &quot;Productos recomendados&quot;. Actualmente, vamos a mantener la lógica simple y no entrar en la segmentación secuencial (al menos aún no, pero abordaremos una lógica más compleja como esa en un artículo futuro).

Otra pregunta es **¿por qué** estamos retrocediendo con las visitas? Técnicamente podría extraer por Visitas o Visitantes aquí, pero también podría querer ver estas páginas específicas por **vistas de página (para el conjunto de páginas específico) por visita** o **vistas de página (para el conjunto específico) por visitante**, este ámbito me da la flexibilidad para realizar esta matemática específica. Dado que estas visitas se pueden asociar fácilmente con visitas o visitantes únicos para determinar el número de visitas o visitantes que ven estas páginas, optaré por el segmento más flexible que pueda utilizar para todos los escenarios.

En primer lugar, para comparar, le presentamos un segmento simple basado en VISITAS para las páginas específicas.

![Segment3A-HitLevelPages](assets/segment-example-3/segment3a-hit-level-pages.png)

Ahora, vamos a construir en la complejidad:

![Segmento3B-MultipleContainersHitAndVisitor](assets/segment-example-3/segment3b-multiple-containers-hit-and-visitor.png)

Observarán que no sólo utilizo varios contenedores, sino que estoy mezclando el ámbito de esos contenedores. El segmento en su conjunto está en el nivel de VISITA INDIVIDUAL, pero también busco VISITANTES que hayan realizado un pedido.

![Tabla de comparación de segmentos3C](assets/segment-example-3/segment3c-comparison-table.png)

Vamos a pasar un poco de tiempo para desempaquetar esto, ya que hay mucho que hacer.

En primer lugar, en lugar de mostrar un desglose diario, estoy mostrando un desglose de página, ya que creo que esto ayudará a ilustrar mejor los dos segmentos.

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Las tres primeras columnas (Vistas de página, visitas y visitantes únicos) no están segmentadas y, por lo tanto, muestran todas las páginas del sitio. Tenga en cuenta que no he incluido pedidos aquí, ya que los pedidos se rastrean en una acción y, por lo tanto, no forman parte del ámbito de la dimensión de página.</td>
        <td style="border: 0;">&lt;img src="assets/segment-example-3/segment3c-comparison-table-detail1.png" width="352"
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">A continuación, se muestra el resultado del segmento simple, con solo <strong>visitas</strong> en las dos páginas especificadas. Observará que las demás páginas del desglose resultan en 0, tal como se espera.</td>
        <td style="border: 0;">&lt;img src="assets/segment-example-3/segment3c-comparison-table-detail2.png" width="352"
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Ahora, aquí hay un pequeño consejo adicional, antes de mostrar el resultado del segmento avanzado, utilicé otro segmento simple de "Pedidos existen" (en un ámbito de nivel de VISITA), y lo emparejé con visitantes únicos. Esto me devolverá el total de UV que hicieron pedidos en mi período de informe, así como los UV que tocaron cada una de esas páginas... esto ayudará a ilustrar mejor el siguiente conjunto de columnas.</td>
        <td style="border: 0;">&lt;img src="assets/segment-example-3/segment3c-comparison-table-detail3.png" width="352"
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">El conjunto final de columnas se apilan con mi segmento complejo. Los UV generales con pedidos coinciden con el segmento simple "Pedidos existen" en cada página, pero notará que el total es significativamente diferente; ya que este conjunto de datos restringe explícitamente el conjunto de datos solo a los visitantes que realizaron pedidos Y visitaron las páginas, estoy explícitamente interesado en.</td> <td style="border: 0;"><img src="assets/segment-example-3/segment3c-comparison-table-detail4.png" width="352">
        </td>
    </tr>
</table>

### Ejemplo de segmento 4: Visitas que visitan ofertas destacadas O productos recomendados Y realizan un pedido dentro de la misma visita

El ejemplo anterior muestra cómo se puede agregar un contenedor de ámbito mayor (es decir, visitante) dentro de un contenedor de ámbito más pequeño (es decir, una visita individual para que no sea de extrañar que se puedan agregar contenedores de visita individual dentro de segmentos con ámbito de visitante o visita.

Usando algunas de las mismas páginas que estábamos viendo anteriormente, ahora solo nos importa recuperar a los visitantes que visitaron las ofertas destacadas O la página de productos recomendados Y realizaron un pedido en la misma visita.

![Segment4A-VisitorWithVisit](assets/segment-example-4/segment4a-visitor-with-visit.png)

Este segmento combina los tres ámbitos. El nivel superior del segmento es visitante, por lo que se asegurará de que se devuelvan TODAS las visitas de todas las visitas del visitante coincidente. Dentro de él, hemos agregado un contenedor de ámbito de visita, que va a garantizar que el visitante debe haber tenido al menos una visita que coincida con los criterios específicos de hacer un pedido Y haber visitado páginas específicas. Hemos agregado un contenedor de ámbito de visita para las propias páginas, de modo que podemos utilizar la lógica OR para buscar la página de ofertas destacadas O la página de productos recomendados.

La ventaja de este segmento con ámbito de visitante es que devolverá **TODAS** las visitas de los visitantes que cumplan con este criterio, por lo que este segmento será bueno si quiero ver los comportamientos de las visitas anteriores que llevaron a esta combinación y las acciones de estos visitantes después de este escenario.

![Segment4B-ComparisonTable](assets/segment-example-4/segment4b-comparison-table.png)

Aquí estoy comparando las visitas en ofertas destacadas/contenido recomendado, con los pedidos que existen, con el segmento complejo en el que tanto el pedido como una de las páginas especificadas existen en la misma visita. En el segmento complejo es donde se cruzan los dos primeros segmentos, pero como es el ámbito del visitante, también se devolverán todas las demás visitas de esos visitantes.

## Modelo de atribución

El modelado de atribución dentro de una definición de segmento pertenece principalmente a dimensiones que tienen una caducidad que no es de visita, por lo que las props (que siempre son de nivel de visita) no son realmente una buena candidata. Sus eVars, canales de marketing, etc. sin embargo, son para los que están diseñados estos ajustes.

Antes de mirar el segmento, deberíamos hacer una revisión rápida de cómo funciona el modelado de atribución en un ejemplo sencillo.

Digamos que tenemos dos eVars, una de ellas está configurada para visitar la caducidad (eVar 1) y una de ellas está configurada para una caducidad de 30 días (eVar 2). Para simplificar, se va a realizar el seguimiento de una campaña interna (icid).

**Visita 1**

- Página A
   - **eVar 1** no está establecido
   - **eVar 2** no está establecido
- Haga clic en el banner de promoción con ?icid=promo-banner en la URL.
- Página B
   - **eVar 1** y **eVar 2** se han configurado como &quot;promo-banner&quot;
   - **Se ha activado la instancia de eVar 1**
   - **Se ha activado la instancia de eVar 2**
- Página C
   - Tanto **eVar 1** como **eVar 2** mantienen el valor &quot;promo-banner&quot;
   - Ninguna de las métricas de instancia de las eVars se activa, ya que ambas eVars utilizan valores persistentes

**Visita 2**

- Página D
   - **eVar 1** no se ha establecido en ningún valor y no se ha activado **instancia de eVar 1**
   - **eVar 2** mantiene el valor &quot;promo-banner&quot; debido a la caducidad de 30 días
   - **La instancia de eVar2** no se ha activado porque el valor es persistente y no se ha establecido
- Haga clic en Promoción de carril lateral con ?icid=promo-side-rail en la URL
- Página E
   - **eVar 1** y **eVar 2** están configurados en &quot;promo-side-rail&quot;
   - **Se ha activado la instancia de eVar 1**
   - **Se ha activado la instancia de eVar 2**
- Página F
   - Tanto **eVar 1** como **eVar 2** mantienen el valor &quot;promo-side-rail&quot;
   - Ninguna de las métricas de instancia de las eVars se activa, ya que ambas eVars utilizan valores persistentes

Actualmente, aquí está el resultado esperado de estas dos visitas:

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top"></th><th colspan="1" valign="top"><b>Page Views</b></th><th colspan="1" valign="top"><b>Visitas</b></th><th colspan="1" valign="top"><b>Instancia de eVar 1</b></th><th colspan="1" valign="top"><b>Instancia de eVar 2</b></th></tr>
<tr><td colspan="1" valign="top"></td><td colspan="1" valign="top"></td><td colspan="1" valign="top">6</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" rowspan="7" valign="top">Página</td><td colspan="1" valign="top"></td><td colspan="1" valign="top">6</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" valign="top">Página A</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
<tr><td colspan="1" valign="top">Página B</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">Página C</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
<tr><td colspan="1" valign="top">Página D</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
<tr><td colspan="1" valign="top">Página E</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">Página F</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">0</td><td colspan="1" valign="top">0</td></tr>
</table>

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top"></th><th colspan="1" valign="top"><b>Page Views</b></th><th colspan="1" valign="top"><b>Visitas</b></th><th colspan="1" valign="top"><b>Instancia de eVar 1</b></th></tr>
<tr><td colspan="1" valign="top"></td><td colspan="1" valign="top"></td><td colspan="1" valign="top">4</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">EVAR 1</td><td colspan="1" valign="top"></td><td colspan="1" valign="top">4</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" valign="top">promo-banner</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">promo-side-rail</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
</table>

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top"></th><th colspan="1" valign="top"><b>Page Views</b></th><th colspan="1" valign="top"><b>Visitas</b></th><th colspan="1" valign="top"><b>Instancia de eVar 2</b></th></tr>
<tr><td colspan="1" valign="top"></td><td colspan="1" valign="top"></td><td colspan="1" valign="top">5</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">EVAR 2</td><td colspan="1" valign="top"></td><td colspan="1" valign="top">5</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">2</td></tr>
<tr><td colspan="1" valign="top">promo-banner</td><td colspan="1" valign="top">3</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td></tr>
<tr><td colspan="1" valign="top">promo-side-rail</td><td colspan="1" valign="top">2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">1</td></tr>
</table>

Ahora, veamos dónde puede establecer la atribución en el segmento.

**Figura 4: Modelo de atribución**

![Figura4-Modelo de atribución](assets/figure4-attribution-model.png)

*El icono de engranaje en su dimensión es donde puede establecer la atribución. Cada opción tiene información disponible al pasar el puntero sobre &quot;?&quot; icono. Básicamente:*

- El comportamiento predeterminado devolverá todas las instancias del eVar en las que se haya establecido el valor (ya sea de forma específica o a través de la atribución set)
- Instancia solo devolverá la dimensión donde el valor esté establecido explícitamente (es decir, en las visitas individuales donde se activa la &quot;Instancia de eVar&quot;)
- La instancia no repetida solo devolverá la primera vez que se establezca el valor de la dimensión (es decir, aunque no se trata en el ejemplo anterior, imagine que el usuario ha hecho clic en el banner de promoción varias veces, esto también incrementaría la &quot;Instancia de eVar&quot; cada vez que se hace clic en el banner; esta configuración solo tomaría la primera instancia única de &quot;promo-banner&quot; e ignoraría los recuentos posteriores de este banner)

### Ejemplo de segmento 5: Canal de marketing &quot;Búsqueda de pago&quot; frente a las instancias directas de búsqueda de pago

Como todos debemos saber, los canales de marketing tienen un modelo de atribución largo (30 días de forma predeterminada, pero esto podría personalizarse según sus propias necesidades), y una vez configurado, el canal de marketing no se sobrescribirá con las posteriores visitas &quot;directas&quot; al sitio, para que sus controladores específicos obtengan la atribución de conversión. Sin embargo, a veces necesita ver específicamente las ***entradas*** en el sitio por un canal de marketing específico; y por entradas, quiero decir que necesita ver cuándo se establece específicamente el canal de marketing en función de sus reglas de procesamiento de marketing.

Cambiemos las cosas y empecemos por ver las comparaciones, luego vamos a adentrarnos en los segmentos.

![Segment5A-TableComparison](assets/segment-example-5/segment5a-table-comparison.png)

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Las primeras 4 columnas no están segmentadas y deberían ser fáciles de entender. Tenga en cuenta que *"Entradas"* es básicamente un valor calculado basado en el lugar donde los visitantes inician la sesión. Lo he agregado aquí para mostrar que esto no devuelve la información que estamos buscando, ya que los usuarios pueden entrar al sitio a través de múltiples canales de marketing (mirando las redes sociales, haciendo búsquedas, haciendo clic en correos electrónicos de marketing, etc.). todos dentro de la misma visita/sesión).</td> <td style="border: 0;"><img src="assets/segment-example-5/segment5a-table-comparison-detail1.png" width="352">
        </td>
    </tr>
</table>

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">El siguiente conjunto de columnas utiliza un "Segmento de visita estándar", que básicamente busca las visitas individuales donde el canal de marketing es "Búsqueda de pago". Sin embargo, esto devolverá TODAS las visitas en función de la atribución del canal de marketing, no aislará las pulsaciones de "Búsqueda de pago" reales. Por lo tanto, esto no devolverá los datos que necesitamos.</td> <td style="border: 0;"><img src="assets/segment-example-5/segment5a-table-comparison-detail2.png" width="352">
        </td>
    </tr>
</table>


![Segmento5A-VisitaBúsquedaPagada](assets/segment-example-5/segment5a-paid-search-hit.png)

<table style="border: 0;">
    <tr>
        <td width="352" style="border: 0;">Ahora, los dos siguientes conjuntos de datos parecen idénticos y, de hecho, devuelven los mismos datos de dos formas diferentes. Pero ahora busco específicamente las <i>instancias</i> en las que el canal de marketing estaba <strong>establecido</strong> en "Búsqueda de pago".</td> <td style="border: 0;"><img src="assets/segment-example-5/segment5a-table-comparison-detail3.png" width="352">
        </td>
    </tr>
</table>

Esto se puede hacer de dos maneras:

En primer lugar, se usa la atribución de dimensión &quot;estándar&quot; y se empareja con la métrica específica &quot;Instancia de canal de marketing&quot; (ya que *existe* lógica):

![Segment5A-PaidSearchHitANDInstanceExists](assets/segment-example-5/segment5a-paid-search-hit-and-instance-exists.png)

O segundo, para un segmento más sencillo, puede cambiar la atribución a Instancia. Tenga en cuenta que el nombre de la dimensión cambiará de &quot;Canal de marketing&quot; a &quot;Canal de marketing (instancia)&quot;.

![Segment5A-PaidSearchHitInstance](assets/segment-example-5/segment5a-paid-search-hit-instance.png)

## Poniéndolo todo junto

Como cualquier buen mago, podemos empezar con cada truco individual, construyendo la audiencia a medida que avanzamos, llevándolos al &quot;prestigio&quot; final. Aquí es donde realmente brillamos, tomando todos los pequeños trucos, y enrollarlos en un gran final. Tomando las partes aparentemente desconectadas del truco, y mostrando que de hecho, todas trabajan juntas para formar un todo cohesivo.

![Conejo_Fuego](assets/fire-bunny.jpeg)


### Ejemplo de segmento 6: Visitantes que han realizado un pedido durante una visita con una instancia social de pago y que excluyen a los visitantes que se han suscrito a cualquier newsletter

![Segmento6A-VisitantesComprandoDeSocialPagadoSinNewsletter](assets/segment-example-6/segment6a-visitors-purchasing-from-paid-social-with-no-newsletter.png)

Esto me permite identificar a los visitantes que han realizado una compra de forma activa durante una visita en una campaña de medios sociales, pero que no se han registrado en nuestros boletines informativos. Esto permitirá a nuestro equipo de marketing ver el grupo potencial de usuarios que deben intentar realizar la conversión para boletines informativos y correos electrónicos de marketing.

## Final

![Escenario_Teatro](assets/theater-stage.jpeg)

Hay tantas maneras de combinar la lógica para entrar en escenarios muy detallados, que solo puedo arañar la superficie de las posibilidades.

Como cualquier gran mago, el verdadero poder está en inspirar a la nueva y futura generación para construir sobre lo básico, para re-imaginar los aprendizajes en algo nuevo y maravilloso! ¡Espero con ansias ver lo que todos ustedes tienen!

## Autor

Este documento fue escrito por:

![Jen Headshot](assets/jen-headshot.png)

Jennifer Dungan, jefa de optimización de análisis en Torstar

Campeona de Adobe Analytics

