---
title: "Confirmación y evaluación inicial de un incidente de ciberseguridad"

---

Este artículo ofrece una guía completa sobre cómo las empresas pueden estructurar un proceso de notificación de incidentes, implementar estrategias para tomar decisiones oportunamente y evitar la propagación del incidente. Además, se detalla cómo manejar las actividades post-incidente y preparar un reporte que incluya las lecciones aprendidas. Por último, se identifican todos los roles involucrados en la gestión de incidentes para asegurar una respuesta coordinada y efectiva.

## Proceso de Notificación de Incidentes

En esta sección, se presenta una guía sobre cómo establecer un proceso de notificación de incidentes efectivo, que incluye la detección, inicialización de la notificación, y los canales de comunicación adecuados para asegurar que los incidentes se gestionen de manera eficiente y oportuna.

### Detección del Incidente:

Todos los empleados deben estar capacitados para reconocer posibles incidentes de seguridad, se debe reportar inmediatamente cualquier sospecha de incidente al equipo de seguridad de la información.

#### Indicadores para Detectar un Incidente de Seguridad

| **Categoría**             | **Nombre del Indicador**            | **Descripción del Indicador**                                                                                                                         |
|---------------------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Técnicos**              | Actividad Inusual en la Red         | Incremento inesperado en el tráfico de red, conexiones a IPs sospechosas, picos de actividad en horas no laborales.                                      |
|                           | Alertas del IDS                     | Notificaciones de intentos de acceso no autorizado, escaneos de puertos, patrones de tráfico malicioso detectados.                                       |
|                           | Logs del Sistema                    | Registros de múltiples intentos fallidos de inicio de sesión, accesos desde ubicaciones geográficas inusuales, cambios no autorizados en configuraciones. |
|                           | Comportamiento Anómalo de Usuarios  | Actividades que no coinciden con los patrones normales de uso, como accesos a datos sensibles por parte de empleados sin privilegios.                   |
|                           | Archivos y Aplicaciones Sospechosos | Presencia de archivos no reconocidos, modificaciones no autorizadas en archivos existentes, o instalación de aplicaciones sin aprobación.               |
| **Físicos**               | Accesos No Autorizados              | Intentos de acceso físico a áreas restringidas, como salas de servidores o equipos sensibles.                                                           |
|                           | Dispositivos Desconocidos           | Detección de dispositivos no reconocidos conectados a la red, como unidades USB, laptops, o dispositivos móviles.                                        |
| **De la Empresa**         | Comportamiento del Personal         | Informes de empleados sobre comportamientos sospechosos o dispositivos que funcionan de manera inusual.                                                |
|                           | Problemas de Rendimiento            | Lentitud inexplicable en el rendimiento del sistema o caídas inesperadas de servicios críticos.                                                         |
|                           | Desaparición de Datos               | Pérdida o corrupción de datos sin explicación aparente.                                                                                                |
| **Externos**              | Alertas de Proveedores de Seguridad | Notificaciones de proveedores de servicios de seguridad sobre amenazas emergentes que podrían afectar a la organización.                                |
|                           | Noticias y Reportes                 | Informes de medios de comunicación o alertas de seguridad pública sobre nuevas vulnerabilidades o ataques que podrían estar relacionados con la empresa. |
  

### Inicialización de la Notificación:

Proveer un formulario estandarizado para la notificación inicial que incluya detalles como:

   - Fecha y hora del descubrimiento.
   - Descripción del incidente.
   - Sistemas afectados.
   - Datos potencialmente comprometidos.

### Canales de Comunicación

   - **Correo Electrónico:** Un correo electrónico dedicado a incidentes de seguridad.
   - **Teléfono:** Línea directa de emergencia para incidentes críticos.
   - **Sistema de Gestión de Incidentes (ITSM):** Utilización de una plataforma ITSM para registrar y gestionar los incidentes.

### Confirmación y Evaluación Inicial

Debe habar un `Equipo de Respuesta a Incidentes` (IRT) encargado de evaluar la validez y gravedad del incidente reportado. Tambien debe asegurar que todos los detalles del incidente se registren adecuadamente.

### Confirmación y Evaluación Inicial del Incidente

La confirmación y evaluación inicial de un incidente son pasos cruciales para determinar la veracidad y gravedad de una potencial amenaza. Este proceso asegura que los recursos de la organización se utilicen de manera efectiva y que las medidas adecuadas se tomen de inmediato.

#### 1. Confirmación del Incidente

**Equipo de Respuesta a Incidentes (IRT):**
   - **Recepción del Reporte:** El IRT recibe la notificación del incidente a través de los canales designados (correo electrónico, teléfono, sistema ITSM).
   - **Verificación Inicial:** El equipo revisa la información proporcionada en la notificación para verificar su validez y relevancia. Esto puede incluir revisar logs del sistema, alertas del IDS, y entrevistar a la persona que reportó el incidente.
   - **Análisis de la Fuente:** Identificar si la fuente del reporte es confiable y si los datos proporcionados son consistentes con la naturaleza del incidente.

#### 2. Evaluación Inicial del incidente de seguridad

**Gravedad del Incidente:** Determinar el nivel de amenaza que representa el incidente. Esto incluye evaluar el potencial impacto en los sistemas críticos, la confidencialidad, integridad y disponibilidad de los datos. A continuacion una lista de posibles niveles de gravedad:

   - **Bajo:** Incidentes menores con impacto limitado, como intentos de phishing sin éxito.
   - **Medio:** Incidentes con impacto moderado que requieren atención, como malware detectado en una máquina de un usuario.
   - **Alto:** Incidentes graves con potencial de causar daño significativo, como una brecha de datos o un ataque ransomware.

**Alcance del Incidente:** Identificar qué sistemas, redes, datos y usuarios están afectados. Esto puede implicar: Revisar logs de acceso y actividad de red, Inspeccionar dispositivos comprometidos, Evaluar la propagación potencial del incidente a otros sistemas, etc.

**Establecimiento de Prioridades:** Basado en la gravedad y alcance del incidente, asignar los recursos necesarios para manejar la situación de manera efectiva. Informar y coordinar con otros departamentos relevantes, como TI, legal, y comunicaciones, para asegurar una respuesta unificada.

Una evaluación inicial efectiva permite a la organización tomar decisiones informadas rápidamente y minimizar el impacto del incidente en las operaciones.
