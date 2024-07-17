---
title: Creación de modelos de puntuación de persona para programas de Marketo Engage
description: Adobe Marketo Engage le permite crear sus modelos de puntuación desde cero. Antes de saltar directamente a Marketo Engage para crear sus programas de puntuación, tendrá que configurar los campos de puntuación esenciales, como Puntuación demográfica, Puntuación conductual y Puntuación total de la persona. Obtenga más información sobre las estrategias que utilizan los Campeones Marketo Engage para desarrollar modelos de puntuación que satisfagan las necesidades de su empresa.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00Z
jira: KT-14810
thumbnail: KT-14810.jpeg
exl-id: 73976144-f02b-4423-9b4b-410330117ba9
source-git-commit: e0d0c47eec98b7259363350d331ba69bbcaaa64b
workflow-type: tm+mt
source-wordcount: '2111'
ht-degree: 2%

---

# Creación de un modelo de puntuación de persona

La puntuación de personas le ayuda a identificar a las personas que más se relacionan con su empresa y que son su perfil de cliente ideal, de modo que pueda compartir estos posibles clientes con su equipo de ventas y cerrar acuerdos. Junto con las ventas, puede determinar qué posibles clientes desea entregarles mediante un programa de puntuación de posible cliente/persona en Adobe Marketo Engage. Esto puede determinarse mediante una puntuación mínima de comportamiento, una puntuación demográfica o ambas.

En este tutorial, le guiaremos a través de tres ejercicios sugeridos por las campeonas Marketo Engage Christina Zuniga y Katja Keesom. Continúe para determinar qué actividades y características son indicadores importantes que un cliente potencial está interesado en comprar (puntuación de comportamiento) y es el adecuado para usted (puntuación demográfica), y tenga en cuenta los matices en todos los mercados.

## ¿Por qué desarrollar y utilizar un modelo de puntuación de persona?

Es posible que tenga muchos posibles clientes en su base de datos, pero ¿cómo sabe cuáles están listos para comprar sus productos y servicios ahora? A medida que su organización de marketing busca optimizar la calidad del posible cliente y la preparación para las ventas, aquí es donde entra en juego el modelo de puntuación.

Al puntuar a las personas en la base de datos de Marketo Engage, puede medir la cualificación de los posibles clientes generados y establecer criterios para cuándo están listos para realizar ventas. Esto permite a su equipo de ventas centrarse en los posibles clientes que es más probable que cierren mientras que el equipo de marketing sigue nutriendo a las demás personas de la base de datos a través de sus programas de marketing.

## Ejercicio 1: Determinación del interés del comprador con puntuaciones de comportamiento

La puntuación de comportamiento proporciona un valor numérico a las acciones rastreables que realiza un cliente potencial que indican interés en sus productos y servicios e intención de comprar. Por ejemplo, visitar el sitio web muestra interés y visitar la página de precios puede mostrar intención. Por el contrario, visitar la página Empleo puede indicar que la persona no va a realizar ninguna compra.

**Paso 1**: haga una lista de las actividades de clientes potenciales que importan a su proceso de ventas o que son valiosas para su organización. Puede resultar útil trabajar con su equipo de ventas para determinar qué actividades indican que un posible cliente tiene la intención de comprar, lo que le ayuda a alinear los criterios con las ventas y a priorizar en función de sus observaciones de ofertas cerradas. Estas son algunas de las preguntas sugeridas que puede hacer a su equipo de ventas:

* ¿Qué actividades indican una ventaja buena o mala para usted?
* ¿Qué tipo de contenido consumido por un posible cliente tiene una intención de compra más sólida?

**Paso 2**: enumere las acciones que indican que un cliente potencial no está interesado en su producto. Asegúrese de enumerar las actividades de las que se puede realizar un seguimiento mediante Marketo Engage.

**Ejemplo 1a - Actividades que indican intención de compra**

| **Actividades que indican intención de compra** | **Actividades que indican que NO hay intención de comprar** |
| --- | --- |
| Página de precios de visita | Sin interacción en los últimos 90 días |
| Asistir al evento anual de clientes | Visite la página Empleo |
| Registrarse en el seminario web | Cancelaciones de la suscripción |
| Descargar documento técnico |     |
| Rellene el formulario de solicitud de demostración |     |

**Paso 3**: Analice y elija una puntuación de umbral de transferencia de ventas.

* Una vez que un posible cliente indica suficiente interés realizando algunas de las actividades definidas en el paso 1 y la puntuación total supera este umbral, las entregará a las ventas. Este umbral simplemente será un número que le ayudará a establecer una referencia para las puntuaciones que asigne a comportamientos individuales.
* El número de umbral debe ser lo suficientemente grande como para que una persona necesite completar varias interacciones con su marca para cumplirlo. Por ejemplo, es poco probable que un correo electrónico abierto sea un calificador suficiente. Si acaba de empezar, intente trabajar con un umbral de 100 y crear la puntuación de su persona a partir de ahí.
* La configuración de un umbral alto o bajo depende de qué posibles clientes estén más interesados en recibir y convertirse en oportunidades comerciales. Si tiene datos sobre sus ofertas de ventas recientes, analícelos y vea qué acciones realizaron las personas en las ofertas exitosas. Esto puede ayudarle a determinar cuántos puntos de contacto entran en un posible cliente cualificado y le ayuda a extrapolar a partir de ahí cuál debe ser su número de umbral.

**Ejemplo 1b - Umbral de transferencia de ventas:**

| Cantidad promedio de puntos de contacto para posible cliente cualificado | 4 |
| --- | --- |
| Umbral de traspaso de ventas | 50 |

**Paso 4** - Asigne una puntuación a cada actividad enumerada en &#39;Ejemplo 1a - Actividades que indican intención de compra&#39;.

* Utilice una puntuación de comportamiento positiva para las actividades que indican interés para aumentar la puntuación general del posible cliente y una puntuación negativa para indicar desinterés.
* Utilizando el umbral de &quot;Ejemplo 1b - Umbral de traspaso de ventas&quot; como referencia, determine las puntuaciones de comportamiento en relación con la importancia de sus acciones. Por ejemplo, los posibles clientes que soliciten una demostración deben ir directamente a Ventas. Asignar a esa acción un valor de punto igual al umbral de transferencia de clientes potenciales tendrá más sentido. Mientras tanto, descargar un libro blanco no es un indicador tan fuerte de interés de compra y por lo tanto debería valer menos puntos.

**Ejemplo 1c - Actividades de puntuación que indican intención de compra:**

| Umbral de traspaso de ventas = 50 puntos |     |
| --- | --- |
| Actividad | Puntuación |
| Rellenado &quot;solicitar un formulario de demostración&quot; | +50 |
| Sin interacción en los últimos 90 días | \-10 |
| Descargar un documento técnico | +5 |
| Visítenos en una feria comercial | +15 |

**Paso 5**: Recuerde que la puntuación es un proceso iterativo. Revise y ajuste continuamente las puntuaciones y los umbrales a medida que recopila más datos para su análisis.

## Ejercicio 2: Identificación del ajuste perfecto con las puntuaciones demográficas

Ahora que ha definido las actividades que indican intención de compra, debe completar el modelo de puntuación con los Perfiles del cliente potencial ideal. Para identificar si un cliente potencial es el adecuado para continuar la conversación de ventas, es importante asignar puntuaciones demográficas además de puntuaciones de comportamiento para que el modelo ayude a determinar los mejores posibles clientes en términos de ajuste e intención.

**Paso 1**: haga una lista de características para sus posibles clientes ideales.

* Considere la posibilidad de enumerar atributos como el sector, la compañía, el departamento y la función. Asegúrese de que estas características correspondan a los campos demográficos disponibles en la instancia de Marketo Engage.
* Trabaje con su equipo de ventas para determinar qué posibles clientes responden mejor a las consultas de ventas y cuáles son los contactos clave durante las oportunidades de ventas.
   * Puede resultar útil analizar las oportunidades ganadas cerradas recientes para ver qué características tienen sus mejores clientes. Por ejemplo,
      * Explorar las oportunidades perdidas cerradas para patrones puede llevarte a encontrar datos demográficos que deseas evitar.
      * Identifique a los responsables de la toma de decisiones y a los líderes internos que impulsan los esfuerzos de venta. Sumérjase en los datos y lleve sus conclusiones a un taller con algunos de sus equipos de ventas para validar o perfeccionar sus conclusiones.
   * También puede entrevistar a su equipo de ventas con las siguientes preguntas de ejemplo:
      * ¿En qué departamento suelen participar?
      * ¿Cuáles son los cargos de las personas que participan en las demostraciones de productos y quiénes son las personas que deben firmar la compra?

**Ejemplo 2a - Características ideales del cliente potencial**

| **Categoría** | **Características del cliente potencial ideal** |
| --- | --- |
| Sector | Aeroespacial, Fabricación |
| Tamaño de empresa | 100 - 999, 1.000 - 9.999 |
| Cargo | Director, vicepresidente, nivel C |
| Departamento | HR |

**Paso 2**: asigne una puntuación a cada característica según su relevancia en el perfil de cliente potencial ideal. Utilice puntuaciones positivas para rasgos deseables y negativas para rasgos que hacen que el posible cliente sea menos adecuado para su producto.

**Ejemplo 2b - Asignar puntuaciones a características de cliente potencial ideales e indeseables**

| **Característica** | **Puntuación** |
| --- | --- |
| Industria - Aeroespacial | +10 |
| Industria - Fabricación | +5 |
| Tamaño de la empresa - 100 - 999 | +5 |
| Tamaño de la empresa - 1.000 - 9.999 | +10 |
| Tamaño de la empresa - &lt;10 | \-10 |

## Ejercicio 3: Incorporar la flexibilidad local en el modelo de puntuación

Con los modelos básicos de puntuación demográfica y de comportamiento que ha completado, puede llevarlo al siguiente nivel, lo que permite la flexibilidad local. Los valores empresariales pueden variar en distintos mercados cuando una organización opera a nivel global. En el siguiente ejercicio, aprenderá a aplicar puntuaciones para reflejar el valor comercial real de las actividades o características de los posibles clientes en diferentes situaciones.

¿Prefiere una guía en vídeo para este ejercicio? La campeona Marketo Engage Katja Keesom muestra cómo incorporar la flexibilidad local en el modelo de puntuación.

>[!VIDEO](https://video.tv.adobe.com/v/3426914/?learn=on)

**Paso 1**: tome las actividades y características de los ejercicios 1 y 2 y determine para cada elemento si varían según la ubicación o la línea de productos.

**Ejemplo 3a - Señales en mercados globales y locales:**

| **Señal** | **Global** | **Local** |
| --- | --- | --- |
| Actividades | <ul><li>Rellenado el formulario &quot;Solicitar demostración&quot;</li><li>No hubo interacción en los últimos 90 días (alrededor de 3 meses)</li></ul> | <ul><li>Visítenos en la feria</li><li>Descargar un documento técnico</li></ul> |
| Características | <ul><li>Departamento</li><li>Cargo</li></ul> | <ul><li>Sector</li><li>Tamaño de empresa</li></ul> |

**Paso 2**: Defina su matriz de puntuación para los mercados locales:

* Configure una matriz diferente para los elementos demográficos y de comportamiento.
* Determine los temas prioritarios en los que puede solicitar la opinión del equipo local.
* Defina el número de valores que se utilizarán para clasificar dentro de los temas.
* Asigne valores individuales alineando el valor relativo con las puntuaciones globales.
* Considere la posibilidad de definir escenarios comunes cuando los posibles clientes interactúen con su marca y pruebe su puntuación general para ellos.
   * Por ejemplo, un recorrido de cliente potencial común que usted ve sería que una persona entre a su sitio web en una página de contenido, luego haga clic hasta una página de producto y descargue un folleto. Puede dirigirse a ellos con una invitación al seminario web y estos responden registrándose, pero no asistiendo. Considere si sus ventas ya quieren hablar con esta persona o no y evalúe si su modelo de puntuación lleva a estos clientes potenciales a la puntuación general correcta para reflejar ese nivel de interés.

**Ejemplo 3b - Matriz de puntuación demográfica:**

| **Matriz demográfica** | **Prioridad 1** | **Prioridad 2** | **Prioridad 3** |
| --- | --- | --- | --- |
| Valores altos | 20 puntos | 10 puntos | 7 puntos |
| Valores de Medium | 10 puntos | 7 puntos | 3 puntos |
| Valores bajos | 5 puntos | 3 puntos | 1 punto |

**Paso 3**: recopile información de sus equipos de ventas locales o regionales para desarrollar una vista integral. Observará que en el ejemplo 3c no se incluyen puntuaciones individuales. Esto permite al equipo de ventas centrarse en el valor relativo de los diferentes temas durante el proceso de revisión. Sin embargo, debería tener el modelo completo documentado como material de fondo para otros administradores de Marketo Engage.

* Bloquee lo que no se pueda ajustar para la coherencia global (aquí en la columna &quot;Implementar tema&quot;).
* Marque (aquí en las columnas &quot;Prioridad&quot; y &quot;Puntuación&quot;) lo que se puede ajustar para las influencias locales.

**Ejemplo 3c - Valor relativo de los temas de puntuación:**

<table>
 <tr>
    <th>#</th>
    <th>Implementar tema</th>
    <th>Demográfico/Conductual</th>
    <th>Tema</th>
    <th>Prioridad</th>
    <th>Valores</th>
    <th>Puntuaciones</th>
 </tr>
 <tr>
    <td rowspan="6">1</td>
    <td rowspan="6"><b>OBLIGATORIO</b></td>
    <td rowspan="6">Demográfico</td>
    <td rowspan="6">Sector</td>
    <td rowspan="6"><b>2</b></td>
    <td>Tecnología</td>
    <td><b>Alto</b></td>
  </tr>
  <tr>
    <td>Moda</td>
    <td><b>Alto</b></td>
  </tr>
  <tr>
    <td>Comercial</td>
    <td><b>Medio</b></td>
  </tr>  
  <tr>
    <td>Fabricación</td>
    <td><b>Medio</b></td>
  </tr>
  <tr>
    <td>Asistencia sanitaria</td>
    <td><b>Bajo</b></td>
  </tr>
  <tr>
    <td>...</td>
    <td><b>Bajo</b></td>
  </tr>
<tr>
    <td rowspan="3">2</td>
    <td rowspan="3"><b>Sí</td>
    <td rowspan="3">Demográfico</td>
    <td rowspan="3">Tamaño de la empresa (empleados)</td>
    <td rowspan="3"><b>3</td>
    <td>&gt;1000 empleados</td>
    <td><b>Alto</td>
  </tr>
  <tr>
    <td>250 a 999 empleados</td>
    <td><b>Medio</td>
  </tr>
  <tr>
    <td>1-249 empleados</td>
    <td><b>Bajo</td>
  </tr>  
<tr>
    <td rowspan="3">3</td>
    <td rowspan="3"><b>No</b></td>
    <td rowspan="3">Comportamiento</td>
    <td rowspan="3">Visitas a la página en el sitio web</td>
    <td rowspan="3"><b>2</b></td>
    <td>&gt;Páginas de información del producto</td>
    <td><b>Bajo</b></td>
  </tr>
  <tr>
    <td>Páginas de precios</td>
    <td><b>Medio</b></td>
  </tr>
  <tr>
    <td>Página de solicitud de demostración</td>
    <td><b>Alto</b></td>
  </tr>
</table>

## ¿Qué sigue?

* Descargue la [hoja de ejercicios de puntuación de persona](./assets/build-person-scoring-model-and-local-flexibility-in-adobe-marketo-engage.docx){target="_blank} para desarrollar su modelo de puntuación sin conexión.
* Genere la puntuación de su persona en Marketo Engage. Consulte este [tutorial](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-watch){target="_blank} y [demostración](https://experienceleague.adobe.com/en/docs/events/marketo-and-mochas-recordings/2023/lead-scoring){target="_blank} para comenzar. Puede importar un programa de puntuación de posible cliente/persona [template](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/import-a-program){target="_blank} desde la Biblioteca de referencia de Marketo Engage para acelerar la compilación del programa.
* Cree dos versiones del programa de puntuación:
   * Un programa central que ejecuta todas las puntuaciones que no se pueden actualizar localmente.
   * Una copia local con los elementos de puntuación que se pueden configurar.
* Configure los valores de puntuación como tokens dentro del programa de puntuación. Esto garantiza la coherencia incluso cuando se ajustan las puntuaciones a lo largo del tiempo.
   * Un ejemplo común de puntuaciones tokenizadas es tener un token para actividades de alto valor que cumplen automáticamente con su umbral, como solicitar una demostración o reservar una reunión con su equipo de ventas. Incluso si modifica la puntuación mínima necesaria para alcanzar su umbral, puede actualizar fácilmente todas las actividades de alto valor a la vez actualizando un token.
* Ajuste la campaña inteligente local para cada ubicación:
   * Determine qué actividades demográficas y de comportamiento deben puntuarse solo una vez (es decir, industria) y cuál debe puntuarse cada vez que un posible cliente califica (es decir, asistió a un seminario web). Esto garantiza que los contactos potenciales activados por el cambio de valor de los datos sean relevantes para las ventas.
   * Asegúrese de que sus opciones sean mutuamente excluyentes.
   * Realice las actualizaciones en ambos pasos del flujo para que la puntuación de la persona se actualice de forma idéntica a la puntuación demográfica. De este modo, la puntuación de la persona se mantiene en línea con la combinación de puntuación de comportamiento y puntuación demográfica.
* Pruebe la campaña inteligente una vez que haya terminado de crear el programa. Por ejemplo, ve al formulario de demostración, rellénalo con un correo electrónico de prueba y comprueba la puntuación de la persona de prueba en [base de datos de Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started-with-marketo/quick-wins/simple-scoring#step-view-the-person-info){target="_blank}.
* Después de crear el modelo, considere la posibilidad de configurar una alerta para que salga a ventas una vez que la puntuación de la persona haya alcanzado el umbral de transferencia de ventas. Más información sobre cómo configurar una alerta con este [tutorial](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/send-alert){target="_blank}.

### Autores

{{christina-zuniga}}

{{katja-keesom}}

{{amy-chiu}}
