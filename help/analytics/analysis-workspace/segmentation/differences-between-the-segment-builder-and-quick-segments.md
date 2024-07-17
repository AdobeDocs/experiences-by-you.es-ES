---
title: Diferencias entre el generador de segmentos y los segmentos rápidos en Analysis Workspace
description: Los segmentos pueden ser una de las herramientas más potentes del conjunto de herramientas de análisis de datos. Aprenda las diferencias entre el uso del generador de segmentos y los segmentos rápidos en Analysis Workspace para lograr una mayor eficacia.
feature-set: Analytics
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
exl-id: baeaa90e-8cce-4ddd-b099-fecd266e410c
source-git-commit: 849ec510944d3299c3515fcecd5fc57d74c3fa26
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 0%

---

# Diferencias entre el generador de segmentos y los segmentos rápidos en Analysis Workspace

Los segmentos pueden ser una de las herramientas más potentes del conjunto de herramientas de análisis de datos. Aprenda las diferencias entre el uso del generador de segmentos y los segmentos rápidos en Analysis Workspace para lograr una mayor eficacia.

>[!TIP]
>
> Haga clic en la imagen en la parte inferior de la página para descargar un recordatorio útil sobre cuándo utilizar cada herramienta en Analysis Workspace.

Los segmentos pueden ser una de las herramientas más potentes del conjunto de herramientas de análisis de datos. Si desea observar grupos específicos de tráfico, secciones del sitio o recorridos de clientes, el uso de segmentos puede ser una buena manera de enfocar el análisis en un subconjunto particular de tráfico hacia el sitio. Al provenir de un entorno minorista, algunos de los segmentos más útiles que he creado son para diferentes tipos de grupos de clientes, por ejemplo, clientes nuevos frente a existentes, clientes que iniciaron sesión en una cuenta frente a invitados, etc. Pero también puede hacerlas para diferentes secciones del sitio, clientes que realizan acciones específicas o cualquier otra cosa que se le ocurra.

**Existen dos maneras principales de generar segmentos:**

* Uso del Generador de segmentos en el menú de componentes
* Uso de segmentos rápidos en la parte superior de un panel

Si genera el segmento con el Generador de segmentos, puede guardarlo para reutilizarlo en otros proyectos. Esta es una buena manera de poder centrarse en grupos específicos de clientes, por ejemplo, personas que visitan determinadas secciones del sitio y luego realizan una compra. Por otro lado, si está realizando un análisis exploratorio y desea probar diferentes configuraciones de segmentos, el generador de segmentos rápidos puede ser de gran ayuda. Veamos algunos de los principales beneficios de cada método.

## Segmentos rápidos

En la parte superior de cada panel, puede hacer clic en el icono de segmento rápido (un embudo con el símbolo + ) para abrir el generador. Esto le permitirá generar un segmento en cualquier nivel (visita individual, visita o visitante) con hasta tres condiciones. Similar al generador de segmentos principal, le proporciona una indicación en el lado derecho que indica si el segmento devuelve datos y el % de la población de tráfico general incluida en el segmento, aunque esta es una versión más simplificada que la vista de volumen de segmento completo que se muestra en el generador de segmentos. Al agregar más de una condición, puede utilizar los operadores &quot;and&quot; y &quot;or&quot;. Lamentablemente, no hay una opción &quot;then&quot; para segmentos rápidos, por lo que si necesita segmentos secuenciales deberá utilizar el generador de segmentos completo. También hay un límite de un contenedor en un segmento rápido. Ya que está pensado para utilizarse para segmentos básicos que se pueden crear y editar rápidamente. Una vez que se aplica un segmento rápido a un panel o se guarda, ya no se puede editar dentro del panel.

Cuando realice un análisis exploratorio y desee probar distintos tipos de segmentos para ver cómo reaccionan los distintos grupos de clientes o el rendimiento de las distintas categorías: el uso de segmentos rápidos es mucho más rápido que el uso del generador de segmentos. Además, estos segmentos solo están disponibles en el proyecto en el que se crearon, por lo que si no proporciona los resultados deseados, no es necesario preocuparse por eliminar el segmento guardado de la lista maestra. Si después de probar los segmentos se da cuenta de que va a ser útil en otros proyectos, siempre puede hacer clic en el botón &quot;Abrir generador&quot; para abrir el segmento en el generador de segmentos completo y guardarlo como un segmento normal. Sin embargo, una vez que lo haga, ya no podrá editarlo en el generador de segmentos rápidos.

![Segmento rápido](assets/quick-segement.png)

## Generador de segmentos

Se puede acceder al generador de segmentos haciendo clic en el símbolo + situado encima de la lista de segmentos en el menú de componentes de la izquierda, o haciendo clic en el menú desplegable de componentes y seleccionando &quot;Crear segmento...&quot;. A diferencia de los segmentos rápidos, tiene todas las opciones disponibles. Para agregar varias condiciones, puede crear segmentos secuenciales con el operador &quot;then&quot;. Los segmentos secuenciales también le permiten utilizar un &quot;grupo lógico&quot; como nivel (en lugar de visita individual, visita o visitante). El generador de segmentos también le permitirá agregar una descripción a los segmentos, lo que puede añadir contexto sobre quién creó el segmento o qué tipo de datos se creó para filtrar, o incluso simplemente añadir &quot;etiquetas&quot; al segmento con fines organizativos, lo que no es posible dentro del generador de segmentos rápidos.

El uso del generador de segmentos es esencial cuando el segmento va a tener más de 3 condiciones, si necesita utilizar contenedores o desea segmentos secuenciales. El generador de segmentos completo tiene muchas más opciones para crear segmentos más intrincados, lo que puede ayudarle a desglosar diferentes tipos de clientes, categorías, recorridos de clientes, etc. Una vez creados y guardados estos segmentos, se añaden a la lista maestra de segmentos, lo que significa que se pueden etiquetar, aprobar, compartir, utilizar en varios informes y publicar en el Experience Cloud. La publicación en el Experience Cloud le permite utilizar el segmento en otros [!DNL Adobe] productos, como en [!DNL Adobe] Target para la segmentación de personalización. Los segmentos creados en el Generador de segmentos no se pueden editar en el panel de segmentos rápidos, deberá abrir el Generador de segmentos para realizar cambios en ellos. Afortunadamente, la visualización de previsualización a la derecha proporciona un análisis más detallado del tráfico que el segmento traería en los últimos 90 días, lo que significa que es más fácil asegurarse de que el segmento trae lo que desea antes de guardar.

![Generador de segmentos](assets/segment-builder-quick.png)

## Casos de uso

En diferentes industrias, los usos para crear segmentos personalizados pueden diferir. Trabajando para la división de comercio electrónico de un gran minorista, a menudo realizamos análisis exploratorios para determinar qué rutas están tomando los clientes para comprar. Cuando vemos picos o caídas en acciones como añadir productos a los carros de compras o realizar pedidos, aquí es donde el uso de segmentos rápidos puede resultar útil. Durante un análisis, puedo crear rápidamente un segmento para un tipo específico de cliente o para una acción/vínculo en particular en el que hacen clic. Al no tener que abrir el generador de segmentos y guardar cada segmento, puedo agregar las condiciones rápidamente y luego eliminarlas igual de rápido. Esto ahorra mucho tiempo al intentar explicar por qué vemos un cambio en nuestro sitio.

Por otra parte, hay veces en que el generador de segmentos ha sido mi opción. No todos los clientes son iguales y, a menudo, queremos ver tipos específicos de clientes que se identifican por acciones o rutas que realizan. Con el generador de segmentos, podemos añadir varias condiciones para identificar los diferentes tipos de clientes y guardar los segmentos de modo que varios analistas puedan compartirlos y utilizarlos. Es importante que estos tipos de segmentos sean coherentes en todos los informes, por lo que disponer de uno generado que todos puedan usar es mejor que que cada persona que genere su propia versión, ya que los resultados pueden diferir.

En general, tanto los segmentos rápidos como el generador de segmentos son excelentes herramientas para utilizar en el análisis. Cada uno de ellos tiene sus propósitos, beneficios e inconvenientes. Asegúrese de consultar nuestra práctica hoja de consejos y trucos descargables a continuación para obtener una guía de referencia rápida.

## Autor

Este documento fue escrito por:

![Mandy George](assets/mandy-george-2.png)

**Mandy George**, analista digital III en Best Buy Canada

Campeona de Adobe Analytics

## Descargar

[![Descarga rápida de segmentos](assets/quick-segments-download-small.jpg)](recursos/[!DNL Adobe]_[!DNL Analytics]_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
