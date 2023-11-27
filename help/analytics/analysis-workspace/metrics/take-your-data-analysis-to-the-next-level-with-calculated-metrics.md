---
title: Lleve su análisis de datos al siguiente nivel con Métricas calculadas
description: Descubra cómo un experto del mismo nivel utiliza métricas calculadas para crear nuevas métricas sin cambiar su implementación y utilizando los datos ya recopilados para responder preguntas comerciales complejas.
feature-set: Analytics
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
exl-id: 301ee179-b154-4cf2-b27e-77f38a8945a0
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '1549'
ht-degree: 3%

---

# Lleve su análisis de datos al siguiente nivel con Métricas calculadas

La mayoría de los usuarios nuevos de [!DNL Adobe Analytics] Están familiarizados con los segmentos como una forma de cortar y fragmentar sus datos. Hoy, quiero presentarles las métricas calculadas, la siguiente mejor herramienta de su caja de herramientas de analistas.

Como característica avanzada de [!DNL Adobe Analytics], las métricas calculadas le permiten crear nuevas métricas sin cambiar la implementación con los datos que ya ha recopilado. El Creador de métricas calculadas puede utilizar muchas funciones matemáticas y estadísticas diferentes, de modo que puede crear métricas que respondan incluso a las preguntas comerciales más complejas.

## Introducción a las métricas calculadas

Para empezar a usar las métricas calculadas, veamos un ejemplo sencillo. Imagine que desea saber si los usuarios de autoservicio en línea tienen un valor de pedido promedio (AOV) mayor que los usuarios con asistencia por llamada. Para crear una métrica calculada que responda a esta pregunta, haga lo siguiente:

Para abrir el Creador de métricas calculadas, utilice la barra de navegación superior para hacer clic en → **Componentes** → **Métricas calculadas** → **+ Agregar.** O bien, puede hacer clic en **Signo +** superior **Métricas** en el panel Componentes.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Descripciones de los elementos de interfaz de usuario siguientes*

Una vez que se abra el Creador de métricas calculadas, agregue o haga lo siguiente:

**A.** Nombre de la métrica calculada. Este nombre se muestra en la lista de componentes de métricas, por lo que debe ser claro para usted y para los demás, como *Centro de llamadas AOV*.

**B.** Una descripción de la métrica calculada. Esta descripción aparece cuando los usuarios hacen clic en &#39;**i**&quot; junto a la métrica en la lista de componentes, por lo que debe asegurarse de que es informativa. Por ejemplo, para Call Center AOV, podríamos añadir *Calcula AOV para pedidos asistidos por centro de llamadas*.

**C.** El formato de la métrica: Elija decimal, tiempo, porcentaje o moneda, y añada lugares decimales y polaridad. Aquí, vamos a elegir *Divisa para el formato, 0 para el número de decimales y* ⬆ *Bueno (verde) para la polaridad.*

**D**. Si utiliza etiquetas, que le permiten aplicar temas y localizar rápidamente métricas calculadas, agregue las etiquetas que se apliquen aquí. Hemos añadido lo siguiente *AOV* y *Centro de llamadas* etiquetas.

**E.** Esta sección está destinada a su visualización: a medida que genere la métrica calculada en la sección F, la fórmula se mostrará aquí.

**F..** Aquí puede arrastrar y soltar dimensiones (H), métricas (I) o segmentos (J) para crear la métrica calculada y los operadores de la fórmula. Para cada métrica, si hace clic en la rueda dentada, puede cambiar el Tipo de métrica (Estándar/Total) y el Modelo de atribución. *Arrastraremos y soltaremos los ingresos del centro de llamadas, luego debajo de eso,*÷￼*. Aceptaremos el tipo de métrica y el modelo de atribución predeterminados.*

**G**. Use esto **+Agregar** opción para agregar condiciones adicionales o números estáticos, que no necesitamos aquí.

**K.** Y finalmente, a medida que construye su cálculo, puede obtener una vista previa de los datos de los últimos 90 días aquí.

Ahora que hemos creado el centro de llamadas AOV, también necesitamos una métrica calculada para AOV en línea. Lo haríamos siguiendo los mismos pasos descritos anteriormente.

A continuación, podemos crear una tercera métrica calculada, ya sea mediante el Creador de métricas calculadas o sobre la marcha desde la tabla de forma libre, para comparar el centro de llamadas y el AOV en línea, de modo que terminemos con algo similar a esto:

![Calc 05](assets/calc05.png)

En nuestro ejemplo, vemos un alza significativa cuando los compradores utilizan el centro de llamadas para ayudarles a realizar una compra. Estos datos pueden entonces informar nuestras decisiones sobre cómo ayudar a los clientes a obtener asistencia con sus compras a través, por ejemplo, de ofertas emergentes u otras experiencias guiadas.

## Uso de segmentos en métricas calculadas

Ahora, veamos cómo podemos usar segmentos en métricas calculadas para obtener más información sobre el comportamiento, las preferencias y las motivaciones de los clientes. Con los segmentos y las métricas calculadas, podemos aprender lo suficiente sobre los clientes para mejorar su experiencia, aumentar los ingresos y mejorar la satisfacción y lealtad de los clientes.

Ya sabemos, a partir de los ejemplos de AOV anteriores, que las compras asistidas por el centro de llamadas suelen tener un AOV más alto. Sin embargo, otras métricas indican que la mayoría de los usuarios no utiliza el centro de llamadas para realizar compras.

Entonces, ¿qué categorías minoristas (y rutas de usuario a través de esas categorías) resultan en el AOV más alto?  Podemos averiguarlo combinando segmentos con métricas calculadas.

Para ello, primero debemos crear el nivel de visita *include* y *excluir* segmentos para cada categoría de producto. Incluir o excluir se determina haciendo clic en **Opciones** engranaje en la esquina derecha del contenedor. El valor predeterminado es Incluir.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Una vez creados estos segmentos, podemos crear una métrica calculada para darle la respuesta a su pregunta. Abrimos el Generador de métricas calculadas y hacemos lo siguiente:

1. Busque los segmentos recién creados y arrastre y suelte los que desee utilizar en el área gris de la parte superior del **Definición** cuadro. Por ejemplo, si queremos crear una AOV para usuarios que visitaron las categorías femenina y masculina, pero no la infantil, podemos arrastrar y soltar estos tres segmentos en esa área: *Incluir ropa de mujer*, *Incluir de hombre*, y *Excluir del niño*. A esto le llamamos *apilar segmentos*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. A continuación, arrastramos y soltamos el **Ingresos en línea** en el mismo contenedor, **Pedidos en línea**. Dado que los contenedores funcionan como expresiones matemáticas para determinar el orden de las operaciones, los elementos de los contenedores se procesan antes que los procesos posteriores, aunque no tenemos varios contenedores o procesos en este cálculo.
1. Cambiamos el operador entre las dos métricas a división (÷).
1. Seleccionamos **Moneda** como formato, **0** decimales, y **ARRIBA** para la polaridad.
1. Asigne un nombre a la métrica calculada y proporcione una descripción.
1. Guardar.

Cuando hayamos terminado, la métrica calculada tendrá este aspecto:

![Calc 10](assets/calc10.png)

Después de crear métricas calculadas utilizando segmentos apilados para cada combinación de recorrido de categoría del visitante y echar un vistazo a los datos, ¡observe lo que aprendemos! Los usuarios que visitan las categorías femenina y masculina durante su visita tienen la mayor AOV y, en comparación con los visitantes de una sola categoría, el alza es significativa:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Sabiendo esto, podemos optimizar el diseño de la página, las ubicaciones de los productos y la mensajería promocional para que más personas entren en estas categorías antes de cerrar sesión.

## Útil, pero no disponible en todas partes

**Por lo tanto, las métricas calculadas, tanto simples como complejas, son muy valiosas para los analistas.**

Sin embargo, estas métricas no están disponibles en todas las áreas de [!DNL Adobe Analytics]. No se pueden usar las métricas calculadas en:

- Secuelas en Analysis Workspace
- Análisis de cohortes en Analysis Workspace
- Data Warehouse 
- Informes en tiempo real
- Informes de datos actuales
- [!DNL Analytics] para Target
- Report Builder

## Prácticas recomendadas para métricas calculadas

Ahora que sabe lo valiosas que pueden ser las métricas calculadas, veamos algunas prácticas recomendadas para crearlas.

1. **Compruebe la sintaxis de la fórmula.** Asegúrese de que la sintaxis de la fórmula sea correcta y siga el [!DNL Adobe Analytics] sintaxis para asegurarse de obtener información significativa.
1. **Compruebe el orden de las operaciones.** Asegúrese de utilizar los contenedores con cuidado y poner las cosas en el orden matemático adecuado de las operaciones.
1. **No cuente los datos dos veces**. Puede evitar el recuento doble de datos asegurándose de que la fórmula utilizada en la métrica calculada no cuente los mismos datos varias veces. Esto a menudo se logra combinando *Incluir* y *Excluir* condiciones en la métrica calculada o mediante el uso de segmentos.
1. **Compruebe la granularidad de tiempo.** Asegúrese de que la métrica calculada tiene la misma granularidad de tiempo que las métricas de origen utilizadas en la fórmula.
1. **Utilice datos precisos:** Solo obtendrá resultados valiosos si utiliza datos precisos y fiables en el cálculo.

## Prácticas recomendadas de segmentos personalizados

Al crear segmentos en [!DNL Adobe Analytics], tenga en cuenta estas prácticas recomendadas:

1. **Manténgalo simple.** Evite complicar en exceso el segmento. Sea lo más sencillo posible y utilice únicamente las condiciones necesarias para garantizar la precisión.
1. **Utilice los tipos de contenedores correctos**. Asegúrese de utilizar el tipo de contenedor correcto (visitante, visita o visita individual) en la definición del segmento para evitar obtener resultados incorrectos.
1. **No cuente los datos dos veces**. Al igual que con las métricas calculadas, asegúrese de que el segmento no cuente los mismos datos varias veces. Los contenedores Incluir y Excluir pueden ayudar.
   1. Cuando se utiliza un contenedor de inclusión, *incluye* *todo el contenido de la visita* si alguna visita individual coincide con la condición dentro de la visita.
   1. Cuando se utiliza un contenedor de exclusión, *excluye todo el contenido de la visita* si alguna visita individual coincide con la condición dentro de la visita.
1. **Anidar los contenedores correctamente**. Determine qué datos se incluyen utilizando el contenedor exterior y, a continuación, aplique reglas anidadas a los datos restantes. A medida que se aplican reglas anidadas, el flujo del segmento actúa como un canal y las reglas subsiguientes no se aplican a ninguna visita individual que haya sido excluida por la primera regla.
1. **Asegúrese de que los datos estén actualizados.** Asegúrese de utilizar datos precisos y actualizados en la definición del segmento para obtener resultados precisos.
1. **Pruebe el segmento.** Pruebe siempre el segmento para asegurarse de que funciona según lo previsto antes de lanzarlo a otros usuarios.
1. **Considere el rendimiento.** Los segmentos pueden ralentizar el procesamiento de los informes, por lo que tenga en cuenta ese impacto al crearlos.

## Principales conclusiones

Combinación de segmentos y métricas calculadas en [!DNL Adobe Analytics] puede llevar a un análisis de datos más robusto y efectivo. Al dividir y cortar en trozos los datos y crear cálculos para comparar, puede obtener perspectivas más profundas del comportamiento de los clientes que puede utilizar para optimizar sus campañas de marketing y crear paneles e informes personalizados. Sin embargo, recuerde que las métricas calculadas no están disponibles en todas las áreas de [!DNL Adobe Analytics]y asegúrese de seguir las prácticas recomendadas para asegurarse de que obtiene datos precisos y útiles.


## Autor

Este documento fue escrito por:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Senior [!DNL Adobe Analytics] Responsable en Adswerve

![Adswerve](assets/calc14.png)
