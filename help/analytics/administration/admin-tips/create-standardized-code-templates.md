---
title: Creación de plantillas de código estandarizadas
description: Para una implementación de línea de base (es decir, lo que su empresa considera como los KPI que debe tener para todos los  [!DNL Adobe Analytics] sitios), su organización debe tener un único método de implementación, siempre que sea posible.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: edd3df73-6d1a-4a26-a984-810cc7dd382f
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Creación de plantillas de código estandarizadas

**QUÉ:** Para una implementación de &quot;línea de base&quot; (es decir, lo que su compañía considera como los KPI que debe tener para todos los sitios de [!DNL Adobe Analytics]), su organización debe tener un único método de implementación, siempre que sea posible. Por ejemplo, utilice la misma estructura de capa de datos en todos los sitios y aproveche la misma regla/código personalizado de administrador de etiquetas para capturar cosas como búsquedas internas o información del perfil del visitante.

**POR QUÉ:** Tener una implementación de línea de base repetible y escalable hace que agregar nuevos elementos o nuevos sitios/aplicaciones sea un esfuerzo racionalizado y de bajo esfuerzo, al mismo tiempo que mantiene la implementación limpia y hace que sea fácil solucionar problemas. El uso de un método uniforme también facilita que los nuevos administradores/desarrolladores se conecten y entiendan con qué están trabajando.

**CÓMO:** Adopte una plantilla de formato único para entregársela a los desarrolladores cuando se publique un nuevo sitio o una mejora del etiquetado. Normalmente, funciona bien un documento de texto, en el que se pueden esbozar los siguientes elementos:

* Variables que se están implementando, su propósito y cuándo se van a configurar. Por ejemplo:

| Variable de AA | Descripción | Cuándo/dónde se establece | Cómo se establece |
|--- |--- |--- |--- |
| EVAR 8 | Palabras clave de búsqueda interna | Al aterrizar en la página de resultados de búsqueda interna | capa de datos |
| event8 | Recuento de búsquedas internas | Al aterrizar en la página de resultados de búsqueda interna | Regla de Launch |

* Detalles sobre cómo se establece. Aquí es donde especificaría los objetos de capa de datos necesarios y su sintaxis, así como las reglas del sistema de administración de etiquetas que se deban configurar y los detalles de la configuración de reglas.
* Los casos de prueba para asegurarse se cubren en el control de calidad y todas las variables que espera ver en un caso de prueba exitoso. Describa qué debe incluir una implementación correcta cuando el desarrollador pruebe esta mejora.

Lo ideal es que este documento solo necesite retocarse para el siguiente sitio donde actualice los conceptos básicos, como nombre de propiedad, convención de nomenclatura de páginas, etc. No es necesario reinventar la rueda cada vez, y puede ahorrar más tiempo.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataforma digital [!DNL Analytics] en NortonLifeLock
[!DNL Adobe Analytics] campeón

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en [!DNL Adobe]
