---
title: "Proceso y técnicas de gestión de incidentes de seguridad"
subtitle: "Optimizando la Resolución de Incidentes de Seguridad: Estrategias, Procesos y Herramientas para una Gestión Eficiente | Normativas ISO 27001"
tags: ["redes"]
authors: ["blindma1den", "lorenagubaira"]

---

Los incidentes en la seguridad de la información parecen inevitables hoy en día por lo que no tenemos más remedio que plantearlos como vamos a gestionar dichos incidentes de la manera más ágil y eficiente para la organización

Es por ello que la norma **[ISO 27001](https://normaiso27001.es/)** dedica un capítulo a establecer controles para gestionar los incidentes en la seguridad de la información e inclusive se ha dedicado un documento específico con los principios para gestionar incidentes en la seguridad de la información

### Objetivo 1: Gestión de incidentes y mejoras de seguridad de la información

Garantizar un enfoque consistente y eficaz para la gestión de incidentes de seguridad de la información, incluyendo la comunicación de eventos de seguridad y debilidades.

Como hemos mencionado, un análisis de riesgos no puede concluir con la eliminación total de las vulnerabilidades pues esto aún ni siquiera seria práctico o viable por lo que las vulnerabilidades residuales siempre existen por lo que tendremos de seguro incidentes en la seguridad de la información además de que puedan surgir amenazas o y vulnerabilidades no identificadas hasta ahora.

Es por ello que debemos implementar una herramienta para la gestión de los incidentes de la seguridad de la información con los siguientes objetivos generales

- **Detectar**, informar y evaluar incidentes de la Seguridad de la información
- **Responder** a incidentes
- **Reportar** vulnerabilidades
- **Aprender** de los incidentes de la Seguridad de la información

## Los pasos para la resolución de incidentes

La gestión de incidentes de seguridad se basa en diferentes pasos, que incluyen:

![Gestión de incidentes](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/incident-management/incident-management-image-1.jpg)

> *NOTA: Estos pasos podrían ser estados diferentes que un incidente por lo que también es importante informar al usuario sobre cualquier cambio en el estado del incidente.*

- **1. Notificación del incidente:** una persona detecta un evento que puede dañar el funcionamiento de la organización, por lo que necesita comunicar el incidente de acuerdo con los procedimientos de comunicación de la organización (generalmente un correo electrónico, una llamada telefónica, una herramienta de software, etc.)
- **2. Clasificación del incidente:** una persona recibe la notificación del incidente y, según los diversos parámetros, se clasifica. La persona que detecta el incidente también puede hacer una clasificación, pero es un experto técnico que lo clasifica de la manera adecuada.
- **3. Tratamiento del incidente:** una vez que se clasifica el incidente y se conoce la gravedad y el tiempo acordado para su resolución, un experto técnico debe decidir sobre las medidas necesarias para resolverlo.
- **4. Cierre el incidente:** una vez que se resuelve el incidente, se registra toda la información generada durante el tratamiento y, finalmente, se notifica a la persona que envió primero la notificación del incidente que se cerró.
- **5. Base de conocimiento:** toda la información generada durante el tratamiento del incidente es crítica para posibles incidentes similares en el futuro, así como para recopilar evidencia. Imagine que un usuario actualiza un sistema y luego de esto, el sistema se cierra (involuntariamente). Luego, el usuario abre un incidente y el incidente se resuelve y se cierra. La información generada para resolver el incidente se registra, por lo que si el problema vuelve a ocurrir en el futuro, simplemente pueden referirse a la base de conocimiento; Tendrán la solución perfecta sin perder tiempo.

> 👉 En este sentido la norma establece una serie de controles empezando por la organización que debemos llevar a cabo para acometer esta tarea

## Controles para la gestión de incidetes de la seguridad de la información

### Responsables y procedimientos

En primer lugar deberemos tener implantado y documentado los procedimientos que nos dirijan en el proceso de gestión de incidentes de la seguridad de la información.

Estos procesos deben tener en cuenta:

- **Las responsabilidades**
    - Defina un responsable o responsables para la gestión de incidentes quien deberá garantizar que se desarrollan los procedimientos adecuados para que se realicen todas las tareas o procesos necesarios para gestionar los incidentes.
    - Defina las responsabilidades de cada empleado tanto en la colaboración para la respuesta, como en la necesidad de comunicación de los incidentes de seguridad de la información.
- **Los procesos o procedimientos**
    - Que existan procedimientos para la detección, análisis y elaboración de informes de incidentes de la seguridad de la información.
    - Elabore procedimientos para que se comuniquen los incidente.
    - Que dichos procedimientos sean conocidos (Que cada empleado conozca los procedimientos de comunicación de incidentes y sus responsabilidades).
    - Que existan vías de comunicación adecuadas (asegúrese de que se definen los puntos de recogida de información para los incidentes y eventos de la seguridad de la información).
- **Capacitación**
    - Asegúrese de la competencia del personal de atención y resolución de incidentes. Mantenga un plan de capacitación de las personas que se ocupan de los incidentes de la seguridad de la información.

## Reportes de eventos de seguridad de la información

Este control nos pide que establezcamos los canales de comunicación para todos los eventos o incidentes. Estos canales, naturalmente deben estar establecidos con los responsables de la gestión de los incidentes.

Es importante que todos los usuarios estén informados y familiarizados con los mecanismos de notificación. Con usuarios nos referimos a usuarios tanto internos como externos.

Antes que nada vamos a distinguir entre dos conceptos más o menos similares pero que debemos separar para un correcto análisis de los incidentes en la Seguridad de la Información.

### Evento de la seguridad de la información

Cualquier ocurrencia identificada en un sistema de información, servicio o estado de la red que indica una posible infracción en la seguridad de la información, en la política o fallo en los controles, o una situación previamente desconocida que puede ser relevante para la seguridad.

### Incidente de la seguridad de la información

Cuando el evento se puede clasificar como no deseado o inesperado dentro de los eventos de seguridad de la información y además tienen una probabilidad significativa de comprometer las operaciones comerciales y suponen una seria amenaza para la seguridad de la información.

Un evento en la seguridad de la información no significa necesariamente una implicación en la confidencialidad, integridad o disponibilidad a veces incluso lo deseamos, podemos aprender de ello y endurecer la seguridad.

- El incidente siempre es indeseado

### Aclarando conceptos: amenaza, vulnerabilidad, evento e incidente

![Gestión de incidentes - amenaza, vulnerabilidad, evento e incidente](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/incident-management/incident-management-image-2.jpg)

## Amenaza para la Seguridad de la información

> *Una amenaza se refiere a cualquier cosa que tenga el potencial de causar daños graves a un sistema o activo de información. Una amenaza es algo que puede suceder o no, pero tiene el potencial de causar un daño grave.*
>
> *Las amenazas pueden provocar ataques a sistemas informáticos, redes y más.*

### Vulnerabilidad en la Seguridad de la información

Se refiere a una debilidad o defecto en un sistema o activo de información que puede dejarlo expuesto a una amenaza o ataque. Una vulnerabilidad también puede referirse a cualquier tipo de debilidad en un sistema de información en sí mismo, en un conjunto de procedimientos o en cualquier cosa que deje la seguridad de la información expuesta a una amenaza.

### Evento en la Seguridad de la información

Un evento de seguridad de la información es un cambio en las operaciones diarias de una red o servicio de tecnología de la información que indica que una política de seguridad puede haber sido violada o una protección de seguridad puede haber fallado.

### Incidente en la Seguridad de la información

Una sola o una serie de eventos de seguridad de la información no deseados o inesperados que tienen una probabilidad significativa de comprometer las operaciones comerciales y amenazar seguridad de información. Por ejemplo un comportamiento anómalo en un sistema es un evento, sin embargo, si se encuentra evidencia del virus en el sistema, se puede considerar un incidente de seguridad.

### Reporte de debilidades de seguridad de la información

El reporte de incidentes debe acompañarse con un reporte de posibles debilidades del sistema que se detecten en cualquier momento. Esto debe estar soportado por:

- La comunicación a los usuarios de la exigencia de observar y reportar cualquier debilidad de seguridad de la información vista o sospechada en sistemas o servicios

> 💡 Se aconseja advertir que los usuarios que probar la fortaleza o debilidad de los sistemas a ver si encuentran una vulnerabilidad serán considerados por la compañía como un mal uso del sistema

### Evaluación y decisión sobre los eventos de seguridd de información

Como ya hemos visto en los puntos anteriores, los eventos de la seguridad de la información pueden clasificarse en simples eventos o pueden pasar a ser Indecentes de la seguridad de la información

Para ello establece:

- Un criterio de priorización de incidentes dependiendo del sistema o servicio afectado, del usuario etc.
- La evaluación de incidentes debe ser realizada tanto por el usuario como por el equipo de gestión que debe revisar la prioridad.
- Lleve un registro de la evaluación de los incidentes para poder analizar los parámetros de calidad tanto en su resolución como de su clasificación.

Hay muchas formas de clasificar incidentes, pero lo habitual es considerar dos parámetros:

- **Impacto:** Daño causado al negocio (en términos económicos, imagen, etc.)
- **Urgencia:** La rapidez con la cual la organización necesita corregir el incidente

La combinación de estos parámetros nos permitirá determinar la prioridad de cada incidente, por lo que de esta manera puede establecer, por ejemplo, la siguiente tabla de valores:

![Gestión de incidentes - Nivel de amenazas](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/incident-management/incident-management-image-3.jpg)

Así podríamos clasificar las incidencias en:

- **NIVEL CRÍTICO (5 a 6)**
- **NIVEL GRAVE (4)**
- **NIVEL LEVE (1 a 2)**

### Respuesta a incidentes de seguridad

Se trata de controlar el proceso de resolución de incidentes en la seguridad de la información.

Los controles a establecer serian.

- Evalue si la organización tiene la capacidad para resolver el incidente por si misma o necesita ayuda de terceros.
- Mantenga un registro con las evidencias de las incidencias.
- Establezca el sistema de comunicaciones necesarias entre usuarios y el equipo de gestión de incidencias o quien deba estar informado de las actuaciones y situación del proceso de resolución de las incidencias.
- Registre las acciones llevadas a cabo y los resultados de las mismas.
- Cierre la incidencia formalmente cuando se haya resuelto.
- Realice un análisis para determinar las causas de cada incidente.

### Aprendiendo de los incidentes de seguridad de la información

Como ya hemos adelantado los incidentes no solo son un problema a solucionar sino una fuente de información para la resolución de futuros incidentes o para la mejora de la seguridad de la información.

Los controles de la norma para mantener una base de conocimientos sobre los incidentes en la seguridad de la información son:

- Creación de un registro que considere
- Volumen de incidentes producidos
- Tipología de incidentes producidos
- Coste de la resolución de la incidencia
- Impacto de la incidencia
- Solución aplicada

La información sobre los incidentes nos puede ayudar a:

- Identificar los incidentes más recurrentes y de alto impacto.
- Mejorar nuestro sistema de gestión con nuevos controles y criterios para la evaluación de riesgos.
- Realizar entrenamientos a los usuarios para evitar incidentes y a los gestores de incidentes para mejorar la resolución de los mismos.

> 👉 Para este último punto se recomienda utilizar datos No reales para los entrenamientos.

### Recolección de evidencia

Los incidentes sobre la seguridad de la información pueden requerir acciones posteriores como sanciones o acciones legales. Recuperar las evidencias para utilizarlas posteriormente puede volverse un dolor de cabeza si no hemos previsto algún mecanismo para guardarlas.

En este capítulo la norma nos pone como control el que conservemos la información sobre las incidencias de forma que podamos recuperar:

- Los inicios y cierres de sesión
- Las identificaciones
- El estado de los dispositivos y de las redes
- Las evidencias de reuniones informativas, documentación sobre responsabilidades y funciones de seguridad del personal

***No debe pasar por alto…***

En ocasiones puede ser necesaria una investigación forense de las evidencias informáticas. Conviene tener en cuenta mantener a salvo los derechos de acceso a la información para poder realizar una investigación forense.

Para ello hay que tener en cuenta los distintos requisitos de las jurisdicciones pertinentes y estar preparados mediante la comunicación previa al personal o la firma de cláusulas contractuales

- **Otro tema es la preservación de las evidencias…**

Los incidentes no sabemos normalmente en que van a terminar y si requerirán posteriores acciones legales o disciplinarias Determinadas incidencias pueden conllevar el borrado de las evidencias con el objeto de ocultar al responsable de las mismas, es por ello que se recomienda establecer sistemas de copiado y preservación de registros con tal de que ciertas evidencias no se puedan eliminar tan fácilmente.

- **Seguridad de las evidencias…**

Finalmente si es posible o se identifica como necesario se pueden certificar los sistemas de recogida de evidencias o mantener medios de vigilancia y control independientes (homologados y legales) para fortalecer las evidencias de cara a acciones legales

## Herramientas de gestión de incidentes de seguridad

Nos gustaría destacar que la gestión de incidencias no se hace sólo con una herramienta, sino con la selección correcta de herramientas, las mejores prácticas y el equipo de DevOps. Vamos a hablar de nuestras herramientas de gestión de incidencias favoritas que creemos que marcan la diferencia en el proceso de gestión de incidencias:

- [BigPanda](https://www.bigpanda.io/)
- [OnPage](https://www.onpage.com/)
- [NinjaRMM](https://www.ninjarmm.com/)
- [Rundeck](https://www.rundeck.com/open-source)
- [ServiceNow](https://www.servicenow.com/)
- [Issuetrak](https://www.issuetrak.com/)
- [AlertOps](https://alertops.com/)
- [Atlassian](https://www.atlassian.com/software/jira/service-management/features/service-desk)

Hay otras herramientas estupendas que ayudan a realizar el seguimiento de los incidentes, que cada incidente puede ser rastreado y documentado para poder identificar tendencias y hacer comparaciones a lo largo del tiempo. Hay algunas salas de chat que permiten la comunicación de texto en tiempo real para diagnosticar y resolver el incidente como un equipo y proporcionar un rico conjunto de datos para el análisis de la respuesta más tarde. Además, el chat de vídeo complementa el chat de texto para muchos incidentes, el chat de vídeo en equipo puede ayudar a discutir los hallazgos y trazar una estrategia de respuesta. El sistema de alertas, que es extremadamente importante, se integra con su sistema de supervisión y gestiona las rotaciones de guardia y las escaladas. Las herramientas de documentación, como Confluence, pueden capturar los documentos del estado de los incidentes y los postmortem.
