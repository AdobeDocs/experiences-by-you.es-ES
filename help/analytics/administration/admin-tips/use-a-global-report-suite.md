---
title: Uso de un grupo de informes globales
description: Tener un único grupo de informes globales puede ayudar de muchas maneras y simplificar de verdad la implementación.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
exl-id: f133d049-9a24-4153-88c5-40ec480d1e4e
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Uso de un grupo de informes globales

**QUÉ:** Es tentador crear grupos de informes para cada uno de sus sitios, pero esto puede convertirse rápidamente en su peor pesadilla, tanto en términos de complicar los informes como de la implementación. Tener un único grupo de informes globales puede ayudar de muchas maneras y simplificar de verdad la implementación.

**POR QUÉ:** La creación de un grupo de informes globales es la única opción para tener una vista unificada de las propiedades digitales y los recorridos de los usuarios en cada propiedad. Si tiene una aplicación móvil y un sitio web, siempre debe combinar los datos de la aplicación y los datos web en un grupo de informes para aprovechar los recorridos entre dispositivos y rastrear a quienes visitan ambas propiedades como un único visitante, en lugar de con grupos de informes separados, donde tendría un conjunto de datos desenlazados que mostraría 2 visitantes (1 de cada propiedad), sin forma de conocer el cruce.

Estas son las ventajas y desventajas de tener un único grupo de informes para ayudarle a sopesar las opciones:

* PROS:
   * Poder entender todo su panorama digital fácilmente. Si ha implementado la dimensión &quot;propiedades&quot; (eVar) a la que se hace referencia en otras sugerencias, podrá obtener con facilidad una sola vista de todos sus sitios y aplicaciones, tráfico y conversiones. Ver este panorama general es clave para comprender su negocio en general.
   * En el mismo sentido, ahora puede ver cómo fluyen los usuarios entre todas las propiedades y comprender su recorrido en todo el panorama digital.
   * Facilidad de administración. Cuando utilice varios grupos de informes, deberá mantener la interfaz en varios lugares, así como varios documentos de etiquetado (o uno más complicado). Mantener todo en un solo lugar significa que solo hay un lugar donde hacer actualizaciones. También facilita mucho la concesión de acceso.
   * Mejor facilidad de uso de la interfaz. Si los usuarios solo tienen un lugar al que ir, no necesitan pensar qué grupo de informes seleccionar. Tenga en cuenta que no puede utilizar varios grupos de informes en el mismo panel del espacio de trabajo y que, si hay varios, puede confundir a los usuarios.
   * Menos llamadas al servidor = menos costes. Si realiza llamadas a varios grupos de informes, aumenta los costes. Si la implementación es sencilla, también se reducirán los costes.
   * Puede, simplemente, aprovechar los grupos de informes virtuales (VRS) para dividir los datos específicos del sitio en el grupo de informes globales y reducir los permisos de usuario basados en un VRS si es necesario. Una vez que los datos se separan en grupos de informes individuales, no se pueden resumir, pero si ya se han unido en un conjunto de datos (RS global), se pueden desglosar fácilmente.
* CONTRAS:
   * Si tiene propiedades muy separadas y los usuarios no pasan de una a otra ni se espera que lo hagan, es posible que desee mantener grupos de informes separados.
   * Si las propiedades tienen necesidades de etiquetado y creación de informes muy diferentes, puede ser recomendable configurar grupos de informes separados en aras de la eficiencia de las variables. Tener grupos de informes separados le dará más flexibilidad para usar variables personalizadas (más eVars).
   * Excesos en la cantidad de valores exclusivos: la interfaz [!DNL Adobe Analytics] solo le permite ver 500 000 valores únicos dentro de una sola dimensión durante un período de tiempo determinado. Una vez superada esta cifra, los valores se agrupan como &quot;excesos en la cantidad de valores exclusivos&quot; o &quot;bajo tráfico&quot; en la interfaz. Estos valores permanecen disponibles en el servidor (es decir, la Data Warehouse y las fuentes de datos), pero no se pueden visualizar en la interfaz. Si tiene datos muy granulares (como ID de usuario, PSN, etc.), es fácil alcanzar este nivel. Tener grupos de informes separados puede ayudar con este problema.

**CÓMO:** Comenzar con una nueva implementación de AA y usar un grupo de informes globales es sencillo y directo. Solo necesita crear el grupo de informes globales (uno para Desarrollo y otro para Producción) en la IU de administración de AA y aplicar los mismos valores de ID del grupo de informes (RSID) en todas sus propiedades.

La migración desde una estrategia de etiquetado múltiple con un grupo de informes único por propiedad requiere más estrategia y planificación. Algunas de las consideraciones que debe tener en cuenta:

* Alinee las variables (es decir, el eVar 1 en la Propiedad A debe capturar el mismo punto de datos que el eVar 1 en la Propiedad B)
* Consolidar cualquier regla de procesamiento, regla de canal de marketing o clasificación (SAINT y Generador de reglas).
* Migración de fuentes de datos
* Elija una fecha de corte y comuníquela a todos los usuarios empresariales

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataforma digital [!DNL Analytics] en NortonLifeLock
[!DNL Adobe Analytics] campeón

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en [!DNL Adobe]
