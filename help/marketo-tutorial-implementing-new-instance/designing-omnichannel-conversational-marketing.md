---
title: Diseño de marketing conversacional omnicanal con Dynamic Chat
description: Comience rápidamente a diseñar marketing conversacional con Adobe Dynamic Chat, el canal nativo de participación conversacional dentro de Adobe Marketo Engage. Este tutorial ofrece fórmulas procesables para implementar casos de uso como reserva de reuniones de ventas, participación en contenido de sitios web y promoción de eventos/seminarios web.
role: Admin
level: Beginner
doc-type: Article
duration: 0
last-substantial-update: 2024-05-23T00:00:00Z
jira: KT-14814
source-git-commit: 4ac24e1297287adbd6832030fda5590b696e45ed
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---


# Diseño de marketing conversacional omnicanal con Dynamic Chat

Para los especialistas en marketing, su sitio web es esencial para generar posibles clientes, impulsar las conversiones y acelerar los ciclos de ventas. La interacción con los visitantes en tiempo real en su sitio web permite que su equipo de ventas clasifique a los compradores de forma más eficaz. Adobe Dynamic Chat, el canal de chat nativo dentro de su suscripción a Adobe Marketo Engage, le permite automatizar las conversaciones para ampliar las capacidades de los Marketo Engage.

Este tutorial describe el proceso de reflexión y los casos de uso principales que compartió Sara Barriuso, directora de operaciones de marketing de Cornerstone OnDemand, durante el curso &quot;Aprenda de sus colegas&quot;. Explicó cómo su organización utilizaba Dynamic Chat para maximizar las capacidades de los Marketo Engage.

## Integración de la participación conversacional en la estrategia de generación de demanda

Los visitantes exploran el sitio web por un motivo. Es posible que busquen contenido en sus productos o servicios o que busquen información de contacto para hablar con sus representantes de ventas. También podrían ser sus clientes que buscan información adicional sobre el producto. El chat permite a los visitantes del sitio web autoabastecerse y autoclasificarse si están listos para hablar con su equipo de ventas.

Cuando Sara Barriuso implementó Dynamic Chat, se sintió atraída por su perfecta integración con Marketo Engage y el [déclencheur de actividad creados previamente](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-activities){target="_blank"} que activan programas de Marketo Engage y viceversa. Desarrolló sus estrategias de interacción conversacional con tres segmentos de audiencia en mente:

1. Perspectivas desconocidas: ofrezca llamadas de demostración de forma proactiva para generar nuevos posibles clientes.
2. Clientes/posibles clientes conocidos: amplíe el tiempo que los visitantes dedican a la navegación por el contenido y ofrezca llamadas de demostración para generar oportunidades de ampliación de ventas y de venta cruzada.
3. Clientes potenciales/potenciales: proporcione experiencias personalizadas al ampliar los esfuerzos de las campañas de marketing.


## Casos de uso clave para empezar a crear los cuadros de diálogo

Para implementar estas estrategias, Sara construyó sus Diálogos de Dynamic Chat en torno a los siguientes casos de uso:

1. Cuadro de diálogo global predeterminado: dé una opción inicial a todos los visitantes, guiándolos para que realicen sus tareas de forma más eficiente.

2. Promoción del registro en eventos y seminarios web: lleve a los visitantes del sitio web a registrarse en eventos y seminarios web para canalizarlos a la fase de compra más rápidamente.

3. Ampliación de la participación en el contenido de la campaña: ofrezca un contexto adicional o aborde posibles preguntas cuando los visitantes naveguen por el contenido del sitio web.

Veamos estos casos de uso en acción, ya que Sara muestra su proceso, desde la asignación del flujo de conversación hasta la configuración de los cuadros de diálogo y la segmentación en Dynamic Chat y Marketo Engage.

### Caso de uso 1: Cuadro de diálogo global predeterminado para todos los visitantes del sitio

Este cuadro de diálogo proporciona cinco opciones iniciales entre las que los visitantes del sitio pueden elegir, lo que crea una experiencia autoguiada que les ayuda a encontrar la información que necesitan en función de su personalidad. Para empezar, es posible que desee explorar la bandeja de entrada del correo electrónico &quot;Contáctenos&quot; para identificar temas comunes y categorizarlos en opciones de Cuadro de diálogo que se aplican a los visitantes del sitio. Vea la demostración y siga los pasos a continuación para crear su cuadro de diálogo global predeterminado:

>[!VIDEO](https://video.tv.adobe.com/v/3429194/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### Fase 1

1. Cree el cuadro de diálogo y un vínculo de prueba.
2. Añada un objetivo para rastrear las conversiones (por ejemplo, envío de solicitud de demostración).
3. Pida a 2-3 personas que lo prueben y recopilen comentarios.

#### Fase 2

1. En &quot;Audiencia&quot;, añada una URL de página web en &quot;Destino&quot; para indicar dónde se mostrará el cuadro de diálogo.
2. En &quot;Configuración&quot;, añada el nombre, la descripción, la prioridad y el idioma de la campaña.
3. Haga clic en &quot;Publicar&quot;

>[!TAB Marketo Engage]

#### Fase 1

1. Cree su campaña inteligente de seguimiento.
2. En &quot;Lista inteligente&quot;, utilice el déclencheur &quot;Alcanza el objetivo del diálogo&quot;. Utilice el mismo objetivo (por ejemplo, Solicitud de demostración) que utilizó Diálogo
3. En &quot;Flujo&quot;, incluya el paso &quot;Cambiar estado del programa&quot; para rastrear la conversión.
4. La fuente se mostrará como &quot;dynamicChat&quot;. Puede crear una campaña inteligente para actualizar el origen a un nombre que tenga sentido para usted.

#### Fase 2

1. Vuelva a probar la campaña inteligente de seguimiento cuando esté activa.

>[!ENDTABS]

#### Subir de nivel: marketing basado en cuentas

Puede mejorar aún más el cuadro de diálogo global predeterminado incorporando contenido orientado al sector, lo que hace que las conversaciones sean aún más útiles para los visitantes. Por ejemplo, puede sugerir documentos técnicos o casos prácticos específicos del sector para que los descarguen sus visitantes. Vea la demostración y siga los pasos a continuación para crear un cuadro de diálogo global predeterminado para el marketing basado en cuentas:

>[!VIDEO](https://video.tv.adobe.com/v/3429195/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Clone el &quot;Cuadro de diálogo predeterminado&quot; y renómbrelo.
2. En &quot;Stream Designer&quot;, adapte los mensajes de diálogo al sector de destino (solo un flujo + la pregunta inicial).
3. Pida a 2-3 personas que prueben el cuadro de diálogo y recopilen comentarios.
4. Cree un vínculo de prueba y compártalo.
5. En &quot;Audiencia&quot;, añada una URL de página web en la que el cuadro de diálogo muestre y actualice el destinatario según el sector que desee.
6. En &quot;Configuración&quot;, añada el nombre de la campaña, la prioridad de la descripción y el idioma.
7. Haga clic en Publicar.

>[!TAB Marketo Engage]

1. Cree su campaña inteligente de seguimiento y pruebe el objetivo.
2. Vuelva a probar la campaña inteligente de seguimiento después de publicar el cuadro de diálogo.

>[!ENDTABS]

### Caso de uso 2: Promoción del registro en eventos y seminarios web

Los eventos y seminarios web son tácticas de marketing populares para que las empresas B2B generen demanda. Ofrecen experiencias atractivas e información enriquecida que atraen a clientes potenciales. La conexión de los visitantes de su sitio web a los próximos eventos y seminarios web le permite calificar a los clientes potenciales aún más rápido. La creación de este cuadro de diálogo supone un esfuerzo reducido y un coste bajo. Puede demostrar su éxito rápidamente, ya que le ayuda a obtener el apoyo de las partes interesadas en el marketing para añadir participación conversacional a su plan de automatización omnicanal. Vea la demostración y siga los pasos a continuación para crear su cuadro de diálogo de promoción de evento/seminario web:

>[!VIDEO](https://video.tv.adobe.com/v/3429196/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### Fase 1

Cree una plantilla para el cuadro de diálogo &quot;Registro de eventos&quot; para el uso continuo de la campaña.

#### Fase 2

1. Clone la plantilla.
2. Copiar y pegar texto en el mensaje de diálogo para un nuevo evento
3. Actualice los parámetros de UTM utilizados en el vínculo de evento (por ejemplo, utm_medium=website&amp;utm_source=adobe).
4. Cree un vínculo de prueba, haga clic en &quot;Publicar&quot; y compártalo con el solicitante.
5. Revisar por pares y aplicar comentarios.


>[!TAB Marketo Engage]

#### Fase 1

1. Cree su campaña inteligente de seguimiento dentro de la plantilla del programa de seminario web/evento y pruébela.

#### Fase 2

1. Añada su nombre de campaña al seguimiento de la campaña inteligente en Marketo Engage y pruébelo.

>[!ENDTABS]


#### Subir de nivel: registrar a personas conocidas

Puede ofrecer una experiencia aún mejor a los visitantes del sitio web registrándolos para sus eventos y seminarios web sin tener que rellenar un formulario. Las experiencias personalizadas generan confianza y muestran a los visitantes que los recuerda. Vamos a ver cómo subir de nivel su evento y la promoción de seminarios web Diálogo en acción.

>[!NOTE]
>Tenga en cuenta el posible riesgo de seguridad que implican ciertos estados o países de protección e implemente esta personalización cuidadosamente consultando con su equipo legal.

>[!VIDEO](https://video.tv.adobe.com/v/3429197/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Clone el cuadro de diálogo Promoción de evento/seminario web.
2. En Stream Designer, después de que el usuario responda &quot;Sí&quot;, agrega una tarjeta de preguntas &quot;Anteriormente has compartido tu dirección de correo electrónico con nosotros. ¿Desea conservar esto para los detalles del evento?&quot;
3. Si responden &quot;Sí&quot;, añada una tarjeta de mensaje &quot;Recibirá un correo electrónico de confirmación en su correo electrónico con los detalles del evento/seminario web&quot;.
4. Si responden &quot;No&quot; - añada una tarjeta de mensaje &quot;Por favor, rellene el formulario en la página de registro&quot;.
5. Cree un vínculo de prueba, haga clic en &quot;Publicar&quot; y compártalo con el solicitante.
6. En la pestaña Audiencia, añada [el correo electrónico no está vacío].

>[!TAB Marketo Engage]

1. Añada este nuevo cuadro de diálogo al seguimiento de la campaña inteligente en Marketo Engage y pruébelo.

>[!ENDTABS]

### Caso de uso 3: Ampliación de la participación en el contenido de una campaña

Imagina que una pantalla de ventana cautivadora llama la atención y te atrae a una tienda. Si un recepcionista le ayuda a seleccionar productos o responde a sus preguntas, es posible que se sienta más cómodo haciendo una compra. Para replicar esta experiencia en línea, puede hacer que el cuadro de diálogo del Dynamic Chat aparezca en las páginas web donde las campañas de marketing dirigen a los visitantes. A medida que los usuarios interactúan con el contenido web, Dynamic Chat muestra inmediatamente conversaciones relevantes, sugiriendo contenido adicional o abordando posibles preguntas. Esto se logra aprovechando los déclencheur de automatización para activar campañas de Dynamic Chat basadas en la participación del usuario dentro de los programas de Marketo Engage. Ahora, veamos cómo dar vida a este caso de uso.

>[!VIDEO](https://video.tv.adobe.com/v/3429199/?learn=on)

Ampliación de la participación en el contenido de Campaign: configuración:

>[!VIDEO](https://video.tv.adobe.com/v/3429200/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Genere nuevos posibles clientes para sus campañas a través del correo electrónico y los puntos de contacto de las campañas sociales. En este ejemplo, la encuesta del índice de salud Talent está alojada en el sitio web de la marca.
2. Clone una plantilla de cuadro de diálogo existente (por ejemplo, un cuadro de diálogo global predeterminado) para crear tres cuadros de diálogo para los siguientes escenarios y actualizar la &quot;URL de destino&quot; en la pestaña &quot;Audiencia&quot; en consecuencia:
   * Cuando los visitantes web provienen de sus canales de marketing y llegan a su página web.
   * En la página de agradecimiento
   * Visitantes que regresan al sitio web dentro de los 45 días posteriores a la participación en la campaña de marketing (retargeting).

>[!ENDTABS]

## ¿Qué sigue?

* Mapa del flujo de conversación en [Diseñador de secuencias](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/automated-chat/stream-designer){target="_blank"} o un diagrama de flujo sin conexión.
* Cree un cuadro de diálogo global predeterminado en el Dynamic Chat.
* Active las conversaciones posteriores a la campaña utilizando déclencheur de automatización en Marketo Engage.


## Autores

{{sara-barriuso}}

{{amy-chiu}}