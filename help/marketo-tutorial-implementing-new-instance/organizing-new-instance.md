---
title: Organización de una nueva instancia y establecimiento de convenciones de nomenclatura
description: Aprenda a configurar una buena organización dentro de la instancia de Marketo Engage, lo que permite a los futuros especialistas en marketing de la organización navegar fácilmente por los programas, modificar los recursos y extraer informes.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-03T00:00:00Z
jira: KT-14813
thumbnail: KT-14813.jpeg
exl-id: 19b3de9e-53f3-4308-b46e-7b8f756c30a0
source-git-commit: e0d0c47eec98b7259363350d331ba69bbcaaa64b
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 2%

---

# Organización de una nueva instancia y establecimiento de convenciones de nomenclatura

Como administrador que implementa una nueva instancia de Marketo Engage, está sentando las bases para permitir que los futuros especialistas en marketing de la organización puedan navegar fácilmente por ella. Familiarizarse con la estructura de carpetas de árbol y las convenciones de nomenclatura mantendrá la instancia ordenada y configurada para tener éxito a largo plazo. Este tutorial incluye ejemplos recomendados por la campeona de Adobe y Marketo Engage (2019-2020), Natalie Kremer, para ayudarle a [organizar las carpetas y asignar nombres a los recursos de forma coherente](https://nation.marketo.com/t5/champion-program-blogs/keep-marketo-engage-organized-with-folders-and-naming/ba-p/245630){target="_blank"}.

## ¿Por qué es necesario estructurar carpetas y aplicar convenciones de nomenclatura?

Mantenerse organizado en la instancia facilita al usuario y a los compañeros el seguimiento de las campañas, los programas y los recursos, así como la creación de informes sobre el rendimiento del programa. Para organizar el árbol de navegación en su instancia y compilarlo a escala, se recomienda usar [carpetas](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/understanding-folders){target="_blank"}, [convenciones de nomenclatura estándar](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#naming-schemes){target="_blank"} y características como [clonación](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#cloning){target="_blank"}.

## Cómo organizar una instancia de Marketo Engage

>[!VIDEO](https://video.tv.adobe.com/v/3421577/?quality=12&learn=on)

### Paso 1: Configuración de una estructura de carpetas para ordenar los programas

El primer paso para organizar su instancia es [configurar una estructura de carpetas](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/create-new-campaign-folder.html) para alojar su programa y sus recursos de una manera fácil de encontrar y ordenada.

A continuación se ofrecen algunas sugerencias rápidas para estructurar las carpetas en árbol:

* Mantenga una estructura de carpetas plana para permitir la detección.
* Organice las carpetas para que reflejen la estructura de equipo de su organización (por ejemplo, Región o Equipo) o iniciativas (por ejemplo, Newsletters).
* Incluya etiquetas basadas en el tiempo para permitir la búsqueda y señalar el momento adecuado para el archivado (por ejemplo, 2024).
   * Se recomienda a los administradores que archiven las carpetas al menos una vez al año. Con un nombre de carpeta anual, puede desactivar fácilmente las campañas inteligentes en directo y archivar toda la carpeta al final del año.

A continuación se muestran ejemplos de carpetas de cómo poner en práctica estas sugerencias.

**Nombre de carpeta en árbol**

>[!BEGINTABS]

>[!TAB Actividades de marketing]

![Carpetas y actividades de mercadotecnia](/help/marketo-tutorial-implementing-new-instance/assets/folders-marketing-activities.png)

>[!TAB Estudio de diseño]

![Estudio de diseño de carpetas](/help/marketo-tutorial-implementing-new-instance/assets/folders-design-studio.png)

>[!TAB Database]

![Base de datos de carpetas](/help/marketo-tutorial-implementing-new-instance/assets/folders-database.png)

>[!ENDTABS]

### Paso 2: Creación de carpetas dentro de los programas

Ahora, vamos a aplicar la estructura de carpetas en el nivel de programa. Como práctica recomendada, alojar los recursos locales en subcarpetas le ayudará a mantener los programas ordenados y permitirá a los usuarios internos modificar o informar sobre los programas de forma eficaz. Las subcarpetas comunes incluyen correos electrónicos, páginas de aterrizaje, campañas inteligentes, listas, informes, etc.

**Nombre de carpeta dentro de programas**
* Campañas: *Carpeta para todas las campañas que administran interacciones y seguimiento de estado.*
* Assets local: *Carpeta para todos los recursos específicos de este programa.*
   * Correos electrónicos
   * Páginas de destino
   * Campañas inteligentes
   * Listas: *Solo se necesitan cuando hay listas específicas del programa.*
   * Forms - *Solo se necesita cuando hay Forms específicos del programa; la mayoría de Forms son Assets globales.*
   * Informes - *Solo se necesitan cuando hay informes específicos del programa.*

### Paso 3: Creación de convenciones de nomenclatura para sus programas y recursos

Una vez que tenga la estructura de carpetas en el árbol, querrá asignar nombres a los programas y recursos de forma coherente. Este es el momento en el que la estandarización de las convenciones de nomenclatura resultaría útil para ampliar el proceso de nomenclatura internamente. Estos son algunos componentes que puede utilizar para establecer una convención de nombres para garantizar la capacidad de búsqueda:

* Abreviatura del tipo de programa: correo electrónico, contenido, nutrición, seminario web, etc.
* Categoría: tipo de programa: correo electrónico, newsletter, etc. independientes.
* Fechas: fecha de inicio del programa
* Breve descripción: breve descripción del programa

Ahora, vamos a colocar los valores en la fórmula y generar los nombres de los programas para varios tipos de programas.

#### Fórmula de nomenclatura de programas

| **Abreviatura del tipo de programa** | **AAAA** | **\-** | **MM** | **\-** | **DD(Opcional)** | **Categoría** | **\-** | **Descripción breve del programa** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EM: envío de correo electrónico (programa de correo electrónico) | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| NL - Newsletter | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| ENG - Programa de participación | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| WBN: seminario web | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| IW: seminario web interactivo | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| TS - Feria | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| LE - Evento en directo (Roadshow) | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| UG - Grupo de usuarios | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| WC - Contenido del sitio web | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| CS: distribución de contenido | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| LI - Importación de lista | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| OA - Advertising en línea | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |
| PPC - Pago por clic | AAAA | \- | MM | \- | DD (opcional) | Categoría | \- | Breve descripción del programa |

| **Ejemplos** |
| --- |
| Contenido cerrado ES 2023-10: documento técnico de XYX |
| WC-2023-10- Seminario web mensual - ABC Caso práctico |

#### Fórmula de nomenclatura de recursos

Un nivel por debajo de la asignación de nombres a los recursos, es mejor que no repita el nombre del programa y utilice identificadores cortos y genéricos para usos futuros de clonación. A continuación se ofrecen algunos consejos rápidos a tener en cuenta:

* Numerar los recursos en función de su secuencia en el proceso del programa.
* Utilice &quot;-&quot; (guión) para separar los componentes de nomenclatura en lugar de &quot;&quot;.(punto) o &quot;\_&quot;(guion bajo).
   * ¿Por qué? El Marketo Engage utiliza un punto para separar el Nombre del programa del Nombre de la campaña. Usar &quot;\_&quot; evitará que lo vea cuando el recurso tenga un hipervínculo.
* Utilice acrónimos estándar en los nombres de los recursos para acortar la referencia y facilitar el reconocimiento.

Teniendo en cuenta esto, aplicaremos estas sugerencias a los siguientes recursos y crearemos fórmulas para generar nombres:

##### Asignar un nombre a los recursos en función de la secuencia del proceso del programa

| **Secuencia en el proceso del programa** | **\-** | **Descripción** |
| --- | --- | --- |
| 01 | \- | Descripción |
| 02 | \- | Descripción |
| 03 | \- | Descripción |

| **Ejemplos: Smart List** |
| --- |
| 01-Enviar correo electrónico |
| 02-Abierto |
| Con 3 clics |
| Formulario rellenado en 04 |
| Influenciado por 05 (éxito del programa) |
| 06 - Cancelación de la suscripción |

##### Asigne un nombre a los recursos con la abreviatura de tipo de recurso

| **Abreviatura del tipo de recurso** | **Tipo de recurso** | **\-** | **Descripción de la meta** |
| --- | --- | --- | --- |
| LP - Página de aterrizaje | LP | \- | Descripción de la meta |
| CORREO ELECTRÓNICO: correo electrónico (saliente) | EMAIL | \- | Descripción de la meta |
| ALERT - Alerta por correo electrónico | ALERTA | \- | Descripción de la meta |
| WF: formulario web | WF | \- | Descripción de la meta |
| EXCL - Lista de exclusión | EXCL | \- | Descripción de la meta |
| SLST: lista inteligente | SLST | \- | Descripción de la meta |
| LISTA - Lista estática | LISTA | \- | Descripción de la meta |

| **Ejemplos** |
| --- |
| LP-Registro |
| LP-Gracias |
| EMAIL-Outbound |
| CORREO ELECTRÓNICO-Newsletter |
| EMAIL-Invitation |
| EMAIL-Reminder |
| EXCL-Competitors |

##### Asigne un nombre a los archivos descargables (.pdf) con la abreviatura de tipo de recurso

| **Tipo de recurso** | **Descripción del contenido** | **\-** | **Abreviatura del tipo de recurso** | **.** | **PDF** |
| --- | --- | --- | --- | --- | --- |
| WP - Libro blanco | Descripción del contenido | \- | WP | . | pdf |
| CS: Caso práctico | Descripción del contenido | \- | CS | . | pdf |
| DS: hoja de datos | Descripción del contenido | \- | DS | . | pdf |

| **Ejemplos: Archivos de PDF descargables** |
| --- |
| XYZ-Gadget-DS.pdf |
| Acme-Company-CS.pdf |
| How-XYZ-Gadgets-make-life-easier-WP.pdf |

>[!CAUTION]
>
>Al asignar nombres a los archivos en los ejemplos anteriores, no utilice espacios y evite el uso de guiones bajos &quot;\_&quot;

## ¿Qué sigue?

* Descargue la hoja de cálculo: [Convenciones de nomenclatura y organización de Marketo Engage](./assets/adobe-marketo-engage-organization-and-naming-conventions.xlsx){target="_blank"} para admitir la creación de la estructura de carpetas y las convenciones de nomenclatura.
* Una vez que haya determinado los componentes necesarios en la convención de nombres estándar, considere la posibilidad de crear fórmulas en una hoja de Google o en Microsoft Excel. Para su uso futuro, simplemente introduzca los valores en la hoja de cálculo para generar los nombres de los programas.
* Una vez que se alinee en una estructura de carpetas general, es hora de pensar en las plantillas que necesita en función de los casos de uso más frecuentes y las solicitudes más comunes que recibe su equipo. A continuación, empiece a crear la primera plantilla de programa. Siga leyendo para empezar a usar [plantillas de programa de Adobe Marketo Engage](https://business.adobe.com/blog/how-to/get-started-with-marketo-engage-program-templates){target="_blank"}.

### Autores

{{natalie-kremer}}

{{amy-chiu}}
