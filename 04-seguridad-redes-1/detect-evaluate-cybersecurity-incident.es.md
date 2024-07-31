---
title: "Detección, Evaluación y Análisis"
technology: ["cybersecurity"]

---

> **Detección: Identificación y Gestión de Elementos Indicadores de un Incidente**

La fase de detección es crucial para identificar que algo no está bien. Los mecanismos de detección incluyen varias fuentes y señales:

## Mecanismos de Detección

- **Alertas en sistemas de seguridad:** Los programas como los antivirus y sistemas de detección de intrusos generan alertas cuando detectan actividad sospechosa. Es vital que los administradores de TI tengan conocimiento total sobre los comportamientos de la infraestructura que están administrando.
- **Caídas de servidores:** Una caída inesperada de un servidor puede ser un indicio de un ataque o problema de seguridad. Los logs de servidores son esenciales para investigar la causa.
- **Reportes de usuarios:** Los usuarios a menudo son los primeros en notar comportamientos anómalos, como dificultades para acceder a sistemas o datos. Tener conocimientos de las características normales a nivel de red y de los sistemas ayuda a diferenciar entre problemas técnicos y posibles incidentes de seguridad.
- **Software antivirus dando informes:** Los antivirus no solo eliminan amenazas, sino que también generan informes detallados sobre posibles infecciones y actividades sospechosas.
- **Otros funcionamientos fuera de lo normal del sistema:** Cualquier comportamiento inusual en el sistema, como lentitud inesperada o acceso no autorizado a archivos, puede ser un indicador de un incidente.

Para detectar eficazmente los incidentes, es fundamental contar con una **única fuente de tiempo** (sincronización de relojes), ya que esto facilita la correlación de eventos y el análisis de información.

## Elementos que Alertan sobre un Incidente

- **Logs de servidores:** Los registros detallados de actividades en los servidores pueden revelar patrones anómalos. Toda información que permita realizar análisis al incidente debe estar centralizada.
- **Logs de aplicaciones:** Los logs de las aplicaciones pueden mostrar intentos de acceso no autorizados y otros comportamientos inusuales.
- **Logs de herramientas de seguridad:** Estos logs son cruciales para identificar intentos de intrusión y otras amenazas de seguridad.
- **Otras herramientas de identificación:** Cualquier herramienta que permita la identificación de un incidente de seguridad es valiosa. Es importante efectuar correlación de eventos para descubrir patrones de comportamiento anormal y poder identificar de manera más fácil la causa del incidente.

## Evaluación y Análisis de la Incidencia
Una vez detectada la incidencia, evaluarla y analizarla en detalle es esencial para comprender su impacto y tomar las medidas adecuadas.

- **Revisión de logs:** Examinar minuciosamente los registros de eventos para identificar el origen y la trayectoria del ataque. Para un correcto análisis de un incidente, debe existir una única fuente de tiempo.
- **Entrevistas:** Hablar con los usuarios afectados y otros testigos puede proporcionar contexto adicional sobre lo ocurrido.
- **Herramientas de análisis:** Utilizar software especializado para examinar archivos sospechosos y tráfico de red.

## Clasificación y Priorización

Clasificar y priorizar las incidencias ayuda a determinar la gravedad y el tipo de respuesta necesaria.

- **Clasificación:** Identificar la gravedad de la incidencia (baja, media, alta) en función del impacto en el negocio y la sensibilidad de los datos afectados.
- **Priorización:** Determinar el orden de atención basado en el impacto y el alcance de la incidencia. Crear matrices de diagnóstico e información para los administradores menos experimentados es una buena práctica.

### Nivel de Prioridad

La prioridad de un incidente depende del valor o importancia dentro de la entidad y del proceso que soporta el o los sistemas afectados. A continuación se presentan diferentes niveles de criticidad:

| Nivel Criticidad | Valor | Definición |
| --- | --- | --- |
| Inferior | 0,10 | Sistemas no críticos, como estaciones de trabajo de usuarios con funciones no críticas. |
| Bajo | 0,25 | Sistemas que apoyan a una sola dependencia o proceso de una entidad. |
| Medio | 0,50 | Sistemas que apoyan más de una dependencias o proceso de la entidad. |
| Alto | 0,75 | Sistemas pertenecientes al área de Tecnología y estaciones de trabajo de usuarios con funciones críticas. |
| Superior | 1,00 | Sistemas Críticos. |

- **Impacto Actual:** Depende de la cantidad de daño que ha provocado el incidente en el momento de ser detectado.
- **Impacto Futuro:** Depende de la cantidad de daño que pueda causar el incidente si no es contenido ni erradicado.

| Nivel Impacto | Valor | Definición |
| --- | --- | --- |
| Inferior | 0,10 | Impacto leve en uno de los componentes de cualquier sistema de información o estación de trabajo. |
| Bajo | 0,25 | Impacto moderado en uno de los componentes de cualquier sistema de información o estación de trabajo. |
| Medio | 0,50 | Impacto alto en uno de los componentes de cualquier sistema de información o estación de trabajo. |
| Alto | 0,75 | Impacto moderado en uno o más componentes de más de un sistema de información. |
| Superior | 1,00 | Impacto alto en uno o más componentes de más de un sistema de información. |

Luego de definir estas variables, se calcula la prioridad mediante la siguiente fórmula:

\[ \text{Nivel de Prioridad} = (\text{Impacto Actual} \times 2.5) + (\text{Impacto Futuro} \times 2.5) + (\text{Criticidad del Sistema} \times 5) \]

Los resultados se comparan con la siguiente tabla para determinar la prioridad de atención:

| Nivel Prioridad | Valor |
| --- | --- |
| Inferior | 00,00 – 02,49 |
| Bajo | 02,50 – 03,74 |
| Medio | 03,75 – 04,99 |
| Alto | 05,00 – 07,49 |
| Superior | 07,50 – 10,00 |

### Tiempos de Respuesta

Para la atención de incidentes de seguridad, se establecen tiempos máximos de respuesta según la criticidad e impacto del incidente. Los tiempos en la siguiente tabla representan el tiempo máximo en que el incidente debe ser atendido, no necesariamente solucionado, ya que la solución puede variar según el caso.

| Nivel Prioridad | Tiempo de Respuesta |
| --- | --- |
| Inferior | 3 horas |
| Bajo | 1 hora |
| Medio | 30 min |
| Alto | 15 min |
| Superior | 5 min |


Cada entidad tiene la libertad de definir los tiempos de atención según consideren conveniente y según la criticidad de los activos impactados.

## Conclusión
La gestión de incidencias de seguridad requiere un enfoque sistemático y bien coordinado. Mantener y usar una base de conocimiento con información sobre nuevas vulnerabilidades, información de los servicios habilitados, y experiencias con incidentes anteriores es crucial para mejorar continuamente el proceso de detección, evaluación y análisis. Siguiendo estos pasos, las organizaciones pueden responder de manera efectiva a incidentes de seguridad, minimizar el daño y proteger sus activos más valiosos.
